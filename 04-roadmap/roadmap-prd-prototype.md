# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
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
- **Prototype/roadmap screenshot link (paste into your deliverables):** _(not filled in)_
