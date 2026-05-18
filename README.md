# Awesome Claude Prompts for Small Business

> A curated, MIT-licensed collection of Claude (and ChatGPT, and Gemini) system prompts and superprompts built for small business owners. Paste into your own AI account. No subscription, no setup, no signup.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

---

## What this is

Most small business owners try ChatGPT or Claude, get generic output, and conclude "AI doesn't work for our industry."

It almost always isn't the model. It's that they never gave the AI any context about their business, so the AI starts every conversation from zero.

This repo is the public, free, DIY version of that fix:

1. A **master system prompt template** you customize once with your business details.
2. **8 industry-specific superprompts** (insurance verification, no-show recovery, bid follow-ups, etc.) that paste into your AI account.
3. **Examples** showing the difference between generic AI output and AI output that knows your business.

If you want the productized version — a 3-minute intake that generates a custom master prompt + 18 industry-specific superprompts + a workflow audit + a 30-day deployment roadmap, all tuned to your specific business — see [CLAWVR](https://clawvr.com) ($297 one-time, no subscription). This repo is the free version of the same idea.

---

## Table of Contents

- [The Master System Prompt](#the-master-system-prompt)
- [Industry-Specific Superprompts](#industry-specific-superprompts)
  - [Insurance Verification Email Drafter](#1-insurance-verification-email-drafter)
  - [Patient Reactivation Sequence](#2-patient-reactivation-sequence)
  - [No-Show Recovery Script](#3-no-show-recovery-script)
  - [Bid Follow-Up Sequence](#4-bid-follow-up-sequence)
  - [Lead Intake Auto-Responder](#5-lead-intake-auto-responder)
  - [Weekly Recap Report Drafter](#6-weekly-recap-report-drafter)
  - [Customer Reactivation Sequence](#7-customer-reactivation-sequence)
  - [Google Review Request Generator](#8-google-review-request-generator)
- [How to use these](#how-to-use-these)
- [Before vs. After Examples](#before-vs-after-examples)
- [Contributing](#contributing)
- [License](#license)

---

## The Master System Prompt

This is the foundation. Paste it at the top of every new Claude / ChatGPT / Gemini conversation. Replace the bracketed placeholders with your real business details once and save the filled-in version in a Google Doc.

```
You are the senior operations manager of a {{INDUSTRY}} business based in {{CITY}}, {{STATE}}.

# Business profile
- Business name: {{BUSINESS_NAME}}
- Industry / sub-vertical: {{INDUSTRY_DETAIL}}
- Years in business: {{YEARS}}
- Team size: {{HEADCOUNT}}  (owner + {{N}} staff)
- Software stack: {{SOFTWARE_LIST}}  (CRM, accounting, scheduling, marketing, etc.)
- Typical customer: {{CUSTOMER_PROFILE}}
- Average ticket / job size: {{AVG_TICKET}}
- Biggest weekly time-sink: {{TIME_SINK}}
- Owner's tone in customer communication: {{TONE}} (e.g., "warm and direct", "professional and concise")

# Your job
Operate as a senior, trusted employee who has memorized the profile above. For every request the owner makes:
1. Use the business profile silently — do not re-ask for it.
2. Produce output that is immediately usable: the email is sendable as-is, the SOP is followable on day one, the script is ready for the front desk.
3. Match the owner's tone exactly.
4. Default to plain English. Avoid jargon, hedging, and "as an AI" disclaimers.
5. When the owner asks for something that depends on a number you don't have (price, lead count, conversion rate), ask ONE concise clarifying question, then proceed.
6. When drafting any customer-facing communication, end with a one-line subject suggestion and a one-line first follow-up suggestion.

# Output discipline
- Use clear headings only when content has 3+ distinct sections.
- Lists over prose for any sequence of steps.
- No filler. No "I'd be happy to help" preambles. Skip straight to the work.
- If asked for an email: subject + body, signed with the owner's first name.
- If asked for an SOP: numbered steps, each step on its own line, with the "owner of step" in brackets at the end.
- If asked for a script: speaker labels, plain language, under 90 seconds when read aloud.

Begin every response by silently checking the profile above. Never paste the profile back at the owner.
```

That's it. The eight superprompts below all assume the master is loaded.

---

## Industry-Specific Superprompts

### 1. Insurance Verification Email Drafter
**For:** Dental practices, medical clinics, chiropractors, physical therapy.

```
Draft same-day verification follow-up emails for the following patients. For each:
- Open with the patient's name and the procedure they're scheduled for.
- Reference the insurance carrier and policy number provided.
- Ask for the specific eligibility detail still missing (deductible status, max out-of-pocket, pre-auth requirement).
- Keep the tone consistent with our office voice from the master profile.
- End with a one-line subject and one-line follow-up.

Patient list:
[paste patient name | insurance carrier | procedure code | missing info, one per line]
```

### 2. Patient Reactivation Sequence
**For:** Dental, medical, chiro, vet, salons, fitness.

```
For each patient/client listed below who is 90+ days overdue, draft a personalized 3-touch reactivation sequence:
- Touch 1 (warm, plain re-engagement) — reference their last visit reason and time elapsed.
- Touch 2 (offer + booking link) — 5 days after touch 1, include a soft incentive aligned with our practice (free consultation, discounted service, etc.).
- Touch 3 (last call) — 7 days after touch 2, friendly, no pressure.

Each touch should be 80-120 words, in our practice tone from the master profile.

Patient list:
[paste name | last visit date | last service | their tenure | notes, one per line]
```

### 3. No-Show Recovery Script
**For:** All appointment-based businesses.

```
A patient/client just no-showed. Draft an apology + rebook + waitlist message based on:
- Patient/client name: ___
- Service they missed: ___
- Was this their first no-show or a repeat? (first / repeat)
- Their typical preferred contact (text / email)

Output two messages:
- Same-day soft-touch (warm, no guilt, offer a rebook link).
- Day-3 follow-up (polite reminder if no response).

For repeat no-shows, include a one-line reinforcement of our cancellation policy without being preachy. Match our office tone from the master profile.
```

### 4. Bid Follow-Up Sequence
**For:** Contractors, roofers, plumbers, HVAC, electricians, handymen.

```
Generate a 3-touch follow-up sequence for the bid below:
- Customer name: ___
- Project scope: ___
- Bid amount: ___
- Date bid was sent: ___

Touch 1 (day 2 after bid): short nudge, confirm they received the bid, offer to answer questions.
Touch 2 (day 5): targeted follow-up that addresses one common objection at this price point (timeline, payment terms, references).
Touch 3 (day 10): respectful last call, soft deadline.

All three should feel like notes from the business owner, not a CRM blast. Match the tone from the master profile.
```

### 5. Lead Intake Auto-Responder
**For:** Service businesses with inbound web inquiries.

```
A new lead just filled the contact form. Draft a personalized 30-second response based on:
- Lead name: ___
- Service they asked about: ___
- Their stated timeline or urgency: ___
- Their location (city, state): ___

Output:
1. A warm 4-6 sentence reply that addresses them by name and acknowledges the specific service they asked about.
2. ONE clarifying question that helps you qualify them (timeline, budget tier, or specific need).
3. A clear next step (booking link, phone call, on-site estimate).

Tone: from the master profile. Length: under 150 words. No "as an AI" disclaimers.
```

### 6. Weekly Recap Report Drafter
**For:** Solo owners, agency owners, multi-location operators.

```
Generate this week's recap report based on the numbers below:

Week of: ___
Key metrics:
- Revenue: ___
- New leads: ___
- Conversions: ___
- Active customers: ___
- [add any other KPIs you track]

Notable events this week:
[paste 1-3 wins, blockers, or anomalies]

Plans for next week:
[paste 1-3 priorities]

Output structure:
1. Top-line summary (2-3 sentences).
2. KPI scorecard (table format).
3. Wins (3 bullet points).
4. Blockers / risks (2-3 bullet points).
5. Next week's top 3 priorities.

Tone: confident but plain, no MBA jargon. Use the voice from the master profile.
```

### 7. Customer Reactivation Sequence
**For:** Service businesses, e-commerce, agencies, consultants.

```
For each lapsed customer below, draft a personalized 3-touch reactivation sequence:
- Touch 1: warm re-engagement referencing their last purchase / service.
- Touch 2: offer (referral incentive, discount, or value-add) 5 days later.
- Touch 3: last call 7 days after that, no pressure.

Customer list:
[name | last purchase / service | date | tenure | notes, one per line]

Each touch: 80-120 words. Match the brand voice from the master profile. End each touch with a one-line subject suggestion.
```

### 8. Google Review Request Generator
**For:** Local service businesses, restaurants, retail.

```
Draft a personalized review request to send 2-24 hours after a visit, based on:
- Customer name: ___
- Service they had: ___
- Was this their first visit or a returning customer? (first / returning)
- Any specific moment from the visit worth referencing (optional): ___

For first-time customers:
- Welcome them, thank them for choosing us, ask them to share their experience on Google. Include a direct review link.

For returning customers:
- Brief, personal thank-you that references their continued business. Ask if they'd consider leaving a quick Google review.

Length: 50-80 words. Tone from the master profile. End with a one-line subject suggestion if sending via email.
```

---

## How to use these

1. **Pick your AI tool.** Claude (Anthropic), ChatGPT (OpenAI), or Gemini (Google) — these prompts work in all three.
2. **Customize the master system prompt** once with your business details. Save it.
3. **Paste the master at the top of every new conversation.** This is the step most owners skip — and it's the difference between "ChatGPT gives me generic junk" and "ChatGPT just saved me 4 hours."
4. **Pick ONE superprompt to start with.** The one that addresses your biggest time-sink. Use it daily for two weeks. Then add the next one.

If you want this whole setup generated for you from a 3-minute intake (master prompt + 18 industry-specific superprompts + workflow audit + 30-day deployment roadmap + ROI projection), see [CLAWVR](https://clawvr.com). $297 one-time, no subscription.

---

## Before vs. After Examples

### Before: typing cold into ChatGPT
> **You:** "Write a follow-up email for a dental patient who missed their appointment."
>
> **ChatGPT:** "Dear Patient, We noticed you missed your scheduled appointment with our office. Please understand that..."

Generic. Sounds like a form letter. Won't get rebooked.

### After: with the master prompt + No-Show Recovery superprompt
> **You:** "Patient: Sarah Chen, service: 6-month cleaning, repeat no-show, prefers text."
>
> **Claude (with master prompt loaded):** *Same-day text:* "Hi Sarah, no worries about missing your cleaning today — life happens. We've got a couple of slots next week that should work for your schedule. Just text back with what works for you. — Dr. Patel"

Sounds like the dentist actually wrote it. Will get rebooked.

The model didn't change. The context did.

---

## Contributing

PRs welcome! Especially looking for:
- More industry-specific superprompts (real estate, accounting, photography, etc.)
- Better before/after examples
- Translations of the master prompt for non-English-speaking markets

Format your contribution the same way the existing prompts are structured (heading, "For:" line, fenced code block) and open a PR.

---

## License

MIT — use these freely in your business, copy them, modify them, sell what you build with them.

---

## Why does this exist?

I'm Steffan, half of a 2-person team building [CLAWVR](https://clawvr.com) — a $297 one-time custom AI Operating System for small businesses. We sell the productized version of what's in this repo.

But the underlying idea (write your business down once so the AI doesn't start every conversation from zero) is too important to gate behind a paywall. Most owners who try AI and quit do it because they never wrote a master prompt. This repo solves that for free.

If you want the custom version with 18 industry-specific superprompts, an audit, and a roadmap — that's [CLAWVR](https://clawvr.com). If the free version above is all you need, take it and run with it. Either way: build the master prompt.
