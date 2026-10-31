---
title: "mg/dL vs mmol/L: Reading Your Pregnancy Glucose Log in Either Unit"
slug: mg-dl-vs-mmol-l
article_id: C5
pillar: doctor-communication
target_keyword: "mg/dl to mmol/l"
secondary_keywords: ["mg/dl vs mmol/l pregnancy", "blood glucose unit conversion", "mmol/l to mg/dl glucose"]
meta_description: "How to convert mg/dL to mmol/L (and back) for a pregnancy glucose log, why the two units appear side by side, and how to spot a mixed-unit log before it confuses anyone."
status: draft
updated: 2026-10-29
plan_ref: "content-plan.md §3 C5 — 组合词无实测锚（GSC 验证优先）；换算常数来源=NIH PubChem 葡萄糖分子量 180.16（本会话经 REST API 实测核对）；示例数值=NIDDK 官方页（本会话核对）"
noindex: true
---

# mg/dL vs mmol/L: reading your pregnancy glucose log in either unit

> **DISCLAIMER:** This guide is general information, not medical advice, diagnosis, or treatment. BumpSugar is a logging and reminder tool, not a medical device. It never recommends medications or insulin doses, and nothing here should be taken as advice to start, stop, or change any medication. Target ranges and check schedules belong to you and your care team — always follow your doctor. Reminders use standard local notifications and may be delayed or suppressed by Focus or notification permissions — do not rely on BumpSugar as your only reminder to test. If a reading or symptom concerns you, contact your healthcare provider. This article is educational only — for questions about your own care, consult your OB/GYN, endocrinologist, or another member of your care team.

Sooner or later it happens to almost everyone logging glucose in pregnancy: the meter says one thing, a lab report says another, a forum post from overseas says a third — and two of the three are in a unit you don't use. mg/dL and mmol/L measure exactly the same glucose; they're just two ways of writing it. Here's how to convert between them, where the mismatch actually bites, and how to keep one log readable in either unit.

## The two units, in one paragraph

- **mg/dL** — milligrams per deciliter. One tenth of a liter of blood, and how many milligrams of glucose are in it. This is the unit you'll most often see on US lab reports, meters, and US apps.
- **mmol/L** — millimoles per liter. How many thousandths of a mole of glucose are in a liter. Much of the rest of the world writes glucose this way, and you'll meet it in international guidelines, research summaries, and forums.

The only fact you need to move between them is glucose's molecular weight, which the [NIH's PubChem database](https://pubchem.ncbi.nlm.nih.gov/compound/5793) lists as **180.16 g/mol**. Everything below is arithmetic from that one number.

## The conversion (and where it comes from)

One millimole of glucose weighs 180.16 milligrams. A liter is ten deciliters, so one **mmol/L** of glucose works out to **18.0 mg/dL**:

- **mg/dL → mmol/L: divide by 18.**
- **mmol/L → mg/dL: multiply by 18.**

Worked examples, using the example targets for gestational diabetes that the [NIDDK](https://www.niddk.nih.gov/health-information/diabetes/overview/what-is-diabetes/gestational/management-treatment) lists on its page (before meals/at bedtime "95 or less", "1 hour after eating: 140 or less", "2 hours after eating: 120 or less"):

| mg/dL | ÷ 18 | mmol/L |
|---|---|---|
| 95 | 95 ÷ 18 | ≈ 5.3 |
| 140 | 140 ÷ 18 | ≈ 7.8 |
| 120 | 120 ÷ 18 | ≈ 6.7 |

One caution that belongs to your care team, not to this page: those NIDDK numbers are *examples on a government information page*, and the same page ends with "Ask your doctor what targets are right for you." Your own targets are whatever your care team set — converting them between units changes nothing about what they mean.

## Where the mismatch actually bites

- **Meter vs. lab vs. app.** A meter set to mmol/L next to a US lab report in mg/dL will look off by a factor of 18 — and if you transcribe one into the other's column, your log quietly becomes two logs.
- **Forum math.** International posts arrive in mmol/L. Before comparing anyone's "5.3" to your "95", convert one side. (5.3 × 18 ≈ 95.)
- **Entry errors.** Typing a mmol/L value into an mg/dL field (or the reverse) is the classic way a log gets a wild-looking entry. It's also the most fixable: the number itself wasn't wrong, just the unit label — so a good tool should let you edit it.
- **Telling them apart by size.** mmol/L readings live in the single digits to low teens; mg/dL readings are two to three digits. If a fasting check shows up as "9.5" on a log otherwise full of nineties, suspect the unit before anything else — then just verify which unit the device was set to.

## Keeping one log readable in either unit

- **Pick one unit for the whole pregnancy and stick to it** in your log, even if other documents around you disagree.
- **Set the unit once, at the tool level.** In BumpSugar, mg/dL and mmol/L is a single global setting ([bumpsugar.pages.dev](/)) — every entry field, target, and summary switches together, so mixed-unit entries can't accumulate silently.
- **Record your targets in your own unit, per check type**, exactly as your care team gave them. If they hand you a printout in the other unit, convert once, write down both, and move on.
- **Keep lab reports in their original units**, stored with the date — don't transcribe lab values into your log from memory. If a reading belongs in your log, enter it as the lab reported it and note the source.
- **At appointments, say the unit out loud once.** "My log is in mg/dL" takes two seconds and prevents the most confusing kind of thirty-second misunderstanding.

## Toolbox

**BumpSugar** ([bumpsugar.pages.dev](/)) supports **mg/dL and mmol/L as a global setting** — one switch, applied everywhere: entry, targets, summaries, exports. Logging is free forever, with free CSV export (values export in your chosen unit, clearly labeled) and free JSON backup; there are no ads, no account, and data never leaves your device. The subscription ($19.99 / 6 months, 14-day full-feature trial) adds the clinic-ready PDF report and week/month charts. A free printable log PDF (US Letter and A4) is on the site.

## Questions to bring to your care team

1. "My meter and your patient portal may use different units — which one do you want my log in?"
2. "When my lab results come back, can they be filed in the same unit as my meter, or should I bring both?"
3. "The example targets I see online are in mg/dL — can we write down my targets together, in my log's unit, before I go?"

Two units, one glucose, one conversation: as long as everyone in the room knows which unit the log is in, the conversion is the easy part — it's just eighteen.
