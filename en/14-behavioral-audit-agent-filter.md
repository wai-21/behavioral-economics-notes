---
lang: en
title: The Behavioral Audit — Turning 14 Biases Into an Agent's Mandatory Filter
description: Knowing your biases is useless until they become items someone else can check. From 20 rules to 24, the bias-detection matrix, and the input contract for a decision-audit agent.
keywords: behavioral audit, cognitive bias checklist, trading agent rules, bias detection matrix, debiasing, decision filter, cool state enforcement
alternates:
  en: /en/14-behavioral-audit-agent-filter.html
  zh-CN: /docs/14-行为金融审计-24条规则-把偏差做成Agent滤网.html
---

> [📚 Index](README.md) · [⬅️ Previous](13-nudge-choice-architecture.md) · [Next ➡️](A-24-risk-rules.md)
> 🇨🇳 [Chinese full version of this topic](../docs/14-行为金融审计-24条规则-把偏差做成Agent滤网.md)

# 14. The Behavioral Audit: Turning 14 Biases Into an Agent's Mandatory Filter

> **⚡ Transferable rule:** **Turn the biases into a mandatory filter — every decision must clear four classes of bias triggers before an order can go out.** The only reliable mechanism is not "I remember" but "the process doesn't let it pass."

## 📖 What the book actually says

- **Chapter 9's corollary, applied to a person, becomes this meta-rule:** if biases are predictable, they can be **externalized** — enforced not by the actor's in-the-moment introspection, but by a fixed inspection process.
- **Why must it be externalized?** The first 13 topics prove the same four facts over and over:
  - System 2 is a consumable ([topic 10](10-hot-states-dual-systems.md)) → in-the-moment self-inspection is **physically unavailable** at certain moments;
  - Biases defend themselves ([topic 07](07-mental-accounting.md)) → you will invent a good reason from inside the bias;
  - The reference point sets your risk appetite ([topic 06](06-prospect-theory-loss-aversion.md)) → the you in the loss zone is **not** the you in the gain zone;
  - Wrong answers arrive first, with confidence ([topic 10](10-hot-states-dual-systems.md)) → **introspection cannot distinguish "thought through" from "intuition arrived."**
- **Conclusion: the audit must be done by "someone else."** A risk team, a written checklist, or an **agent that never fatigues and never goes soft on you because you lost money today.**
- **The concrete form from the source: a system prompt for a behavioural-finance decision auditor**, with a three-part structure worth copying for any "psychology engineered into software":
  1. **Bias Detection Matrix** — biases written as a three-column table: typical user utterance → underlying mechanism → intervention;
  2. **Communication protocol** — no emotional validation, mandatory friction, attribution audits;
  3. **Response scripts** for the three highest-frequency hot states, with steps written in advance.

> *"You are not a passive assistant recording positions and NAV. You are a cold auditor with a behavioural-economics nervous system. Your mission: when the user is in a hot state (greedy chasing, panic selling, loss-holding), act as mandatory friction, cut the irrational reflex, and defend the principal."* (source prompt text; confidence: high — this is material content, not the book's)

## 💡 How it rewired my decisions

- **Before:** I treated "finished the chapter" as "mastered it." Nine chapters, all quizzes correct — my self-assessment was "I can use this now."
- **After:** three pieces of evidence split "knowing" from "being able to run it":
  **① The material's own coverage confession.** Asked "is the whole book covered?", the dialogue answered with a confidence-tagged conclusion: **~85% covered; two deep modules not closed** — the **probability weighting function** (prospect theory's other half: nonlinear probability weighting) and **social preferences & game failures**. **The act of declaring the missing 15% is itself the prototype of audit discipline.**
  **② Completing that 15% grew the rules from 20 to 24** — and the four new rules map exactly onto the two gaps:

| Gap | New rule | Logic |
| :--- | :--- | :--- |
| Probability weighting | **Rule 21 — no naked far-OTM insurance** | Chasing deep-OTM puts at panic-level IV is paying the small-probability overweight premium; protection belongs in spread structures that sell further OTM to offset it |
| Probability weighting | **Rule 22 — accumulate on the high-win-rate edge** | Focus resources on repeated games with 60–75% win rates and positive EV; never allocate core capital to "100x" small-probability narratives |
| Social preference | **Rule 23 — erase anthropomorphic moral judgments** | The market has no fairness, morality or malice; price is the objective result of marginal matching |
| Social preference | **Rule 24 — 48-hour isolation after a stop-out** | Physically block the revenge-trading impulse |

  **③ The last step: putting the rules into an agent.** The bias-detection matrix as a table every request must clear:

| Bias | Typical utterance | Mechanism detected | Intervention |
| :--- | :--- | :--- | :--- |
| **Disposition effect** | "This one's up 10%, let me lock it in; that one's down 20%, I'll wait to break even" | Extreme risk aversion in gains, extreme risk seeking in losses | Interrogate whether the sell reason is "I have profits" or "the thesis broke"; force comparison of forward expected value, not realized P&L |
| **Sunk cost & escalation** | "I'm down 30% — cutting now hurts too much; let me average down" | Sunk costs priced into the present decision; gambler's enlargement of asymmetric downside | Run the zero-based question: with full cash in hand, buy at today's price? |
| **Anchoring** | "It was 100 before, 60 now — cheap" | Historical high or cost basis as the anchor; fundamentals drift ignored | Erase historical coordinates; reprice only from current balance sheet and DCF |
| **Availability & herding** | "Everyone's talking about this sector — if I don't get in now I'll miss it" | Marginal liquidity premium peaked; decision runs on recent exposure | Forced reverse argument: produce at least one solid bear case |

- **The third layer (the real landing point):** of the 24 rules, what I needed most was not the rules but **"who executes them."** Final conclusion — **the auditor must be separated from me**:
  - **Financial decisions** → agent filter + mechanical stop orders (independent of today's state);
  - **Consumption decisions** → the context-strip question + 24-hour cooling (written into a list, not memory);
  - **Habit decisions** → defaults and environmental friction (not resolve).
  **Only when all three close does the archive close:** the book explains how humans err; what I learned is **moving the checkpoints for error out of human hands.**

```text
Behavioral audit module (paste into any decision agent)

  [Input contract] For any buy/sell/adjust/large-spend request, the agent
    must receive three dimensions:
    ① Position P&L state and cost anchors (PnL%, price vs cost vs recent high)
    ② Decision reason and source class (quant signal / community heat /
       breaking news / pure hunch)
    ③ Decision latency and time state (signal-to-order interval, current vol)
    → any missing → refuse to conclude; request the data first

  [Mandatory friction] On "chasing an immediate move up" or "adding into a
    loss": no technical-indicator backing; output a cooling warning plus
    2 counter-questions first

  [Communication protocol]
    ✗ no emotional filler ("don't worry, it'll come back", "great call!")
    ✓ absolutely objective, data-driven, explicit confidence (high/med/low)
    ✓ tag every adjustment's motive: System 2 (quant/pre-set rules) or
      System 1 (intraday stimulus / refusing to accept the loss)

  [Three response scripts]
    A. Wants to hold & average down → name the mechanism → zero-based
       question → quantify the recovery math (loss vs required gain, with data)
    B. Wants to dump a strong winner → disposition effect → expected-value
       check → compromise (dynamic ladder scaling, not all-or-nothing)
    C. Impatient intraday entry → cold-state block (does this meet the
       pre-set objective entry criteria?) → premortem (name 2 catalysts that
       halve the position in 3 months)
```

## 🔗 Go deeper

- [Appendix A — 24 risk rules](A-24-risk-rules.md) — the full pipeline, four modules
- 🇨🇳 [Chinese full version](../docs/14-行为金融审计-24条规则-把偏差做成Agent滤网.md) — the 20→24 evolution and the "remaining 15%" confession in full
- Next: [Appendix A](A-24-risk-rules.md)
