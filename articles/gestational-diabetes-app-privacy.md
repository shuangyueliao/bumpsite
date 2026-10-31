---
title: "Gestational Diabetes Apps and Your Data: Who Sees What"
slug: gestational-diabetes-app-privacy
article_id: A6
pillar: logging-methods
target_keyword: "gestational diabetes app privacy"
secondary_keywords: ["gestational diabetes app data privacy", "pregnancy app privacy", "health data privacy pregnancy app", "GDM app no ads no account"]
meta_description: "A privacy checklist for gestational diabetes apps: the three data architectures (on-device, account + cloud, ads + analytics), what one GDM app's own policy says, and the questions to ask before you install."
status: draft
updated: 2026-10-29
plan_ref: "content-plan.md §3 A6 — 三类数据架构用可核验结构事实；导出权/删除权/无账号检查清单；R6/R8：只引一手隐私文件"
noindex: true
---

# Gestational Diabetes Apps and Your Data: Who Sees What

> **DISCLAIMER:** This guide is general information, not medical advice, diagnosis, or treatment. BumpSugar is a logging and reminder tool, not a medical device. It never recommends medications or insulin doses, and nothing here should be taken as advice to start, stop, or change any medication. Target ranges and check schedules belong to you and your care team — always follow your doctor. Reminders use standard local notifications and may be delayed or suppressed by Focus or notification permissions — do not rely on BumpSugar as your only reminder to test. If a reading or symptom concerns you, contact your healthcare provider. This article is educational only — for questions about your own care, consult your OB/GYN, endocrinologist, or another member of your care team.

Your glucose log will contain some of the most personal data you generate this year: readings several times a day, meals, sleep notes, medications — all stamped against a pregnancy timeline. If you keep it in an app, which ACOG explicitly blesses ("blood sugar logs also can be kept online, stored in phone apps, and emailed to your ob-gyn" — [ACOG, Gestational Diabetes FAQ](https://www.acog.org/womens-health/faqs/gestational-diabetes)), it's worth ten minutes to understand where the data actually goes.

This page explains the three structures behind virtually every health app, quotes one GDM app's own privacy policy as a concrete example, and gives you a checklist to run on any app before you trust it with a pregnancy's worth of readings.

## The three data architectures

**1. On-device only.** The app stores everything on your phone. No servers hold your log, nothing transmits, the developer has no copy — nothing "out there" to breach, subpoena, or sell. The trade-off: lose the phone with no backup and the log is gone; any backup is the one your operating system already manages (more on iCloud below).

**2. Account + cloud sync.** You create an account; entries sync to the company's servers. That buys convenience — switching phones, a tablet login — and costs a permanent question: your most sensitive health data now lives on someone else's computers, tied to your identity, under their retention policy and breach surface. If an app demands an account before the first reading, this is the structure, whatever the marketing says.

**3. Ads + analytics SDKs.** The app is free because advertising pays for it. Ad and analytics toolkits are third-party code inside the app, and their business is collecting signals: device identifiers, IP address, usage patterns. Combined with a health topic, that signal stream is valuable — and it flows to companies you never signed anything with. The privacy policy is where this gets admitted, in the vendor's own words.

One app can be a combination — account + cloud + ads is a common package.

## What one GDM app's own privacy policy says

Not an accusation — the vendor being transparent about its own architecture. The privacy policy of **Gestational Diabetes Tracker**, an ad-supported GDM app on the US App Store, last updated March 2026, states — quoted verbatim (archived copy captured October 28, 2026; check the developer's site or the App Store listing for the current version):

> "The app uses Google Analytics to collect usage data such as app interactions, device information, and diagnostics."
>
> "The app may display ads using Google AdMob. These services may collect data such as device identifiers, IP address, and app interactions, and may share this data with third parties for analytics and advertising purposes, in accordance with their own privacy policies."

The same policy states that health data entered into the app "is stored locally on the user's device only. The developer does not collect, store, or have access to this data" — which is exactly the mixed picture to understand: *your readings* may stay on-device, while *usage and device signals* flow to Google's toolkits for analytics and advertising. Both sentences are true at once, and the distinction is the whole game.

## How to read any app's privacy story in two minutes

- **The App Store "App Privacy" section.** Every listing carries a self-reported privacy "nutrition label": data collected, and whether it's linked to your identity. It's the developer's own writing, under Apple's category definitions — and materially false claims carry enforcement consequences.
- **The developer's privacy policy** — linked from the listing. Search it for the words "advertis", "analytics", "third part", "share". What you find in five minutes is usually the whole story.
- **The permission prompts.** An on-device log app has no honest reason to request contacts, precise location, or your photo library beyond letting you attach a photo.

## The checklist to run before you install

1. **Does it demand an account before the first log entry?** If yes, architecture 2 — your log lives on their servers.
2. **Does the privacy label or policy mention ads or analytics SDKs?** If yes, architecture 3 — usage signals leave the device.
3. **Can you export everything, free?** Your data, in CSV or similar, whenever you want, without paying a ransom. A log you can't leave with is a log you don't own.
4. **Can you delete everything — actually delete?** Ask what happens server-side when you delete your account.
5. **Is the price visible before you've invested weeks of data?** Pricing hidden behind a paywall you hit after your whole pregnancy is already in the app is a retention tactic, not a pricing model.
6. **What happens to history if you stop paying?** A subscription should add features, never hold your own past hostage.
7. **Where does the backup go, and who holds the keys?** Even "no cloud" apps live with the iCloud or system backup you may already use — that's a deliberate, inspectable trade-off, not a silent one.

## BumpSugar's answers, so you can compare

We built BumpSugar ([bumpsugar.pages.dev](/)) as architecture 1, and we'd rather show the receipts than the adjectives: **no ads and no ad SDKs**; **no account** — the app works fully on first launch with nothing to register; **data never leaves your device** (we don't run servers; if you use iCloud backup, that's between you and Apple); **CSV export and full JSON backup are free forever**, so the exit door is always open; your complete history stays readable whether or not you subscribe. Logging is free forever; a 14-day full-feature trial leads into **$19.99 / 6 months** for the clinic-ready PDF report and visit agenda. Requires iOS 17 or later. This page is the standard we hold ourselves to — run the same checklist on us, and on anyone.

## Two sets of questions

**For any app's developer:** "Is an account required? What exactly leaves the device? Can I export everything for free? What survives if I stop paying?"

**For your care team:** privacy extends past the app. ACOG notes logs "can be emailed to your ob-gyn" ([ACOG](https://www.acog.org/womens-health/faqs/gestational-diabetes)) — worth asking what their office accepts and how they handle it, alongside the [rest of your appointment questions](/articles/gestational-diabetes-questions-to-ask-doctor/).

If BumpSugar's trade-offs sound right to you, the [waitlist](/#waitlist) is open — and whichever tool you choose, may it be one you could explain to your OB in detail.
