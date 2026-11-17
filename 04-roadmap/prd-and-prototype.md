# Decline reason and retry hint, Simplified PRD (Riverty BU Pay & Credit, First Consumer Card)

**Scenario:** Riverty BU Pay & Credit, First Consumer Card

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Heavy BNPL user who runs two pay-later apps

## 1. The Big Picture
- **Vision:** Every declined card payment explains itself, so a heavy pay-later user fixes it at the till and does not reach for the debit card.
- **Press release:** Riverty card users now see why a payment failed and what to do next, within seconds of the decline. A clear reason and one retry hint replace the silent failure, in shops and online.

Until now a decline left users guessing. In the test launch, one participant was declined at a bakery with no reason shown and went back to her debit card the same week (N-06). 48 in-store declines were logged with no reason shown (T-101).
- **Success metric:** Heavy-user month-2 active share (1+ purchase two months after activation)
- **Guardrail:** Spend per active card

## 2. The Details
### User stories
- 1. As a heavy user paying in a shop, I want a push with the decline reason so that I know the problem before I leave the till.
- 2. As a user declined online, I want the same reason and hint in the app so that I can fix it without contacting anyone.
- 3. As a user whose decline reason is unclear to the system, I want a plain fallback message so that I am never left with a silent failure.
### Screens to build
- Entry point: Decline alert
- Feature core: Why it was declined
- Success: Payment completed
### Functional requirements
- 1. 100% of declines show a reason in the app. 0 silent declines (baseline: 48 silent in-store declines, T-101).
- 2. Each reason maps to exactly one retry hint, 20 words or fewer (assumption).
- 3. Both in-store and online declines are covered. In Month 4 in-store was about 18 declines on 206 attempts (8.7%), and online about 22 (derived).
- 4. A push fires within 5 s of a decline (assumption), and only one push per decline event, because late or duplicate alerts led users to pay again with another card (T-108).
- 5. Push opens the decline screen in 1 tap.
- 6. All user-facing copy is in German (assumption: German pilot), with the reason at 2 lines or fewer.
- 7. Every unmapped reason routes to a fixed “other” message.
### Smart behaviors (Situation → Outcome)
- In-store decline, reason mapped-> Push with reason. Tap opens Screen 2 with the matching hint.
- Online decline, reason mapped ->	Activity row “Declined” plus push. Same Screen 2.
- Reason unmapped	-> “Other” message and generic hint. No raw code shown.
- Push notifications off -> 	Row appears in the activity list with a red “Declined” state.
- TRY AGAIN succeeds ->	Screen 3. Activity row changes to “Paid”.
- TRY AGAIN fails -> 	Return to Screen 2 with the updated reason. After 2 failed retries, TRY AGAIN is disabled and the other-payment option is promoted (assumption).
- Same decline event reported twice -> 	One push, one activity row.
### Technical constraints
- One HTML file, plain JavaScript. No frameworks, no CDN scripts.
- No external APIs and no login. All data is synthetic and held in memory.
- No real authorization. TRY AGAIN is a scripted outcome per scenario.
- Style: Riverty Classic tokens (sharp corners, warm neutrals, serif headings, uppercase buttons).
- No generated text. Reasons and hints come from a fixed table in the file.

## 3. The Logistics
### Features out
- Changes to credit policy, limits or approval rules (N-11: months of re-approval).
- Reducing the decline rate itself. B1 explains declines and does not prevent them.
- Auto-retry or any override of a decline.
- Fraud or risk-rule detail in reasons.
- Notification infrastructure rebuild beyond this push.
- B3 balance view, B8 one due date, B4, B5, B6, B7.
- Merchant-facing decline detail.
### Edge cases & safety guard
- Reason code unknown - 	Fixed “other” copy (Requirement 7).
- Push delayed or not delivered- 	Row still appears in the activity list, so the decline is not silent.
- Retry succeeds on the second attempt - 	Screen 3 appears once, and the row shows “Paid”.
- User declined online and pays in a shop within seconds	- Declines are separate events, with separate rows and pushes.
- Decline for a reason that must not be shown (risk or fraud)	 - Show the “other” copy. Never disclose the cause.
- Safety guard: the app invents a reason	- Copy comes only from the approved table. If the system holds no reason, it says so and never guesses a cause.
### Decision log
- Reasons stay generic, with no risk or fraud detail. It protects compliance and avoids a re-approval cycle (N-11). Cost: some users get the “other” message.
- TRY AGAIN is a scripted simulation in the prototype, and one-tap retry stays SHOULD HAVE. It exists only to render Screen 3. Cost: the prototype shows a retry the production must-have list excludes. Decide whether to keep it.
### Evals
- 1	Accuracy	 - 100% of scripted decline scenarios (every mapped reason plus “other”, both channels) show the correct reason and hint. 0 silent declines.
- 2	Time on task  -	In a test with 5 or more heavy users, 80%+ state the reason and the next step within 10 s of tapping the alert.
- 3	Safety triggers	 - 0 risk or fraud disclosures. 0 ungrounded reasons. 100% of unmapped codes fall back to “other”.

## MoSCoW scope
- **Must:** - Every decline shows a plain-language reason in the app. Without it the user cannot tell why it failed (T-101, N-06). It needs a fallback reason (“other”), so no decline stays silent.; - One retry hint per reason. It tells the user what to do next with the card. A reason alone leaves them stuck at the till.; - Covers both in-store and online declines. In-store: 8.7% decline rate in Month 4, about 18 declines on 206 attempts. Online: about 22 declines in Month 4 (derived), so an in-store-only fix misses more than half.; - Push notification at the time of decline. The user is at the till and not in the app. T-108 shows late pushes make users assume failure and pay with another card.; German copy; - Merchant-facing decline details.
- **Should:** - Decline and retry instrumentation: log reason code and whether a card purchase follows within a set window. By your rule this is not a must-have. I would still promote it, because without it the go/no-go decision has nothing to read.; - Decline history in the app: the user can look back at why a payment failed.; - One-tap retry: a retry action from the notification.; - Support link from the decline message.
- **Could:** Reason-specific personalised hints based on the user’s history.; Early warning before a likely decline (for example, an approaching limit).; “Was this helpful?” feedback.
- **Won't (now):** - Changes to credit policy, limits or approval rules: N-11 says changes take months to re-approve.; - Reducing the decline rate itself. B1 explains declines and does not prevent them.; - Auto-retry or any override of a decline.; - Detailed fraud or risk-rule reasons. Reasons stay generic and compliance-approved.; - Notification infrastructure rebuild (the T-108 timing fix beyond this push).; - Other backlog items: B3 balance view, B8 one due date, B4 pay-now-or-later, B5 offers, B6 cashback, B7 physical card.

