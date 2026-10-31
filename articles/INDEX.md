# bumpsite/articles · 新增 24 篇内容索引（batch 1–2 新稿）

> **内部策划文档**（含引流策略与差评对位打法），不是站点页面。部署 Cloudflare Pages 时建议将本文件从发布目录排除。
> 生成：2026-10-30。依据：24 篇 frontmatter 与正文出链的逐文件提取（Python 全量解析 `](...)` 链接）、关键文章（free-app 全文、just-diagnosed A1）通读、全站 44 篇文件盘点。所有数字均来自本次实测，不是估算。
> 医疗红线合规（引用可达性、逐字引文、免责/FAQ/文末导流）已由前序两轮编辑逐篇核验（26 篇次检查、33 个去重引用 URL 全部实测可达、2 处修订），本索引只登记结论、不重复该项工作（见 §6）。

## 0. 目录约定与站内快照（2026-10-30 实测）

- **为什么不是 `blog/INDEX.md`**：`bumpsite/` 下无 `blog/` 目录（全站 `find` 核实：仅 `index.html`、`README.md`、`robots.txt` 与 `articles/`）。全部文章唯一约定位置是 `articles/`，故本索引按现有约定写入 `articles/INDEX.md`。
- `bumpsite/articles/` 共 **44 篇**：旧 20 篇（A1–A6 / B1–B7 / C1–C7，文件名带 `b5-`、`c7-` 等字母前缀而 URL slug 不带）+ 本轮 24 篇。
- 全部 24 篇 frontmatter 均带 `status: draft` 与 `noindex: true`。
- **图况**：新 → 旧 65 条边（24/24 篇都有出链）；稿内互链仅 1 条；**旧 → 新回链 0 条**（20×24 逐对解析核实）；`index.html` 引用新 slug 0 处。新稿目前是单向输出。

标记说明：**⭐ = 诊断后第一周关键引流页（主）**，**◇ = 第一周支撑页**，**♦ = 差评对位关键引流页**。

## 1. 24 篇总表（标题 / 一句话意图 / 主关键词 / 引流标记）

主关键词 = 各篇 frontmatter `target_keyword` 原文；标题 = frontmatter `title` 原文。

| # | slug（=URL） | 标题 | 主关键词 | 一句话意图 | 标记 |
|---|---|---|---|---|---|
| 1 | `how-often-to-check-blood-sugar-gestational-diabetes` | How Often to Check Blood Sugar With Gestational Diabetes: Your Team Sets the Number — a System Makes It Happen | how often to check blood sugar with gestational diabetes | 确诊第一周最高频的「一天测几次」：次数由团队定，本文交付把次数写成清单+配提醒的记录系统。 | ⭐ |
| 2 | `blood-sugar-levels-in-pregnancy` | Blood Sugar Levels in Pregnancy: Every Number You'll See, What It Measures, and Who It Belongs To | blood sugar levels in pregnancy | 把孕期能遇到的每类血糖数字按「测什么/归谁解释」讲清并明确拒印目标值，是数值类搜索的全站泄压阀。 | |
| 3 | `gestational-diabetes-first-trimester` | Gestational Diabetes in the First Trimester: Starting Your Log Earlier Than Everyone Else | gestational diabetes first trimester | 比常规窗口更早确诊者的平静开局：早确诊=更早开始记录，医疗疑问全部留给团队。 | |
| 4 | `gestational-diabetes-second-trimester` | Gestational Diabetes in the Second Trimester: From the Screening Window to Your First Month of Logging | gestational diabetes second trimester | 24–28 周筛查窗口主叙事：确诊改变什么/不改变什么，第一个月如何搭起饮食+血糖日志。 | ◇ |
| 5 | `gestational-diabetes-third-trimester` | Gestational Diabetes in the Third Trimester: Weekly Visits, Insulin Conversations, and What to Bring | gestational diabetes third trimester | 晚孕期就诊加密期陪跑：间期记什么、每次产检带什么、胰岛素话题出现时只记录不指导。 | |
| 6 | `how-to-log-blood-sugar-readings` | How to Log a Blood Sugar Reading: the Complete Entry, Meter Memory, and Notes That Make Numbers Usable | how to log blood sugar readings | 一条「完整记录」的字段规范（读数+check type+真实时间戳+语境备注）与从血糖仪内存转录的方法。 | ⭐ |
| 7 | `gestational-diabetes-care-team` | Your Gestational Diabetes Care Team: Who Does What, Who Sees Your Log, and Who to Call | gestational diabetes care team | 一次拿到四张转诊单后的角色地图：谁做什么、谁看我的日志、有事找谁。 | ⭐ |
| 8 | `free-gestational-diabetes-app` | Free Gestational Diabetes Apps: What 'Free' Costs Your Data, Your Attention, and Sometimes Your Export | free gestational diabetes app | 差评对位簇枢纽：把「免费」的真实代价拆成注意力/数据/导出三种货币，交付五分钟自查清单，自然落回永久免费层。 | ♦（簇枢纽） |
| 9 | `how-to-print-blood-sugar-log` | How to Print Your Blood Sugar Log: Getting GDM Numbers Onto Paper Your Clinic Accepts | export blood sugar log（注意：与 slug 字面不同，打的是导出意图） | 导出被锁是竞品差评最集中痛点：App 导出→截图兜底→手工誊录三条路，落到诊所肯收的纸面。 | ♦ |
| 10 | `transfer-blood-sugar-log-new-phone` | New Phone, Same Log: Backing Up and Moving Your GDM Reading History | transfer blood sugar log to new phone | 换机不丢记录史：换机前 10 分钟清单+迁移方法+事后核验，对位「数据锁死/换机即失忆」。 | ♦ |
| 11 | `partner-gestational-diabetes-support` | Your Partner Has Gestational Diabetes: How to Help the Logging System Without Becoming the Food Police | gestational diabetes partner support | 给「第二只耳朵」的分工指南：伴侣管预约/提醒/餐食备注，明确反 food-policing 立场。 | |
| 12 | `gestational-diabetes-log-burnout` | GDM Logging Burnout: the Minimum Viable Log for the Weeks You Can't Keep Up | gestational diabetes burnout | 记录疲劳周的最小可行日志：保住医嘱要求的检查、砍掉自加项、断了补记不重启；对位「被 App 逼到内疚」的情绪搜索。 | ♦ |
| 13 | `gestational-diabetes-meal-ideas` | Gestational Diabetes Meal Ideas: Why Your Log — Not the Internet — Should Shortlist Your Next Meal | gestational diabetes meal ideas | 不给饮食处方：用自己的日志+读数筛出「对你已验证有效」的餐食候选，判断权交营养师的记录实验法。 | |
| 14 | `why-did-i-get-gestational-diabetes` | Why Did I Get Gestational Diabetes? Turning the Blame Question Into Questions for Your Care Team | gestational diabetes causes | 把自责式搜索转成给团队的问题清单：坦诚说清「为什么」能讲到哪，反焦虑立场。 | |
| 15 | `gestational-diabetes-vs-type-2-diabetes` | Gestational Diabetes vs Type 2 Diabetes: the Words on Your Chart, and Why Postpartum Testing Goes in Your Archive | gestational diabetes vs type 2 diabetes | 只做命名与记录口径的区分：两种称呼在病历上各是什么、产后复测为何进同一档案，不回答「会不会变成 2 型」。 | |
| 16 | `gestational-diabetes-second-pregnancy` | Gestational Diabetes in a Second Pregnancy: Bringing Last Time's Log to Your First Appointment | gestational diabetes second pregnancy | 二胎 GDM 搜索者：复发风险只引原文并标注为人群级；交付「上次档案→这次首诊输入」的复用法。 | |
| 17 | `checking-blood-sugar-at-work` | Checking Blood Sugar at Work: Logging Around Shifts, Meetings, and Coworkers' Questions | gestational diabetes at work | 上班场景记录法：倒班/会议间隙怎么测、迟测怎么诚实补记、向同事披露多少由你决定。 | |
| 18 | `gestational-diabetes-dietitian-appointment` | Your First GDM Dietitian Appointment: What to Bring From Your Food Log, and What to Write Down After | gestational diabetes dietitian | 首次见营养师要带什么：可用的饮食日志、排序好的问题清单、真实作息；吃法本身归营养师。 | ◇ |
| 19 | `telehealth-gestational-diabetes-appointment` | Telehealth Visits With Gestational Diabetes: How to Show Your Numbers When There's No Paper to Hand Over | telehealth gestational diabetes | 视频产检没纸可递：提前经门户发什么、屏幕共享报告哪一页、通话中记下医生的调整。 | |
| 20 | `message-doctor-blood-sugar-readings` | Messaging Your Doctor About Blood Sugar Readings: the Portal Message That Actually Gets a Reply | send blood sugar readings to doctor | 门户留言有回音的三段式结构：时段范围+模式描述+一个具体问题，附异步回复的合理预期。 | |
| 21 | `gestational-diabetes-medical-records` | Your GDM Paper Trail: How to Get Copies of Your Own Pregnancy Records, and Keep Them With Your Log | gestational diabetes medical records | 两轨档案法：临床记录（OGTT/就诊记录/住院图表）如何索取副本，与自建血糖日志并档保存。 | |
| 22 | `diet-controlled-gestational-diabetes` | Diet-Controlled Gestational Diabetes: What the Phrase on Your Chart Means, and What It Doesn't | diet controlled gestational diabetes | 「diet controlled」是分期用语不是成绩单：意味着什么/不意味着什么，日志如何支撑标签随孕周更新。 | ⭐ |
| 23 | `gestational-diabetes-appointment-schedule` | Gestational Diabetes Appointment Schedules: the Common Shapes, Your Team's Version, and Tracking Yours | gestational diabetes appointment schedule | 没有唯一的 GDM 产检时间表，只有常见形态：常规节奏+GDM 增量，教你记录自己团队的版本。 | ◇ |
| 24 | `mfm-referral-gestational-diabetes` | Referred to MFM for Gestational Diabetes: What the Referral Process Looks Like, and What to Bring From Your Log | mfm referral pregnancy | 收到 MFM 转诊单的流程陪跑：怎么约、首诊什么样、带什么日志；转诊的医学含义一律归护理团队。 | |

## 2. ⭐ 诊断后第一周 · 关键引流页

第一周搜索者的状态：刚拿到诊断+转诊包+一台血糖仪，问题密集而具体。承接这一周的四篇主页面（判断依据随附）：

- **#1 `how-often-to-check…`** — A1（旧稿 `just-diagnosed-gestational-diabetes`）第一周问题清单第 2 问就是 *"How many checks per day, and at exactly which times?"*（A1 文末问题列表，本次通读核实）；本文正是该问题的正页，且出链直连 A1 与 A5 targets。
- **#6 `how-to-log…`** — A1 周一弧线 *"Days 2–3: set up your logging routine"* 的执行落地页（A1 H2 结构，本次核实）；新稿自标 `article_id: B1`，与旧 B 系「记录方法」词族同轴。
- **#22 `diet-controlled…`** — 确诊谈话里最常被口头告知的短语，回家第一件事就是搜它；本文「不是成绩评级」的反焦虑口径承接第一周情绪（红线 4 的样板页）。
- **#7 `gestational-diabetes-care-team`** — meta_description 原文 *"Handed four referrals at once?"*：一次拿到一叠转诊单就是第一周事件，谁看日志/有事找谁在这篇。

支撑页（◇）：**#4 second-trimester**（确诊当刻的主叙事，把人接进记录习惯）、**#18 dietitian-appointment**（首次营养师约谈通常落在确诊后头两周）、**#23 appointment-schedule**（第一周必问「接下来要见多少人」，出链直连 A1）。

**汇流点**：本簇 7 篇中有 5 篇直链 A1 `just-diagnosed-gestational-diabetes`（how-often、second-trimester、meal-ideas、appointment-schedule + partner/second-pregnancy 等场外页），A1 是全站第一周总枢纽——但 A1 目前 0 条回链指向本簇（§5#1）。

## 3. ♦ 差评对位 · 关键引流页

对位对象：竞品 GDM 记录类 App 的差评主题（广告轰炸、导出收费、数据锁定、停订后历史只读、提醒逼人内疚）。搜索者正处于「比价中/被坑过」状态。四篇主页面：

- **#8 `free-gestational-diabetes-app`（簇枢纽）** — 全文三成本结构 *Cost #1: your attention / Cost #2: your data / Cost #3: your export* 就是差评分类学；正文给出可执行探针（*"read the 20 most recent store reviews and search for 'ads'"*，本次全文通读核实）；收尾落到本司永久免费层（logging / viewing / CSV export free forever），与红线 5 口径一致。
- **#9 `how-to-print-blood-sugar-log`** — H2 *"Route 2: Screenshots, when there's no export"* 直接对位「没有导出功能」差评；target_keyword 打的是 `export blood sugar log`（导出意图词，不是 slug 字面）。
- **#10 `transfer-blood-sugar-log-new-phone`** — 对位数据锁定：换机/停订后历史丢失或只读，本篇给换机前 10 分钟清单+事后核验。
- **#12 `gestational-diabetes-log-burnout`** — 对位注意力税：*"the minimum viable log"* 给被提醒轰炸的用户一个不内疚的台阶。

**旧稿盟友**：A6 `gestational-diabetes-app-privacy`（获 free-app / transfer / at-work 三条新链，隐私深读）与 C4 `best-gestational-diabetes-app`（free-app 链过去的 9 点选型清单）。
**邻接缺口**：C3 `paper-log-vs-app-gestational-diabetes` 目前 0 入链——free-app 的 FAQ 问答 *"Can I just use a paper log instead of an app?"* 是天然回链位，建议发布时补上（§5#1）。

## 4. 互链关系图

### 4.1 簇总览

```
【簇 1 · 诊断后第一周】0–7 天高频搜索 → 记录系统搭建
  just diagnosed gestational diabetes ──► A1 just-diagnosed（旧·总枢纽）
  how often to check blood sugar ───────► ⭐how-often ──► A1 / A5 / B1旧
  how to log blood sugar readings ──────► ⭐how-to-log ──► B2旧 / C5 / B1旧 / 首页
  diet controlled gestational diabetes ─► ⭐diet-controlled ──► A5 / C1
  gestational diabetes care team ───────► ⭐care-team ──► C1 / C2 / 首页
  ◇支撑：second-trimester / dietitian / appointment-schedule
  簇出口：A5 targets · C1 report · C2 questions → 首页 CTA

【簇 2 · 差评对位】比价中/被坑过的搜索者 → 永久免费层
  free gestational diabetes app ───► ♦free-app（簇枢纽）──► A6 privacy / C4 best-app
  export blood sugar log / print ───► ♦how-to-print ──► C1 / B3 printable
  transfer log to new phone ────────► ♦transfer ──► A6 / C7 archive
  gestational diabetes burnout ─────► ♦burnout ──► B2旧 / B3 printable
  簇出口：A6 深读 · C4 清单 → BumpSugar 免费层 CTA
  ⚠ 邻接缺口：C3 paper-log-vs-app（0 入链），free-app 的纸笔 FAQ 是天然回链位

【贯穿主线】孕期阶段叙事（first → second → third trimester，唯一稿内互链
  appointment-schedule → third-trimester 即挂在这条线上）
  + 沟通/记录场景（work、telehealth、message-doctor、medical-records、mfm、
  second-pregnancy、meal-ideas、why-did-i-get、vs-type-2、partner、blood-sugar-levels）
```

### 4.2 逐篇出链表（仅站内链接；65 条新→旧 + 1 条稿内，Python 全量解析核实）

| 新稿 | 出链（→ 旧稿 slug，括号内为旧稿 article_id） |
|---|---|
| how-often-to-check… | blood-sugar-targets (A5)；just-diagnosed (A1)；when-to-check-after-eating (B1) |
| blood-sugar-levels-in-pregnancy | after-birth-gdm-log-archive (C7)；failed-glucose-test (A2)；blood-sugar-targets (A5)；glucose-tolerance-test (A3)；mg-dl-vs-mmol-l (C5)；when-to-check-after-eating (B1) |
| first-trimester | just-diagnosed (A1)；what-is-gestational-diabetes (A4) |
| second-trimester | after-birth-archive (C7)；failed-glucose-test (A2)；blood-sugar-targets (A5)；food-log (B6)；glucose-tolerance-test (A3)；just-diagnosed (A1)；另有资产 `/blood-sugar-log.pdf`（**缺失**，见 §5#4） |
| third-trimester | log-book-report (C1)；insulin-log (B7) |
| how-to-log… | 首页 `/`；blood-sugar-log-pregnancy (B2)；mg-dl-vs-mmol-l (C5)；when-to-check-after-eating (B1) |
| care-team | 首页 `/`；log-book-report (C1)；questions-to-ask-doctor (C2) |
| free-app… | best-gestational-diabetes-app (C4)；app-privacy (A6) |
| how-to-print… | log-book-report (C1)；printable-blood-sugar-log (B3) |
| transfer… | after-birth-archive (C7)；app-privacy (A6) |
| partner… | blood-sugar-targets (A5)；food-log (B6)；questions-to-ask-doctor (C2)；just-diagnosed (A1) |
| log-burnout | blood-sugar-log-pregnancy (B2)；printable-blood-sugar-log (B3) |
| meal-ideas | 首页 `/`；food-log (B6)；just-diagnosed (A1) |
| why-did-i-get… | questions-to-ask-doctor (C2)；what-is-gestational-diabetes (A4) |
| vs-type-2… | after-birth-archive (C7)；failed-glucose-test (A2)；blood-sugar-targets (A5)；what-is-gestational-diabetes (A4) |
| second-pregnancy | after-birth-archive (C7)；blood-sugar-targets (A5)；just-diagnosed (A1) |
| checking-at-work | cgm-pregnancy (C6)；app-privacy (A6)；when-to-check-after-eating (B1) |
| dietitian… | food-log (B6)；questions-to-ask-doctor (C2) |
| telehealth… | `/#waitlist`；blood-sugar-log-pregnancy (B2)；log-book-report (C1) |
| message-doctor… | blood-sugar-log-pregnancy (B2)；log-book-report (C1)；questions-to-ask-doctor (C2) |
| medical-records | 首页 `/`；after-birth-archive (C7)；glucose-tolerance-test (A3) |
| diet-controlled… | blood-sugar-targets (A5)；log-book-report (C1) |
| appointment-schedule | **gestational-diabetes-third-trimester（本轮唯一稿内互链）**；questions-to-ask-doctor (C2)；just-diagnosed (A1) |
| mfm… | log-book-report (C1)；questions-to-ask-doctor (C2) |

### 4.3 旧枢纽入链度（被新 24 篇链入，按入链数排序）

| 入链 | 旧枢纽（slug / id） |
|---|---|
| 7 | blood-sugar-targets (A5)；log-book-report (C1)；questions-to-ask-doctor (C2)；just-diagnosed (A1) |
| 6 | after-birth-gdm-log-archive (C7) |
| 4 | blood-sugar-log-pregnancy (B2)；gestational-diabetes-food-log (B6)；when-to-check-blood-sugar-after-eating-pregnancy (B1) |
| 3 | failed-glucose-test-pregnancy (A2)；app-privacy (A6)；glucose-tolerance-test-pregnancy (A3)；what-is-gestational-diabetes (A4) |
| 2 | printable-blood-sugar-log (B3)；mg-dl-vs-mmol-l (C5) |
| 1 | best-gestational-diabetes-app (C4)；cgm-pregnancy (C6)；insulin-log (B7) |
| **0** | **paper-log-vs-app (C3)；time-in-range (B5)；high-fasting-blood-sugar-reading (B4)** ← 孤儿，见 §5#1 |

## 5. 发布前 housekeeping（图上断点，全部本次实测）

1. **回流断点（最重要）**：旧 → 新回链 **0** 条；`index.html` 引用新 slug **0** 处。新簇目前只有出没有进，站内权重全靠新稿单方面输送。发布清单建议至少补：
   - A1 `Days 2–3: set up your logging routine` 节 → 回链 how-to-log 与 how-often；
   - C1 log-book-report → 回链 how-to-print / telehealth / message-doctor（三篇都链它）；
   - C4 best-app → 回链 free-app（窄口径版 vs 9 点清单版天然分工）；
   - A6 app-privacy → 回链 free-app / transfer / at-work；
   - C7 archive → 回链 transfer / medical-records / second-pregnancy / vs-type-2；
   - free-app FAQ 纸笔问答 → 回链 C3 paper-log-vs-app（顺带救活 0 入链孤儿）；
   - index.html 或未来文章列表页收录 24 篇。
2. **article_id 撞号**：新稿 how-to-log 自标 `article_id: B1`、how-often 自标 `article_id: B2`，与旧稿 when-to-check（`B1`）、blood-sugar-log-pregnancy（`B2`）撞号（frontmatter 逐字核实）；其余 22 篇新稿无 article_id。建议改批次前缀（如 D1/D2）或全面去 id 化，统一以 slug 为准。
3. **pillar 词表不统一**：24 篇出现 6 种取值（logging-and-tools ×7、doctor-communication ×8、pregnancy-basics ×2、reading-your-log ×1、"A — after diagnosis" ×2、"C — records, tools, and doctor communication" ×1），另有 3 篇无 pillar（first-trimester、partner-support、why-did-i-get）。发布前收敛成一套。
4. **缺失资产**：`/blood-sugar-log.pdf` 被 second-trimester 文内引用（`gestational-diabetes-second-trimester.md:79`），但 `bumpsite/` 下不存在该 PDF（全工作区 find 仅 research/ 下无关 PDF）。补资产，或把链接改指 printable-blood-sugar-log 文章。
5. **URL 形态**：内链尾斜杠两种写法并存（如 `/articles/app-privacy` 与 `/articles/app-privacy/` 都在用，本次解析中 65 条边两种形态都有）；且旧稿文件名带 `c7-` 等前缀而 URL slug 不带。发布层需确认路由等价，否则批量统一。
6. **noindex/draft 翻转**：24 篇均 `status: draft` + `noindex: true`，上线动作包含批量翻转 + GSC 提交（README 的 SEO 待办同此口径）。
7. **本文件处置**：含引流与差评对位策略，属内部文档，部署时从发布目录排除（或移入仓库非发布目录）。

## 6. 医疗红线合规状态（登记，不重复核验）

前序两轮编辑已逐篇核验（2026-10-30，见编辑结果一/二）：33 个去重引用 URL 全部 WebFetch 实测可达且引文逐字对上（CDC / NIH-NIDDK / NIH-NLM-MedlinePlus / ADA / ACOG，白名单内）；每篇显著位置免责、FAQ 3–4 问、文末权威链接列表与「永久免费层（记录/查看/CSV 导出，不锁数据）」自然导流齐备；无诊断/剂量/目标值自定，无绝对化医疗表述；两处已修订（#4 Sources 移至文末、#6 删除一条验证不到的引文短语）。本索引仅覆盖结构、SEO 与引流层，未重复医疗合规检查。
