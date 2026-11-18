# A/B Experiment Brief, Riverty BU Pay & Credit, First Consumer Card

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Decline reason and retry hint |
| Persona | Heavy BNPL user who runs two pay-later apps |
| Expected outcome | More heavy-users will still be buying two months after activation, as measured by a 10%  increase in heavy-user share within 2 months.. |
| Primary success metric | Heavy-user month-2 active share (cards with 1+ purchase two months after activation). |
| Baseline rate | All-user baseline is 51.0% (M1 cohort) and 57.1% (M2 cohort). |
| Guardrail metric | Spend per active card |
| Guardrail boundary | Spend per active card must not fall below EUR 233.1 |
| Second guardrail | Overall decline rate must not exceed 3.5% (Month 4), because a balance view must not add declines. |
| Minimum Detectable Effect | 10 |
| Sample size per arm | 386 |
| Traffic split | 50/50 |
| Test duration | 2 weekly cycles |
| Significance threshold | 80%/ 5% |

## Control vs. Variant
- **Control (A):** Today’s experience, unchanged: declines are silent.

In-store payment declines with no reason shown in the app (T-101). 48 in-store declines were logged.
N-06: declined at a bakery, the app did not say why, and the participant went back to the debit card the same week.
Purchase pushes arrive minutes late in some shops, so users assume failure and pay again with another card (T-108).
Decline context: Month 4 in-store decline rate 8.7% (about 18 declines on 206 attempts) and overall 3.5%. Online declines were about 22 in Month 4 (derived).
Funnel context (M3): 431 activated cards, 81.2% buy in the activation month, and 51.0-57.1% of cohorts are active in month 2.
Balance and reminder friction (T-103, T-104) stays in both arms.
- **Variant (B):** One change: every decline explains itself with a reason and one retry hint.

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
- **Held constant (isolation check):** Identical in both arms:

App version and release timing.
Approval, eligibility and credit policy. Limits, pricing and terms (N-11).
Decline rate: B1 explains declines and does not change them.
Balance screens and reminders (T-103, T-104). Instalment display (T-105).
Onboarding, identity check (T-106) and wallet add (T-102).
Partner offers, cashback and help articles (T-107).
Randomization: per card at activation, stratified by employee vs friend/family (assumption)

## Hypothesis
> I believe that Decline reason and retry hint for Heavy BNPL user who runs two pay-later apps will result in More heavy-users will still be buying two months after activation, as measured by a 10%  increase in heavy-user share within 2 months.., as measured by a 10 change in Heavy-user month-2 active share (cards with 1+ purchase two months after activation). within 2 weekly cycles. We will protect Spend per active card throughout the test.

## Shipping criteria
> We will **ship** if Heavy-user month-2 active share (cards with 1+ purchase two months after activation). improves by ≥ 10 at 80%/ 5% and Spend per active card does not reach Spend per active card must not fall below EUR 233.1 after 2 weekly cycles.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 2 weekly cycles, no results reviewed before this date.
