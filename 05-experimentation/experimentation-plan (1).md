# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on N-07 (“I could not see in one place what I owe on the card and what I owe on my normal pay later orders”), the matching tickets T-103 and T-104, and pilot cohorts that lose 11.3-20.5pp of active cards in the first month after activation (only 51.0-57.1% still active in month 2), I believe that giving heavy BNPL users who run several pay-later apps one balance and one due date for card and invoice will result in more of them still buying two months after activation, as measured by a 10 percentage point increase in heavy-user month-2 active share. I will protect spend per active card at EUR 233.15 or higher (Month 4 level) and will make a go/no-go decision after two consecutive activation cohorts have each reached month 2, with 100 or more heavy activated cards per cohort.
- **From M3, your primary success metric & guardrail metric:** Primary success metric:
Heavy-user month-2 active share (cards with 1+ purchase two months after activation). 
Baseline: All-user baseline is 51.0% (M1 cohort) and 57.1% (M2 cohort).
Guardrail metric: Spend per active card
- **From M4, the feature you scoped in your PRD this is what you're testing:** Decline reason and retry hint

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** Decline reason and retry hint
- **Persona pull your M2 persona:** Heavy BNPL user who runs two pay-later apps
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** More heavy-users will still be buying two months after activation, as measured by a 10 percentage point increase in heavy-user month-2 active share.
- **Primary success metric the one number that defines success, from M3:** Heavy-user month-2 active share (cards with 1+ purchase two months after activation).
- **Baseline rate today's rate of your primary metric, from your M3 data:** All-user baseline is 51.0% (M1 cohort) and 57.1% (M2 cohort). Request the heavy-segment baseline first.
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Spend per active card must not fall below EUR 233.1
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** 10 pp absolute
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 386 per arm.
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50, Cover 2 or more payday cycles (assumption).
- **Significance threshold p < 0.05 is standard, explain any deviation:** 80%/ 5%

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** Today’s experience, unchanged: declines are silent.

In-store payment declines with no reason shown in the app (T-101). 48 in-store declines were logged.
N-06: declined at a bakery, the app did not say why, and the participant went back to the debit card the same week.
Purchase pushes arrive minutes late in some shops, so users assume failure and pay again with another card (T-108).
Decline context: Month 4 in-store decline rate 8.7% (about 18 declines on 206 attempts) and overall 3.5%. Online declines were about 22 in Month 4 (derived).
Funnel context (M3): 431 activated cards, 81.2% buy in the activation month, and 51.0-57.1% of cohorts are active in month 2.
Balance and reminder friction (T-103, T-104) stays in both arms.
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** One change: every decline explains itself with a reason and one retry hint.

Screens (from the PRD):

Entry point, Decline alert: lock-screen push card (title, merchant, amount, short reason, timestamp), activity list with a red “Declined” row, tap target opening Screen 2.
Feature core, Why it was declined: header with back link, transaction summary (merchant, amount, channel, time), reason block (headline, 1-2 line explanation), retry hint block, primary button TRY AGAIN, secondary button USE ANOTHER PAYMENT METHOD.
Success, Payment completed: success icon and headline, merchant, amount, time, button DONE returning to the activity list, where the row now reads “Paid”.

Functional requirements (MUST HAVE, from the PRD):

100% of declines show a reason in the app. 0 silent declines.
Each reason maps to exactly one retry hint, 20 words or fewer.
Both in-store and online declines are covered.
A push fires within 5 s of a decline, one push per decline event.
Push opens the decline screen in 1 tap.
All copy is in German, with the reason at 2 lines or fewer.
Every unmapped reason routes to a fixed “other” message.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, eligibility rules, notifications, onboarding). If something changed inadvertently, your test is compromised.:** Identical in both arms:

App version and release timing.
Approval, eligibility and credit policy. Limits, pricing and terms (N-11).
Decline rate: B1 explains declines and does not change them.
Balance screens and reminders (T-103, T-104). Instalment display (T-105).
Onboarding, identity check (T-106) and wallet add (T-102).
Partner offers, cashback and help articles (T-107).
Randomization: per card at activation, stratified by employee vs friend/family (assumption)

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that Decline reason and retry hint for Heavy BNPL user who runs two pay-later apps will result in More heavy-users will still be buying two months after activation, as measured by a 10% increase in heavy-user share within 2 months.., as measured by a 10 change in Heavy-user month-2 active share (cards with 1+ purchase two months after activation). within 2 weekly cycles. We will protect Spend per active card throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if Heavy-user month-2 active share (cards with 1+ purchase two months after activation). improves by ≥ 10 at 80%/ 5% and Spend per active card does not reach Spend per active card must not fall below EUR 233.1 after 2 weekly cycles. We will ITERATE if direction is positive but lift is below MDE. We will KILL if the primary metric shows no improvement or moves negatively. The read date is fixed at the end of 2 weekly cycles, no results reviewed before then.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** _(not filled in)_
