# Decline reason and retry hint

> Every decline explains itself and tells you how to retry, so heavy BNPL users finish the purchase on their Riverty card instead of switching back to debit.

**Violeta Vasiliu, Cohort #2, November 2026** · https://github.com/VioletaVas/pm-final-project

Prototype: 04-roadmap/prototype.html

---

## Final Project Deliverables

### Slide 5 · Strategy
- **Problem:** ## Responses
- **Chosen path, which Riverty business-unit case are you using?:** Business Unit - Pay & Credit
- **Strategic crisis, based on the brief, if the company does nothing for 12 months, what happens to its market position?:** Riverty stays a checkout option that merchants and consumers can swap out. This is a hypothesis, not a measured loss.

Consumers: the best segment is already being served elsewhere. Heavy BNPL users activated at 82.6% and spend €320.88 a month, with 25.4% of purchases on instalments. They already run “two of these apps” [N-02], and without a Riverty card they keep paying with their bank card in shops [N-03].

Merchants: a card that works at every shop weakens Riverty’s checkout pitch (“why would my customers still pick you?” [N-08]). SMEs only value it if the card sends traffic to them, not to marketplaces [N-09].

Timing: Riverty has a banking licence and has said it will grow consumer finance with new products. Staying out of the wallet means the licence produces no consumer product. 

Cost of waiting: the test frictions stay unfixed. 143 activated cards never reached the phone wallet [T-102], and 48 in-store payments were declined with no reason shown [T-101].
- **Moment of misery, what is the user likely doing outside the product (Google, spreadsheets, a competitor) because your tool isn’t serving them?:** Observed in the pack:

After a decline: they go back to their debit card within the week [N-06]. In Month 4, 8.7% of in-store attempts were declined.
After a late push notification: they assume the payment failed and pay again with another card [T-108].
Before payday: they check several pay-later apps [N-02].

Inferred, so verify in interviews:

Tracking the total: they add up card and pay-later balances by hand in notes or a spreadsheet, because two screens show two totals [N-07, T-103].
Searching: they google whether the card affects their credit score [T-107] and which due date applies [T-104].
- **Problem hook, summarize the business risk and user pain into one urgent sentence.:** Riverty’s heaviest pay-later users already juggle several apps, and the test card sends them back to their debit card at the first unexplained decline, so unless one balance and reliable in-store payment ship soon, the banking licence launches a card nobody keeps in their wallet while merchants question Riverty’s checkout.
- **Value proposition, based on the initiative in your assigned Riverty case, what is the new value and why is it urgent to launch now?:** New value: pay later anywhere, with one balance and one due date for card and invoice, and clear reasons when a payment fails. For merchants, the card brings offers that send shoppers to their shops.

Why now:
The licence is live.
The heavy-user segment shows demand.
The Month 1 cohort’s activity falls from 66.3% in month 1 to 51.0% in month 2, so the fixes are needed now.

Challenge to “launch now”: the pack supports deciding now, not a broad launch. The cohort is 53% employees (calc) and risk flags that approvals will look better than real customers [N-10]. Changes also take months to clear approval [N-11].

Recommendation: make the launch conditional on fixing B1 (decline reasons), B2 (wallet at approval) and B3/B8 (one balance and due date), starting with heavy BNPL users plus a non-employee cohort.

## Cold-read your own hook
- **Is the business risk high enough to justify a new initiative, a high-stakes threat, or a minor inconvenience?:** Risk level: initiative-worthy, not yet a proven threat

Supports an initiative:

Funnel: 431 of 1,200 invited (35.9%) activated, and 253 (21.1%) made 3+ purchases in their activation month.
Heavy BNPL users: they activated at 82.6% vs 62.0% for light users, with 5.82 vs 2.46 purchases a month. The segment with the most to gain is the most engaged.
Retention: each activation cohort loses 11 to 21 points of active cards between month 0 and month 1. The Month 1 cohort falls from 77.6% to 51.0% by month 2 (calc).
Active cards: they fell from 278 to 262 in Month 4 while cumulative activations rose (calc), and the decline rate rose from 2.6% to 3.5%.

Why it is not yet a high-stakes threat:

Thin evidence base: it rests on 4 months, 1,200 invitees and 12 notes. Merchant disintermediation rests on two quotes [N-08, N-09], and the pack has no competitor data.
Unmeasured inputs: take-up and annual churn are not measurable in the test, so I can’t size a loss.
Behavior vs approval bias: employees and friends behave alike (activation 71.9% vs 76.1%, spend €222 vs €216). Approval of invited differs (55.1% vs 41.7%, calc), so the bias risk in [N-10] shows up at approval, not usage.

Verdict: the evidence justifies a scoped fix-and-gate initiative. A “do nothing is a crisis” claim needs competitor and merchant data first.
- **Is the moment of misery a systemic problem or just an edge case?:** Moment of misery: systemic in two places
Problem	Systemic or edge?	Evidence
In-store reliability	Systemic	In-store decline rate was 6.4% to 12.1% vs 2.2% to 3.5% overall. 48 declines were logged with no reason shown [T-101].
Split balances and due dates	Systemic by design	Two screens, two due dates, double reminders [T-103, T-104, N-07]. No count of affected users.
Wallet gap	Systemic, limited reach	33.2% of activated cards (143 of 431) never reached the wallet [T-102]. It only matters for in-store payments, which are 15% to 18% of purchases.
Credit score question, ID re-upload, late push	Unquantified, likely edge	One ticket each [T-106, T-107, T-108].

Blind spot: my earlier answer focused on post-activation. The largest leaks are earlier (calc):

Did not apply: 484 invitees, the biggest leak, with no cause in the pack.
Lost between approval and activation: 155 of 586.
Failed identity check: 88 applicants, partly tied to [T-106].
- **Does the value proposition actually remove the obstacle you identified, or is it a generic feature?:** Value proposition: partly specific, partly generic

Removes real obstacles:

One balance and one due date (B3, B8): this directly targets [T-103, T-104, N-07] and is hard for competitors to copy, because it needs Riverty’s invoice base.
Decline reason and retry (B1): it fixes the “no explanation” gap [N-06]. It does not fix the cause of declines, which the pack doesn’t identify (credit policy, limits or technical).
Wallet at approval (B2): it fits the abandonment in [T-102], but the cause of the failures is unknown.

Generic or unproven:

“Pay later anywhere” as the headline: instalments are only 15% to 18% of purchases, and the option appears for some categories only [T-105]. Many pay-later apps already offer this.
Cashback (B6): [N-12] says it drives a first try, not continued use.
Merchant offers (B5): no evidence yet that offers change behavior. Partner merchants already carry 56.8% to 63.1% of card volume, which gives a base to test on.

Sharper prop: one balance, one due date, and clear reasons when a payment fails, for existing pay-later users. Lead with that and treat “anywhere” and cashback as secondary.
- **Value proposition:** Pay later anywhere, with one balance and one due date for card and invoice, and clear reasons when a payment fails. For merchants, the card brings offers that send shoppers to their shops.
- **Hypothesis:** ## Pre-work · Hypothesis check
- **Role , who you are solving for (from M2):** Heavy BNPL user, 18-34, runs two pay-later apps
- **Goal , what this user is ultimately trying to achieve:** Use the Riverty card for everyday spend, including splitting the big weekly shop, without adding another app to monitor and calculate independently how much they need to pay.
- **Friction / moment of misery , the specific pain blocking their goal:** The app shows card balance and pay later orders on two different screens, so they cannot see in one place what they owe. Two reminders for different amounts then arrive in the same week bringing "one more thing to check before payday".
- **Current workaround , the external tool or manual process they rely on (M2):** Open each pay-later app and the Riverty card screen.
Read each balance and due date separately.
Sum the amounts mentally, with some external tool.
Reconcile two reminders against each other.
Ask support or the nearest participant which total is real.
Fall back to the debit card when uncertain.
- **Problem Hook , your one-sentence framing of the business crisis (M1):** Riverty’s heaviest pay-later users already juggle several apps, and the test card sends them back to their debit card at the first unexplained decline, so unless one balance and reliable in-store payment ship soon, the banking licence launches a card nobody keeps in their wallet while merchants question Riverty’s checkout.
- **Value Proposition , the outcome your initiative promised to deliver (M1):** Pay later anywhere, with one balance and one due date for card and invoice, and clear reasons when a payment fails.

## Read the evidence in your case
- **Where does your case say people stall or leave? Does that match the friction you wrote in Module 2?:** After approval, the funnel loses the most people at activation (155 of 586, 26.5%) and at the move from first purchase to 3+ purchases (97 of 350, 27.7%). The biggest raw drop is invited to applied (484, 40.3%), but that happens before anyone meets the product. The funnel shows leaving only, with no timing data, so I cannot separate stalling from leaving.

It matches the previously identified friction only partly.
The split-balance and two-reminder friction (T-103, T-104) happens after purchase, where this funnel stops, so it is not testable here. It fits the retention data better (51.0-57.1% of cohorts active in month 2). The 3+ purchase drop is consistent with habit and app fatigue (N-02, N-03), and the 88 lost between applied and identity check fits T-106 (identity re-upload), but we have no count of failed uploads to confirm it.
- **What got better or worse in the case, and does that support the workaround your persona uses?:** What got better: Spend per active card: EUR 200.09 → 233.15, with stayers buying more often (3.82 → 4.23 purchases, derived).
Month 2 cohort retains best: 57.1% active in month 2, versus 51.0% for Month 1.
In-store decline rate: 12.1% → 8.7%, with a low of 6.4% in Month 3.

What got worse: Every cohort loses 11-20pp in its first month after activation: M1 -11.3pp, M2 -12.8pp, M3 -20.5pp.
Month 3 cohort is the weakest on a like-for-like basis: only 75.7% of its first-month buyers returned (103 of 136), versus 85.5% for Month 1 and 84.4% for Month 2 (derived).
Share of all activated cards that are active fell 77.6% → 60.8% (derived).
Online declines drove the Month 4 overall decline-rate rise (2.2% → 3.5%), per my previous read.

Does it support the persona’s workaround? Potentially.
Losses concentrate in months 1-2 after activation, after the first purchases. That is when balances build and reminders land, which is where the split-balance friction (T-103, T-104) would sit.
This is a hypothesis. The pack has no reminder dates, balance views, repayment data or inactivity reasons. Nothing here shows that the friction caused the drop.
The debit-fallback story (N-06) fits only weakly: in-store share is flat at 15.4-17.7%, and online declines are rising too.
- **Which user in the case is carrying the pain, and is that the person your Module 2 persona describes?:** Two different people carry two different kinds of pain. Light users are visibly leaving. Heavy users carry the most value and the most obligations to track, but this snapshot shows no pain for them. Our persona (heavy, 18-34) is the person with the most at stake. Nothing here shows she is the one suffering most.

Heavy users look healthiest on every engagement metric, yet our friction story is about them. Either they tolerate it, or it bites later in retention. This snapshot cannot tell which.

## Step 2 · Craft your hypothesis
- **Qualitative evidence (from M2) , quote the specific friction / moment of misery for your persona:** N-07: “I could not see in one place what I owe on the card and what I owe on my normal pay later orders.” N-02: “A third card is one more thing to check before payday.” Supported by T-103 (two screens, “which total is the real one”) and T-104 (two reminders, different amounts, same week).
- **Quantitative evidence (from M3) , name the metric or data point that confirms the pain; cite the number:** The pack has no metric that measures balance confusion directly. Best proxies: (1) cohorts lose 11.3-20.5pp of active cards in the first month after activation, and only 51.0-57.1% are still active in month 2. (2) Heavy users carry the most obligations: 25.4% instalments, 5.82 purchases per active month. (3) Heavy users are the value segment: 82.6% activation, EUR 320.88 monthly spend, 32.0% of activated cards (138 of 431). The cause of the retention loss is unproven.
- **Persona , role, goal, and the friction you confirmed in the reconciliation steps:** Role: heavy BNPL user who runs two pay-later apps (N-01, N-02, N-04). Goal: everyday spend, including the big weekly shop (N-04), without another app to monitor. Friction confirmed: split balance and mismatched reminders (T-103, T-104, N-07). Reconciliation caveat: BNPL intensity is supported (2.6x spend vs light). 18-34 is weak: age moves spend only 1.2x (EUR 190.75-235.75), and the pack has no age × intensity cross-tab. Keep “18-34” only as an assumption.
- **Problem you are solving , one sentence describing the specific friction this initiative removes:** Heavy pay-later users cannot see one total or one due date for card and invoice, so the card adds a check instead of removing one.
- **Strategic outcome , what behaviour change do you expect, and how does it map to retention / revenue / churn?:** Behavior: heavy users stop checking several places and keep the card in use after the first statement. Retention: higher month-2 active share than the 51.0-57.1% baseline. Revenue: more months at heavy-user spend (EUR 320.88 vs EUR 125.13 for light). Churn: not measurable. The pack says four months cannot support an annual churn figure.
- **Primary success metric (initiative signal) , the leading indicator that tells you the gap is closing:** Heavy-user month-2 active share (cards with 1+ purchase two months after activation). Baseline: not in the pack for heavy users. All-user baseline is 51.0% (M1 cohort) and 57.1% (M2 cohort). Request the heavy-segment baseline first.
- **Guardrail metric (product signal) , the metric that must NOT drop; it protects your existing base:** Spend per active card must not fall below EUR 233.15 (Month 4). Secondary: overall decline rate must not exceed 3.5% (Month 4), because a balance view must not add declines.
- **Decision window , how much time or data before you scale, pivot, or kill? minimum threshold to proceed?:** Minimum to read a result: two activation cohorts that have each reached month 2. In the pilot only M1 and M2 qualify. Sample is the binding constraint: the whole pilot has 138 heavy activated cards, and the M4 cohort has just 39 cards overall. A single cohort of that size cannot support scale or kill. Proposed thresholds (assumption, not grounded): scale if heavy month-2 retention beats baseline by 10pp or more across two cohorts of 100 or more heavy cards each. Pivot if the gain is 0-10pp. Kill if there is no gain after two cohorts. Timing risk: N-11 says changes needing re-approval take months, so B8 (one due date) may not ship inside the window.
- **Draft your full hypothesis sentence , one to three sentences; quote the metric, name the persona, name the outcome:** Based on N-07 (“I could not see in one place what I owe on the card and what I owe on my normal pay later orders”), the matching tickets T-103 and T-104, and pilot cohorts that lose 11.3-20.5pp of active cards in the first month after activation (only 51.0-57.1% still active in month 2), I believe that giving heavy BNPL users who run several pay-later apps one balance and one due date for card and invoice will result in more of them still buying two months after activation, as measured by a 10 percentage point increase in heavy-user month-2 active share. I will protect spend per active card at EUR 233.15 or higher (Month 4 level) and will make a go/no-go decision after two consecutive activation cohorts have each reached month 2, with 100 or more heavy activated cards per cohort.

### Slide 6 · Research
- **Competitive analysis:** ## Responses
- **Role, who are you solving for? (the specific user segment or profile):** A heavy BNPL user aged 18-34 who already runs two pay-later apps and treats pay later as the default for most purchases (N-01, N-02, N-04).
- **Goal, what is this user ultimately trying to achieve?:** Use the card for everyday spend, including splitting the big weekly shop (N-04), without adding another app to monitor.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** The app shows card balance and pay later orders on two different screens, so they cannot see in one place what they owe (N-07, T-103). Two reminders for different amounts then arrive in the same week (T-104). N-02 names the cost: “one more thing to check before payday.”
- **External tools, the outside platforms or tools the user is forced to use:** spreadsheet, notes app, banking app, calendar) used to work around the split-balance friction.
- **The process, the 3 to 5 manual steps the user takes to get the job done:** 1. Open each pay-later app and the Riverty card screen.
2. Read each balance and due date separately.
3. Sum the amounts mentally, with some external tool.
4. Reconcile two reminders against each other (T-104).
5. Ask support or the nearest participant which total is real (T-103).
6. Fall back to the debit card when uncertain (N-03, N-06).
- **Core frustration, the exact moment the process feels most “broken”:** Not knowing what they owe in total, at the moment a payment demand arrives.
- **The evidence, a specific quote or behavior from the research that proves this:** This is the point where T-103 and T-104 collide:

Two reminders arrive in the same week for different amounts (T-104).
The card balance and pay later orders sit on separate screens, so nothing reconciles them (T-103, N-07).
Participants ask which total is the real one (T-103).

The process is most broken here because the user is being asked to pay and cannot verify the figure. Everything before it is just checking. This is the moment the checking fails to produce an answer.
- **Your journey map file name (e.g. journey-map.html):** journey-map.html
- **Journey map:** file:///Users/violeta.vasiliuriverty.com/Downloads/journey-map.html

Activate & Add to Wallet
User Action
Add card to wallet at approval -> tap-to-pay ready immediately
Internal State (inferred)
Eager to try it; low patience for setup
Pain Point Addressed
Wallet add inside approval (B2) -> fixes 143 of 431 cards never added (T-102)
2
Pay in Shop
User Action
Tap card at supermarket -> split the weekly shop, no extra app
Internal State (inferred)
Expects debit-card reliability (N-03)
Pain Point Addressed
Decline reason and retry hint (B1) -> no silent switch to debit (T-101, N-06)
3
Check One Balance
User Action
Open app before payday -> see card and invoices as one total
Internal State (inferred)
In control; one look settles the question (N-02)
Pain Point Addressed
One balance view (B3) -> ends "which total is real" (T-103, N-07)
4
Settle on One Due Date
User Action
Receive one reminder -> pay one amount on one date
Internal State (inferred)
Confident the amount is right (T-104)
Pain Point Addressed
One due date (B8) -> replaces two conflicting reminders (T-104)

### Slide 7 · Blueprint
- **Roadmap:** ## Your strategic anchors
- **Persona (M2), who are you solving for?:** A heavy BNPL user who already runs two pay-later apps and wants to use the card for everyday spend, including the big weekly shop, without another app to monitor.
- **Primary success metric (M3), your leading indicator:** Heavy-user month-2 active share, meaning cards with 1+ purchase two months after activation. Baseline is not in the pack for heavy users. The all-user figures are 51.0% (Month 1 cohort) and 57.1% (Month 2 cohort).
- **Moment of misery (M2), the specific friction blocking the goal:** A payment reminder arrives and the user cannot tell whether its amount is the real total. Card and pay later orders sit on two screens (N-07, T-103), and two reminders for different amounts arrive in the same week (T-104). N-02: “one more thing to check before payday.”
- **Guardrail metric (M3), what must not drop or break:** Spend per active card at EUR 233.15 or higher (Month 4 level). Optional second guardrail: overall decline rate at or below 3.5%.

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** Instinctive quick wins (without use of AI):

B1- Decline reason and retry hint shown in the app
B2 - Add to phone wallet straight from the approval screen	
B4 - Choose pay now or pay later per purchase after paying

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** Where I have overwritten the AI:

B1: Decline reason and retry hint
AI: 3 / 2
ME: 4 / 2
Fill-in → Quick Win

I opted against placing it as a fill-in, as suggest and more toward a quick-win. It easy to implement technically and minimizes the customer friction of getting declines with no clarity or call to action.

B2: Add to wallet from approval
AI: 2 / 2
ME: 4 / 2
Fill-In → Quick Win

143 of 431 activated cards (33.2%) never reached the wallet (T-102), so those cards cannot tap in shops. My persona’s goal includes the big weekly shop (N-04), which is in-store. AI discounted B2 because heavy users’ in-store share is only 12.1%, but a low share could be a result of the wallet and decline gaps rather than a preference. Heavy users make about 0.70 in-store purchases per active month (derived), close to other segments, so exposure is real, and there is real potential for strengthening the usage of cards, if only it were easier to have it added directly into the customers' wallet.

B4 Pay now or later per purchase
AI: 2 / 4
ME: 4 / 3
Time Sinker → Major Project

Heavy users use instalments most (25.4% of purchases), and T-105 shows an instalment option already appears after purchase for some categories. If that mechanism exists, extending it costs less than the build the AI assumed, so effort 3 is plausible. Moreover, providing customers the option to choose when to pay is a major opportunity and need for our customers.
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** The AI did not overvalue features, but rather diminished the value of some - particularly because it is driven by the pack data set.
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** Yes, it underweighted 3 features, please see the above section on where I decided to override the AI.

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** Decline reason and retry hint
N-06 returned to debit after a silent decline, and Month 4 in-store declines were 8.7%; this protects the 3.5% decline guardrail rather than the core friction.

Add to wallet from approval
Fixes 143 of 431 cards missing the wallet (T-102), but the persona’s in-store share is only 12.1% and online purchases do not need the wallet.
- **What I cut, and the “no” I’m protecting the scope from:** Physical card, No note or ticket asks for it, and the wallet route already covers tap-to-pay.
- **PRD highlights:** # Decline reason and retry hint, Simplified PRD (Riverty BU Pay & Credit, First Consumer Card)

**Scenario:** Riverty BU Pay & Credit, First Consumer Card

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Heavy BNPL user who runs two pay-later apps

## 1. The Big Picture
- **Vision:** Every declined card payment explains itself, so a heavy pay-later user fixes it at the till and does not reach for the debit card.
- **Press release:** Riverty card users now see why a payment failed and what to do next, within seconds of the decline. A clear reason and one retry hint replace the silent failure, in shops and online.

Until now a decline left users guessing. In the test launch, one participant was declined at a bakery with no reason shown and went back to her debit card the same week (N-06). 48 in-store declines were logged with no reason shown (T-101).
- **Success metric:** Heavy-user month-2 active share (1+ purchase two months after activation)
- **Guardrail:** Spend per active card

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
- **Prototype:** 04-roadmap/prototype.html

### Slide 8 · Validation
## Parameters
| Parameter | Decision |
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

### Slide 9 · Launch
- **GTM:** # GTM Launch Plan, Riverty BU Pay & Credit, First Consumer Card

| Field | Value |
| Feature | _(not filled in)_ |
| Goal | _(not filled in)_ |
| Launch tier | S, Minimal |

## Goal & Audience
- **Goal:** _(not filled in)_, Decline reason and retry hint
- **Target audience:** Heavy BNPL user who runs two pay-later apps

## Launch Tier
- **S, Minimal**, Reach - About 431 activations a month. Roughly 40 declines a month across all users (18 in-store plus about 22 online, derived). Heavy, push-enabled cards are about 32 a month (my assumption, from the audience sizing).

Revenue impact - The brief has no ticket size or margin per recovered purchase. The mechanism is recovered declines plus better month-2 retention.	Unquantified. Do not claim a number.
Risk of silence	The feature announces itself at the decline moment. Without an announcement, users see the same decline experience they have today.

Risk of over-investing - Any campaign (email, in-app banner, push) would reach users who never hit a decline, and would contaminate the A/B test.
Reversibility - 	Copy and screen change, no policy, pricing or credit change.

## Channels
1. **Owned: It reaches the audience at the moment of the decline, which is the only moment this feature matters. Audience: about 75K heavy, push-enabled users (assumed). The push must fire within 5 s, once per decline, and open the decline screen in 1 tap. Shipping the feature is the channel. No campaign is needed.**
2. **Owned: Decline screen, red “Declined” row in the activity list, changelog entry, and a push opt-in prompt at activation. Reaches the ~105K heavy monthly app users (assumed) and covers the 75% without push (assumed), who see the declined row only after opening the app. The opt-in prompt is a launch prerequisite. Without push, Channel 1 does not reach most of the base.**
3. **Owned: Targets heavy users with email opt-in, about 120K (assumed). It is the only owned channel that does not depend on push or app opens. It reaches only users who hit a decline after the launch announcement, and it would contaminate the A/B test, so hold it until the experiment reads out. Trigger: M tier only if the primary metric lifts and the guardrail holds.**

## Enablement & Assets
Support/CS - Decline reason to retry hint table, German macros, an FAQ line on what the feature does not do, and a way to see the user’s experiment arm
Product/Risk - Statement that approval, limits and decline rate are unchanged (held constant in both arms)
Partner/Merchant mgmt - Short note on in-store decline context and known shop-side push latency for merchants who ask
Marketing - Message guardrail: no external claims until readout

## Ownership, Budget & Timeline
- **Ownership & budget:** Experiment design and decision rule - Violeta, Product Manager - 	Rewritten hypothesis, primary metric, guardrails, ship/iterate/kill rule

Baseline pulls (heavy share, exposure per card, recovery baseline, decline vs no-decline M2 share) - 	Mike, Data Analyst - Four numbers that confirm the test is feasible

Reason to hint mapping table, German copy	Ria, Content/UX Writer	- Single source of truth, hints of 20 words or fewer, “other” fallback

Decline push (5 s, one per event, 1-tap open)  Kevin, Engineering Lead - Push SLA met, latency logged

Push opt-in prompt at activation  - Andrew, Engineering Lead - Prompt live before launch

Randomization, stratification, SRM check -  Mike, Data Analyst	- Assignment by heavy flag and employee vs friend/family

Support macros and FAQ, contact tagging by reason - 	Christian, Support Lead - Macros live, tagging in place

Risk sign-off (decline rate and policy unchanged) - Rishu, Risk/Credit Lead - Written confirmation

Internal brief, changelog, demo - Marina, Product Marketing Manager - 	Assets 2 to 5 from the mapping table

Readout and ship decision - Violeta, Product Manager (decision), Bandan, Head of BU Pay & Credit (approver) - Decision against the pre-registered rule

Budget:
Engineering. The decline push (5 s SLA) and the push opt-in prompt are new builds. T-108 shows push latency is already unreliable in shops, so feasibility of the 5 s SLA is unconfirmed.
Data.
Experiment instrumentation: decline-event logging in both arms, recovery metric, push latency.
Heavy-user flag at activation. It is not observable unless self-reported, so a source must be confirmed.
Translation and legal review. German copy review for each reason and hint, if not covered in-house.
Support capacity. Macro build and tagging by reason.
Cannot build today (unconfirmed):
Heavy-user flag at activation.
Unconditional spend per activated card guardrail baseline.
Heavy-user baseline for the primary metric.
Not needed. Paid media, agency work and video, per the S tier.
- **Timeline:** Phase 1, Beta

Pull the four baselines and decide whether the test is feasible.
Finalize the mapping table and the decision rule (pre-registered).
Build the push, the decline screen and the opt-in prompt.
Internal dogfood on employee cards.
Gate to Phase 2: all validity gates pass (100% of declines logged, push p95 at 5 s or under, one push per event, SRM clean) and Risk has signed off.

Phase 2, Launch moment

Start the 50/50 experiment on new activations, stratified by employee vs friend/family and by heavy flag.
Ship the support macros, the changelog line and the internal brief.
No external comms.
Gate to Phase 3: the pre-set horizon is reached. Enrollment time depends on the heavy share, at 1.8 to 17.9 months for 772 heavy cards. The month-2 metric adds about 60 days after the last enrollment. The triggered recovery metric needs about 180 decline events, about 4.5 months at current all-user volume (my estimate).

Phase 3, Post-launch

Read out against the decision rule: ship, iterate or kill.
If shipped, roll out to the full activated base and move to the M tier (lifecycle email to opted-in heavy users).
Review support volume by reason, the “other” share and the USE ANOTHER PAYMENT METHOD click share.
Update the mapping table for reasons that fall into “other”.

## Success Metrics
- **Metrics:** 1	Decline recovery rate (primary)	- Share of decline events followed by a successful card payment at the same merchant within [window]	
2	Month-2 active share (secondary) - 	Cards with 1+ purchase in days 31 to 60 after activation (heavy users as a subgroup)
3	Unconditional spend per activated card (Guardrail)-   Total spend divided by all activated cards, not just active ones.
- **Bad signal to watch for:** Recovery up, month-2 active share flat - Users recover the single payment but do not return.  	 Recovery up, USE ANOTHER PAYMENT METHOD clicks high	 - Users recover with a competitor’s method, not the card.	  Declines per card rising	- Users are looping through retries, which fits hints that do not fix the cause.	  Push disable rate up-  The decline push is perceived as noise.
- **Likely post-launch decision:** Iterate:  Exposure is low (about 40 declines a month, derived), the effect is diluted, and the first readout is more likely to be under-powered than conclusive. Expect an inconclusive primary with “other” share and copy as the main lever.  Trigger for iterate. Recovery is positive but the 95% CI includes 0, or the “other” share exceeds [X]%, or the guardrail is inconclusive. Extend to the pre-set maximum N, improve the copy, rerun. Triggers for the other three: Double down: the CI lower bound is above 0, the point estimate is at least [X] pp, the guardrail holds and the “other” share is at most [X]%. Roll out to the full base and move to the M tier. Pivot: recovery rises but month-2 active share does not move, so decline recovery is not the retention lever. Shift to the next friction (T-103 balance, T-104 reminders).  Deprioritize: the point estimate is 0 or below at the pre-set N, or the guardrail is breached.
- **Metrics:** Success Metrics
- **Metrics:** 1	Decline recovery rate (primary)	- Share of decline events followed by a successful card payment at the same merchant within [window]	
2	Month-2 active share (secondary) - 	Cards with 1+ purchase in days 31 to 60 after activation (heavy users as a subgroup)
3	Unconditional spend per activated card (Guardrail)-   Total spend divided by all activated cards, not just active ones.
- **Bad signal to watch for:** Recovery up, month-2 active share flat - Users recover the single payment but do not return.  	 Recovery up, USE ANOTHER PAYMENT METHOD clicks high	 - Users recover with a competitor’s method, not the card.	  Declines per card rising	- Users are looping through retries, which fits hints that do not fix the cause.	  Push disable rate up-  The decline push is perceived as noise.

### Slide 10 · Story
- **Friction + aha:** Friction points:

Some undefined numbers for some cases.
Wrong baseline - the baselines (51.0% and 57.1%) cover all users, but my hypothesis targets heavy users. The heavy share and the heavy baseline were not in the data pack.
Back and forth on the feature to choose for the test. (not happy with it, but the main feature of value was not a quick win, aka a NOW feature).

AHA moment - the feature has a built-in trigger, the decline event, and declines are logged in both arms. That makes the decline event the right unit of analysis. It points to decline recovery as the primary metric and puts month-2 active share second. It also makes the product itself the channel (the decline push), which is why the launch is an S-tier release and not a campaign.
- **Takeaways / next:** AI has been extremely helpful not only in a quick creation of artifacts, but also in bouncing off ideas, so I will continue to enhance my literacy to make it my co-pilot for future product ideas and team empowerment overall.

---

Submitted to the Product Management Certification learning platform · Product School.
