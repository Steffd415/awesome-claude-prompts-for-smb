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
2. **25 industry-specific superprompts** (insurance verification, no-show recovery, bid follow-ups, listing descriptions, lease renewals, hourly-invoice drafting, etc.) that paste into your AI account.
3. **Examples** showing the difference between generic AI output and AI output that knows your business.

If you want the productized version — a 3-minute intake that generates a custom master prompt + 18 industry-specific superprompts + a workflow audit + a 30-day deployment roadmap, all tuned to your specific business — see [CLAWVR](https://clawvr.com) ($297 one-time, no subscription). This repo is the free version of the same idea.

---

## Table of Contents

- [The Master System Prompt](#the-master-system-prompt)
- [Industry-Specific Superprompts](#industry-specific-superprompts)
  1. [Insurance Verification Email Drafter](#1-insurance-verification-email-drafter)
  2. [Patient Reactivation Sequence](#2-patient-reactivation-sequence)
  3. [No-Show Recovery Script](#3-no-show-recovery-script)
  4. [Bid Follow-Up Sequence](#4-bid-follow-up-sequence)
  5. [Lead Intake Auto-Responder](#5-lead-intake-auto-responder)
  6. [Weekly Recap Report Drafter](#6-weekly-recap-report-drafter)
  7. [Customer Reactivation Sequence](#7-customer-reactivation-sequence)
  8. [Google Review Request Generator](#8-google-review-request-generator)
  9. [Real Estate Listing Description Generator](#9-real-estate-listing-description-generator)
  10. [Open-House Follow-Up Sequence](#10-open-house-follow-up-sequence)
  11. [Accounting Client Onboarding Email Pack](#11-accounting-client-onboarding-email-pack)
  12. [Tax-Deadline Reminder Drip](#12-tax-deadline-reminder-drip)
  13. [Legal Intake Triage Memo](#13-legal-intake-triage-memo)
  14. [Salon Color-Correction Consultation Script](#14-salon-color-correction-consultation-script)
  15. [Fitness Trial-to-Member Conversion Sequence](#15-fitness-trial-to-member-conversion-sequence)
  16. [Veterinary Post-Visit Care Summary](#16-veterinary-post-visit-care-summary)
  17. [Restaurant Negative-Review Response Drafter](#17-restaurant-negative-review-response-drafter)
  18. [Photographer Gallery-Delivery Email + Upsell](#18-photographer-gallery-delivery-email--upsell)
  19. [Auto-Repair Estimate Walk-Through Script](#19-auto-repair-estimate-walk-through-script)
  20. [Pet-Service Boarding Confirmation + Upsell](#20-pet-service-boarding-confirmation--upsell)
  21. [Childcare Enrollment Inquiry Response](#21-childcare-enrollment-inquiry-response)
  22. [Insurance Broker Quote Walk-Through](#22-insurance-broker-quote-walk-through)
  23. [E-commerce Order Issue Resolution](#23-e-commerce-order-issue-resolution)
  24. [Coaching / Consultant Discovery-Call Follow-Up](#24-coaching--consultant-discovery-call-follow-up)
  25. [Agency Monthly Client Report Drafter](#25-agency-monthly-client-report-drafter)
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

That's it. The 25 superprompts below all assume the master is loaded.

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

### 9. Real Estate Listing Description Generator
**For:** Real estate agents, brokers, property managers.

```
Generate a listing description for the property below. The description should make a buyer pause when scrolling Zillow / Realtor.com and click for more.

Property:
- Address (city, state only — no street number): ___
- Bedrooms / bathrooms: ___
- Square footage: ___
- Lot size: ___
- Year built: ___
- 2-3 features the seller specifically wants highlighted: ___
- Target buyer (first-time, move-up, downsize, investor): ___
- List price: ___

Output:
1. Headline (under 12 words).
2. Opening paragraph (3-4 sentences) — the emotional hook tailored to the target buyer.
3. Feature paragraph (4-5 sentences) — concrete details, no hyperbole.
4. Neighborhood paragraph (2-3 sentences) — specific, no clichés like "great schools."
5. Call to action — schedule a showing.

Avoid: "must-see," "won't last," "diamond in the rough," any phrase MLS regulations flag as fair-housing risk. Use the voice from the master profile.
```

### 10. Open-House Follow-Up Sequence
**For:** Real estate agents.

```
Sunday open house just wrapped. Draft personalized 3-touch follow-ups for each attendee below.

For each attendee:
- Name (and partner's name if applicable): ___
- Engagement level (browsing / serious / asked specific questions): ___
- One concrete thing they mentioned about the home or their search: ___
- Preferred contact (text / email): ___

Touch 1 (within 24 hours): warm thank-you that references the specific thing they mentioned + a soft next step.
Touch 2 (day 4): share one nearby comparable that just hit MLS OR one improvement detail you didn't get to walk them through.
Touch 3 (day 10): respectful nudge with a clear ask ("Would a private showing this Saturday work?").

Each touch 60-100 words. Sign with the agent's first name. Match the voice from the master profile.
```

### 11. Accounting Client Onboarding Email Pack
**For:** Bookkeepers, CPAs, accountants, fractional CFOs.

```
A new monthly bookkeeping client just signed. Draft the onboarding email pack:

1. Welcome email (warm, sets expectations, links to the secure document portal).
2. Document checklist email (sent 24 hours later — bank statements, prior-year tax return, payroll provider login, etc.).
3. Kick-off call agenda email (sent 3 days before the first call — what we'll cover, what they should have ready).

Client context:
- Business name: ___
- Industry: ___
- Annual revenue tier (under $250K / $250K-1M / $1M+): ___
- What they specifically said is broken about their current bookkeeping: ___

Match the practice voice from the master profile. Plain English, no CPA jargon unless it's something they used first.
```

### 12. Tax-Deadline Reminder Drip
**For:** Accountants, bookkeepers, tax preparers.

```
Draft a 4-touch reminder drip for the upcoming tax deadline below.

Deadline name (e.g., "Q3 estimated taxes"): ___
Deadline date: ___
Who this is going to: (existing clients only / clients + warm leads): ___

Touch 1 (3 weeks out): heads-up, no panic — what they need to gather.
Touch 2 (10 days out): checklist email with a clear "send by [date]" instruction.
Touch 3 (3 days out): friendly nudge for stragglers.
Touch 4 (deadline day): "we filed yours" confirmation OR "haven't heard back, here's what happens next" for non-responders.

Tone from the master profile. Each touch under 150 words. Include a clear subject line for each.
```

### 13. Legal Intake Triage Memo
**For:** Solo and small-firm lawyers.

```
A potential new client just submitted an inquiry. Draft an internal triage memo + the initial response email.

Inquiry details:
- Practice area requested: ___
- Brief description of the matter (in their words): ___
- Their stated urgency: ___
- Jurisdiction: ___
- Any prior counsel mentioned: ___

Output two artifacts:
1. INTERNAL: a 5-line triage memo — practice area fit, conflict-check items to run, urgency level, suggested initial consult length, any red flags.
2. EXTERNAL: a 5-7 sentence reply to the prospect that confirms receipt, sets expectations on response time, and either (a) offers a consult slot if it's a clear fit or (b) asks one qualifying question if more info is needed.

Do NOT give legal advice in the external reply. Match the firm voice from the master profile. Plain English.
```

### 14. Salon Color-Correction Consultation Script
**For:** Hair salons, colorists, beauty studios.

```
A new client booked a color-correction consultation. Draft the in-chair consultation script the stylist will use.

Client context:
- What they've already tried at home or at another salon: ___
- The look they're trying to achieve (with reference image notes if any): ___
- Their hair history (chemical processes in the last 12 months): ___

Output:
1. Greeting + warm rapport opener (15-20 sec when read aloud).
2. Hair-history probe — 3 specific questions phrased non-judgmentally.
3. Honest expectation-setting paragraph — what's possible in one session vs. multiple, with a price range tied to our service menu.
4. Soft close — book the first session today vs. think it over (give a reason to book today that isn't pushy).

Tone: warm + expert + non-judgmental. Voice from the master profile.
```

### 15. Fitness Trial-to-Member Conversion Sequence
**For:** Gyms, CrossFit boxes, yoga studios, pilates, personal training.

```
A trial member's 7-day pass just expired. Draft a 4-touch conversion sequence.

Trial member context:
- Name: ___
- Number of classes attended during the trial: ___
- Their stated goal at signup: ___
- Coach who worked with them (if specific): ___
- Membership tier we'd recommend: ___

Touch 1 (day trial expires): warm thank-you + one specific win you observed in their week.
Touch 2 (day 3 after expiry): the recommended membership tier with a clear price + start-date.
Touch 3 (day 7): one-week extension offer ("come back this week on us — let's see if we can hit X").
Touch 4 (day 14): respectful last call.

60-90 words per touch. Sign from the coach if a specific coach was named, else from the owner. Match the gym voice from the master profile.
```

### 16. Veterinary Post-Visit Care Summary
**For:** Vet clinics, animal hospitals, mobile vets.

```
A pet just left after a sick visit. Draft the owner's take-home care summary.

Visit context:
- Pet name + species + breed: ___
- Reason for visit: ___
- Diagnosis (in plain language): ___
- Treatment given today: ___
- Medications dispensed (name + dose + duration): ___
- When to follow up (and red-flag symptoms that mean call us sooner): ___

Output a 1-page take-home summary that the front desk can hand the owner. Use plain English (5th grade reading level). Include a clear "call us if you see..." red-flag list. End with the clinic phone number and one-line reassurance.

Tone: warm + clinical-but-clear, the voice from the master profile.
```

### 17. Restaurant Negative-Review Response Drafter
**For:** Restaurants, cafes, bars, catering.

```
A negative review just came in. Draft a public response.

Review context:
- Star rating: ___
- Platform (Google / Yelp / TripAdvisor): ___
- Summary of the customer's complaint (in their words): ___
- Was the complaint specific (food, service, wait time) or general: ___
- Anything verifiably wrong with their complaint (e.g., wrong restaurant, factually inaccurate): ___

Output:
1. A public response under 80 words: acknowledge the issue, do NOT argue specifics in public, offer a private channel (email or DM).
2. A private follow-up email or DM (90-130 words) that takes accountability where due, makes one concrete remedy offer (free meal, comped item, etc.), and asks them to give us another shot.

Do NOT: offer remedies in the public response, blame staff, or quote menu prices. Match the brand voice from the master profile.
```

### 18. Photographer Gallery-Delivery Email + Upsell
**For:** Wedding photographers, portrait photographers, family photographers.

```
A client's gallery is ready to deliver. Draft the gallery-delivery email PLUS the upsell pitch.

Session context:
- Client name(s): ___
- Session type (wedding / portrait / family / branding): ___
- Number of edited images delivered: ___
- Gallery link: ___
- Gallery expiration / download deadline: ___
- Upsell options available (prints, albums, additional retouches): ___

Output:
1. Main delivery email (150-200 words): warm, references one specific moment from the session, includes the gallery link + the download deadline.
2. Soft upsell paragraph at the bottom: one specific print product I'd recommend based on the session type, with a "reply if you'd like me to mock something up" CTA. NOT a price-list dump.

Tone from the master profile. Sign with the photographer's first name.
```

### 19. Auto-Repair Estimate Walk-Through Script
**For:** Auto repair shops, mechanics, tire shops.

```
A customer's car came in for a check engine light. Diagnosis is done and the estimate is built. Draft the phone-call script the service advisor will use.

Estimate context:
- Customer name: ___
- Vehicle (year / make / model): ___
- Diagnosis (in plain language): ___
- Recommended repair: ___
- Total estimate (parts + labor): ___
- "Need to do today" vs. "can wait 30-60 days" items: ___
- Customer's prior visit history with us (first-time / returning): ___

Output: a 90-second phone-call script the advisor reads from. Use speaker labels (ADVISOR / CUSTOMER reactions in parens). Include:
- Plain-English explanation of what's wrong (no jargon).
- Why we recommend doing it now (or why it can wait).
- The price + timing.
- ONE objection-handling line ("if they say it's too expensive...").
- A clear close.

Match the shop voice from the master profile. No upsell pressure.
```

### 20. Pet-Service Boarding Confirmation + Upsell
**For:** Dog boarding, cat boarding, grooming, daycare, training facilities.

```
A boarding reservation was just confirmed. Draft the confirmation email + soft upsell.

Reservation context:
- Pet's name + breed: ___
- Owner's name: ___
- Check-in date + check-out date: ___
- Services already booked: ___
- Add-on services available (grooming, training session, extended play, photo updates): ___

Output:
1. Confirmation email body (under 200 words): all key dates, what to pack, drop-off window, our facility's specific check-in process.
2. ONE upsell suggestion paragraph based on stay length: e.g., for stays 5+ days, suggest a bath-before-pickup; for stays 3+ days, suggest a 1-on-1 play session.

Friendly, pet-parent-affirming tone from the master profile. Include the cancellation policy in one sentence at the bottom.
```

### 21. Childcare Enrollment Inquiry Response
**For:** Daycares, preschools, after-school programs, summer camps.

```
A parent just inquired about enrollment. Draft a personalized response.

Inquiry context:
- Parent name: ___
- Child's first name + age: ___
- Program of interest (full-time / part-time / before-after care / summer): ___
- Their stated timeline (immediate / next month / fall): ___
- Anything specific they mentioned (special needs, dietary, sibling already enrolled, transferring from another center): ___

Output:
- A warm, parent-to-parent reply (under 200 words) that addresses them by name, references their child by name, acknowledges their timeline, and offers a specific next step (tour booking link, application form, phone call slot).
- If their timeline is immediate, lead with availability honesty: do we have space in their child's age group?

Match the program's voice from the master profile. Avoid generic phrases like "we're a leader in early childhood education."
```

### 22. Insurance Broker Quote Walk-Through
**For:** Independent insurance brokers (auto, home, life, commercial).

```
A new lead requested quotes. Quotes are back. Draft the walk-through call script.

Lead context:
- Lead name: ___
- Policy type: ___
- Current carrier + premium (if they shared): ___
- Top 1-2 carriers we're quoting: ___
- Our recommended option + why: ___
- Annual savings vs. their current policy (if any): ___
- Coverage differences worth flagging (deductible, limits, exclusions): ___

Output:
1. A 5-7 minute phone call script the broker reads from. Speaker labels. Plain English.
2. Cover: opening (warm reset of their situation), our top recommendation + why, the coverage differences (in their words, not jargon), the price, and one objection-handling line.
3. End with a clear close: "do you want me to bind this today, or do you want to think it over until tomorrow?"

Match the brokerage voice from the master profile.
```

### 23. E-commerce Order Issue Resolution
**For:** Shopify / WooCommerce / Etsy / Amazon FBA SMB store owners.

```
A customer just emailed about an order issue. Draft the response.

Issue context:
- Customer name: ___
- Order number: ___
- Issue type (damaged / wrong item / late delivery / quality complaint / sizing / other): ___
- Customer's stated emotion (calm / frustrated / angry): ___
- Order value: ___
- Our default remedy policy for this issue type: ___

Output:
1. A response email (120-180 words): acknowledge the issue specifically (use their language), take responsibility where due, propose a clear remedy (replacement / refund / store credit), and give a concrete next step + timing.
2. Match emotional energy: if they're angry, be warm and assured; if they're calm, be warm and brisk.

Do NOT: ask them to send the item back before confirming the issue, blame the carrier or warehouse, or use the word "policy" as a shield. Match the brand voice from the master profile.
```

### 24. Coaching / Consultant Discovery-Call Follow-Up
**For:** Business coaches, executive coaches, consultants, fractional CXOs.

```
A discovery call just wrapped. Draft the follow-up email + the proposal-prep note.

Call context:
- Prospect name + title + company: ___
- Their stated biggest problem: ___
- Their stated outcome they want in 90 days: ___
- Engagement model that fits (1-on-1 weekly / monthly retainer / project-based): ___
- Investment range we discussed: ___
- Their stated decision timeline: ___

Output two artifacts:
1. EXTERNAL: a follow-up email (180-250 words) that summarizes their problem and desired outcome in their own words, names the engagement model, restates the investment, and gives a clear next step (proposal arrival timing or scheduling the next call).
2. INTERNAL: a 5-line proposal-prep note for you — what to emphasize, what to underplay, what objection is most likely, and one differentiator that came up in the call.

Match the practice voice from the master profile. NOT salesy.
```

### 25. Agency Monthly Client Report Drafter
**For:** Marketing agencies, design agencies, dev shops, freelancers with retainer clients.

```
End of month. Draft a client report for a retainer client.

Client context:
- Client name: ___
- Engagement scope (SEO / paid ads / social / content / dev / design): ___
- Hours / scope used this month: ___
- 3 KPIs we agreed to track: ___
- This month's numbers vs. last month: ___
- Notable wins (1-3): ___
- Notable blockers (1-2): ___
- What we plan to focus on next month: ___

Output a client-facing report with:
1. Executive summary (3-4 sentences a busy executive will actually read).
2. KPI scorecard (table format with month-over-month deltas).
3. Wins (bullets, with concrete numbers, not adjectives).
4. Blockers + what we need from them (specific asks, not vague).
5. Next month's top 3 focus areas.

Match the agency voice from the master profile. Confident but not boastful. If the month was bad, name it honestly and explain what changes for next month.
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
- More industry-specific superprompts (insurance claims handling, mortgage broker scenarios, pool service, landscaping, freight, medspa, etc.)
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
