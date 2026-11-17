# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Decline reason and retry hint
- **My finalized Must-Haves (after overriding the AI):** - Every decline shows a plain-language reason in the app. Without it the user cannot tell why it failed (T-101, N-06). It needs a fallback reason (“other”), so no decline stays silent.
- One retry hint per reason. It tells the user what to do next with the card. A reason alone leaves them stuck at the till.
- Covers both in-store and online declines. In-store: 8.7% decline rate in Month 4, about 18 declines on 206 attempts. Online: about 22 declines in Month 4 (derived), so an in-store-only fix misses more than half.
- Push notification at the time of decline. The user is at the till and not in the app. T-108 shows late pushes make users assume failure and pay with another card.
German copy
- Merchant-facing decline details.
- **What I demoted from Must → Should/Won’t, and why:** Demoted: customers seeing their credit score as a hint - this is sensitive risk information that we do not divulge, we can only vaguely explain the reason.

Also moved merchant-facing decline response to must-haves, as it is a P1 request by merchants normally,

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** This PRD makes explicit that the decline-rate guardrail has no headroom (3.5% in Month 4), so retries must be defined as in or out of the rate before build, and that B1 explains declines rather than reducing them.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** I did not have to update anything
- **My prototype: save Claude's HTML as prototype.html in 04-roadmap/, open it in your browser, and add a screenshot:** _(not filled in)_
