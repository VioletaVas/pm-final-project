# GTM Launch Plan, Riverty BU Pay & Credit, First Consumer Card

| Field | Value |
|---|---|
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
