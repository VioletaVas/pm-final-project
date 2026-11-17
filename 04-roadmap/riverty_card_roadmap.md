# Feature Roadmap, Module 4 · BU Pay & Credit

**Scenario:** Riverty BU Pay & Credit, First Consumer Card

**Team:** [your assumed team size]

## Strategic anchors
- **Persona:** A heavy BNPL user who already runs two pay-later apps and wants to use the card for everyday spend, including the big weekly shop, without another app to monitor.
- **Primary metric:** Heavy-user month-2 active share, meaning cards with 1+ purchase two months after activation. Baseline is not in the pack for heavy users. The all-user figures are 51.0% (Month 1 cohort) and 57.1% (Month 2 cohort).
- **Moment of misery:** A payment reminder arrives and the user cannot tell whether its amount is the real total. Card and pay later orders sit on two screens (N-07, T-103), and two reminders for different amounts arrive in the same week (T-104). N-02: “one more thing to check before payday.
- **Guardrail:** Spend per active card at EUR 233.15 or higher (Month 4 level). Optional second guardrail: overall decline rate at or below 3.5%.

## Scoring
| Feature | Value | Effort | Quadrant | Decision | Rationale |
|---|---|---|---|---|---|
| B1 Decline reason and retry hint | 4 | 2 | Quick Win | Now | N-06 returned to debit after a silent decline, and Month 4 in-store declines were 8.7%; this protects the 3.5% decline guardrail rather than the core friction. |
| B2 Add to wallet from approval | 4 | 2 | Quick Win | Now | Fixes 143 of 431 cards missing the wallet (T-102), but the persona’s in-store share is only 12.1% and online purchases do not need the wallet. |
| B3 One balance view | 5 | 4 | Major Project | Next | Removes the “which total is real” moment (T-103, N-07) for the persona; effort is high because it combines two data sources. |
| B4 Pay now or later per purchase | 4 | 3 | Major Project | Next | Adds a choice to a persona already checking several places, and likely needs credit and terms approval (N-11). |
| B5 Partner offers in app | 2 | 4 | Time Sinker | Later | Serves the merchant side (N-09), and the pack has no data on shopper response to offers. |
| B6 Cashback on every purchase | 2 | 4 | Time Sinker | Later | N-12 says cashback drives trial, “whether I keep using it is a different question”, and it is a pricing change under N-11. |
| B7 Physical card | 1 | 4 | Time Sinker | Cut | No note or ticket asks for it, and the wallet route already covers tap-to-pay. |
| B8 One due date | 5 | 5 | Major Project | Next | Fixes the two-reminder collision (T-104) directly, but N-11 says terms changes take months to re-approve. |

## Roadmap
### NOW, this sprint
- **B1 Decline reason and retry hint**, N-06 returned to debit after a silent decline, and Month 4 in-store declines were 8.7%; this protects the 3.5% decline guardrail rather than the core friction.
- **B2 Add to wallet from approval**, Fixes 143 of 431 cards missing the wallet (T-102), but the persona’s in-store share is only 12.1% and online purchases do not need the wallet.

### NEXT, the following sprints
- **B3 One balance view**, Removes the “which total is real” moment (T-103, N-07) for the persona; effort is high because it combines two data sources.
- **B4 Pay now or later per purchase**, Adds a choice to a persona already checking several places, and likely needs credit and terms approval (N-11).
- **B8 One due date**, Fixes the two-reminder collision (T-104) directly, but N-11 says terms changes take months to re-approve.

### LATER, backlog
- **B5 Partner offers in app**, Serves the merchant side (N-09), and the pack has no data on shopper response to offers.
- **B6 Cashback on every purchase**, N-12 says cashback drives trial, “whether I keep using it is a different question”, and it is a pricing change under N-11.

### ✂ Cut List
- **B7 Physical card**, No note or ticket asks for it, and the wallet route already covers tap-to-pay.
