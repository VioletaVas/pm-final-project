# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Assumption to validate #1:** Consumers want BNPL flexibility beyond online shopping, including everyday and in-store purchases.
- **Assumption to validate #2:** A Riverty card can offer a compelling reason to switch from Klarna, PayPal or existing bank cards.
- **Assumption to validate #3:** Consumers like Lena experience meaningful friction because BNPL is only available at participating merchants.
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** The user is declined when attempting a txn with the Riverty card, and the app does not say why. Hence the customer went back to debit card the same week.
- **Moment of misery / red flag #2:** Split balances and due dates	- multiple screens, multiple due dates, double reminders, no unified view of what the customer is to pay.
- **Moment of misery / red flag #3:** Identity check asks for a document photo again after a failed upload. Some applicants give up at this step.
- **Product Health & Insights Summary (Claude's output):** Executive Summary

Demand signals are healthy: 93.3% of completed identity checks were approved, and heavy BNPL users activate at 82.6%. Stability gaps at the moments of payment (declines, late notifications, wallet setup) erode that goodwill, and 143 of 431 activated cards never reached the phone wallet. Retention softens by month 2 (51-57% active), while split balances, mismatched due dates and a thin value proposition against existing habits leave the card without a clear reason to stay in use.

Thematic Synthesis
1. Technical Stability

Failures cluster at the point of payment and activation. Users get no explanation when a payment fails, and delayed confirmations push them to pay twice.

Critical: In-store declines with no reason shown (T-101). 48 logged; in-store decline rate 8.7% in Month 4 vs 2.7-3.5% overall. One participant (N-06) returned to their debit card within a week.
Critical: Wallet add fails or is abandoned (T-102). 143 activated cards never reached the wallet (66.8% did). In-store tap use depends on this.
High: Purchase push notifications arrive minutes late, so users assume failure and pay again with another card (T-108).
2. Onboarding & Activation

Funnel loss concentrates after approval, not before it. Applying and approval convert well; activation is the largest controllable leak.

High: Approved to activated 73.5% (155 approved people did not activate). Only 21.1% of invitees made 3+ purchases in the activation month.
High: Application rate 59.7% of invited.
Medium: Identity check re-requests a document photo after a failed upload, and some applicants give up (T-106). Completion was 87.7%.
Medium: Activation varies by BNPL intensity: heavy 82.6%, regular 74.7%, light 62.0%.
3. Trust & Clarity

Users cannot form a single, reliable picture of what they owe or why the product behaves as it does.

High: Card balance and regular pay later orders sit on separate screens; users ask which total is real (T-103, N-07).
High: Statement and pay later due dates differ, producing two reminders in one week for different amounts (T-104).
Medium: Instalment option appears post-purchase for some categories only; users read it as random (T-105). Instalments are 17.4% of purchases.
Medium: Credit-score impact is unanswered and no help article exists (T-107). Light users react negatively to credit/interest framing (N-05).
4. Value Proposition & Engagement

Heavy BNPL users show strong usage; others lack a compelling reason to adopt or stay. Habit competes with the card in-store and a third app adds friction.

High: Retention decay. Month 1 cohort: 77.6% active in month 0, 51.0% in month 2. Month 3 cohort at month 1: 64.0%, below the Month 2 cohort (69.2%).
High: Merchant-side value is unclear. Enterprise: “why pick you at my checkout?” (N-08). SME interest depends on offers steering traffic to them, not to marketplaces (N-09).
Medium: Habit and app fatigue. Users default to the bank card in shops (N-03) and already carry two BNPL apps (N-02).
Medium: Cashback attracts trial; sustained use is unproven (N-12).
Medium: Usage skews to online and partner merchants (63.1% of Month 4 volume); in-store share flat at 15-18%. Heavy users show latent in-store demand (N-04).
5. Support Load

Support demand derives from the clarity and stability gaps above rather than standalone issues.

Medium: Unexplained declines, duplicate reminders, balance confusion and credit-score questions generate avoidable contact (T-101, T-103, T-104, T-107). No volume data is in the pack.
6. Evidence Quality & Operating Constraints

These caveats limit how far the findings generalize.

High: Sample bias. 53% of invitees are employees (639 of 1,200), and the pilot is mostly colleagues (N-10). Approval and repayment rates are likely overstated.
Medium: Small, uneven base. Active cards peaked at 278 and fell to 262 in Month 4; Month 4 activation cohort is 39.
Medium: Proposition changes require re-approval for pricing, credit policy and terms, which takes months (N-11).
Low: 4-month window supports no churn or lifetime-value inference. Spend extrapolation (about EUR 2,595/year) is a 12x multiple of four months.
Minor Technical Debt

Wallet-add and notification timing variance by shop, category-dependent instalment display logic, repeat document upload prompts, missing credit-score help article.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** Yes, the moments of misery were caught quite accurately.
- **Did it smooth over a critical frustration into a generic bullet point?:** No, I have not noticed any explicit changes to the critical frustration points.
- **Did the AI try to suggest features or a roadmap despite the constraints?:** No, Report omits roadmap and recommendations per constraints. Gaps flagged: no support-ticket volumes, merchant-count data (open in pack), or non-employee split of results.
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** I did not note any hallucinations.
- **Logic leak / hallucination #2:** I did not note any hallucinations.
