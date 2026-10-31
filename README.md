# bumpsite — BumpSugar waitlist 落地页

纯静态、零依赖 waitlist 落地页（单文件 `index.html`：内联 CSS、内联 SVG、data-URI favicon，
无任何外部请求、无 JS 框架）。上线文案为英文（US 区），每个文案区块旁有 `<!-- 中：... -->`
中英对照注释，仅供内部维护，浏览器不渲染。

对应上游文档：定位与红线 `out/gdm/prd.md`（§2.3 定位、§8.2 免费层、§9 合规）、
SEO 选词 `out/gdm/aso-dataset.md` §9、站点规范与标准免责 `out/gdm/content-plan.md` §2。

## 文件清单

| 文件 | 作用 |
|---|---|
| `index.html` | 页面本体：hero（定位一句话 + 三差异徽章）、功能三卡（P0 log/trends/doctor PDF）、waitlist 表单、FAQ（7 条，含数据隐私）、页脚完整免责声明、SEO meta + FAQ JSON-LD |
| `robots.txt` | 允许全站抓取（单页站暂不需要 sitemap） |
| `README.md` | 本文件：部署、域名、表单接入、TODO |

## 本地预览

```bash
cd bumpsite
python3 -m http.server 8080
# 打开 http://localhost:8080
```

## 部署：Cloudflare Pages

零构建静态站：**Build command 留空，Build output directory 填 `/`**。

方式 A（最快）：Dashboard → Workers & Pages → Create → Pages → **Upload assets**，
把 `bumpsite/` 目录拖进去，项目名填 `bumpsugar`（决定兜底子域 `bumpsugar.pages.dev`）。

方式 B（CLI）：

```bash
npm i -g wrangler
wrangler login
wrangler pages deploy . --project-name bumpsugar
```

后续更新：改完文件重跑方式 B（或 Dashboard 里重新 Upload）即可。

### 自定义域名建议

- 主域候选：`bumpsugar.com` / `bumpsugar.app` / `bumpsugar.health`。
  ⚠️ **可用性本次未验证**：PRD 只完成了 App Store 层撞名实测（aso-pack §7.2，
  bumpsugar 无同名 App），域名是否可注册需在注册商查询，USPTO 商标粗查仍是 PRD §11#6 未结项。
- 建议域名与 DNS 放同一 Cloudflare 账号（如 Cloudflare Registrar 购入），然后
  Pages 项目 → **Custom domains** → 添加 `bumpsugar.com` 与 `www.bumpsugar.com`，
  证书由 Cloudflare 自动签发。
- 兜底子域：`bumpsugar.pages.dev`。本次构建时在大陆 DNS（202.96.134.133，2026-10-29）
  `nslookup` 返回 NXDOMAIN——可能是未占用，也可能是大陆对 pages.dev 的 DNS 污染，
  **无法确证可占性**；部署时若提示子域冲突就换项目名，并同步改 `index.html` 的
  canonical / og:url。

### 表单接入（上线前必改，TODO 见 index.html 表单注释）

当前 `action="https://TODO-REPLACE-WITH-REAL-ENDPOINT.example/subscribe"` 是占位端点，
提交会失败。三个选项按推荐序：

**选项 1（推荐，零后端心智）：表单服务**（Formspree / Basin / Getform 等）
建一个表单拿到 URL，替换 action 即可；蜜罐字段名 `website` 是通用做法，
Formspree 内置 `_gotcha`，可把字段改名或在其后台开启等价开关。

**选项 2：Cloudflare Pages Functions（自己存）**
在站点根目录加 `functions/api/subscribe.js`（Pages 会自动路由 `/api/subscribe`），
表单 action 改为 `/api/subscribe`，并在 wrangler/Dashboard 绑一个 KV namespace（绑定名 `WAITLIST`）：

```js
// functions/api/subscribe.js — 最小可用版：存入 KV，无邮件通知
export async function onRequestPost(context) {
  const form = await context.request.formData();
  const email = (form.get("email") || "").toString().trim();
  const hp = (form.get("website") || "").toString(); // 蜜罐：必须为空
  if (hp) return new Response(null, { status: 204 });
  if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email) || email.length > 254) {
    return new Response("invalid email", { status: 400 });
  }
  const key = "waitlist:" + email.toLowerCase();
  if (!(await context.env.WAITLIST.get(key))) {
    await context.env.WAITLIST.put(key, new Date().toISOString());
  }
  return Response.redirect(context.env.CANONICAL_URL || "https://bumpsugar.pages.dev/", 303);
}
```

⚠️ 这只把邮箱存进 KV（导出靠 `wrangler kv key list --binding WAITLIST`）。
要收到新订阅提醒，再接一个邮件 API（如 Resend，需注册账号）或干脆用选项 1。

**选项 3：邮件服务订阅 API**（Buttondown / MailerLite 等）：适合之后直接发 launch 邮件，
把表单换成该服务的订阅 action/嵌入码。

### SEO 待办

- 绑定正式域名后：替换 `index.html` 中 `canonical`、`og:url`，补 `og:image`（1200×630，放站点根目录）。
- 上线后在 Google Search Console + Bing Webmaster 提交；GSC 是选词验证的唯一合规路径
  （全场无搜索量数据，aso-pack.md:374），按 content-plan §5 用 GSC 展示数据迭代。
- title/description 已按 aso-dataset §9 的素人词缺口写（`gestational diabetes log book`、
  `blood sugar tracker` 词族）；`ogtt` 与 `time in range` 两个纯空位词已自然落在 FAQ
  与功能卡里，后续内容站（content-plan A3/B5）承接深度意图。

## TODO（上线前）

- [ ] **表单 action**：按上节三选一接真实端点，删除表单处的 TODO 注释
- [ ] **正式域名**：注册 + 绑定 Cloudflare Pages + 替换 canonical / og:url / Contact 邮箱
- [ ] 隐私政策与条款真实页面（本静态站托管 `/privacy`、`/terms`，文本与 PRD §9.2 同源；
      这是 App Store Connect 提审硬要求，prd.md:302），替换页脚两个占位锚点
- [ ] og:image（1200×630）
- [ ] Google Search Console / Bing Webmaster 验证
- [ ] 定价口径复核：FAQ 的价格写的是 PRD 计划价（$19.99/6 个月）并已标注 planned，
      Beta 开放时若 A/B 调价需同步本页（prd.md:242）
- [ ] 医疗文案外部复核（PRD §11#4 机制）：本页免责声明已按 content-plan §2.2 站点标准收敛，
      上线前过一遍复核渠道

## 红线自检（本页如何满足）

- 免责声明：页面中上部显著免责条 + 页脚完整免责（educational only / not medical advice /
  consult your OB/GYN or endocrinologist / 提醒可靠性免责），同源 content-plan.md:44。
- 零临床数值：全页无任何血糖阈值、检查时点数、患病率数字，不需要外部医学引用。
- 不夸大：无 "never fail" 类绝对化承诺（提醒可靠性做了反向免责）；PDF 描述为 parity 功能、
  不写独有；定价、上线日期、平台要求均标注 planned / in development。
- 三差异徽章：No ads / No account / Data never leaves your device（prd.md:54 口径，仅三枚）。
- 表单隐私微文案显式区分「邮箱仅用于上线通知」与「血糖数据不出设备」，避免混淆性宣传。
