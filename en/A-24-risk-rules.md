---
lang: en
title: Appendix A — 24 Behavioural-Finance Risk Rules (Paste Into an Agent)
description: The full 24-rule behavioural-finance risk pipeline in four modules — sentiment identification, entry gates, exit and position control, tail risk and emotional reset. Each with its mechanism and confidence tag.
keywords: behavioral finance rules, trading risk checklist, trading discipline rules, stop loss rules, revenge trading, probability weighting, agent prompt risk module
alternates:
  en: /en/A-24-risk-rules.html
  zh-CN: /docs/A-附录A-24条行为金融风控规则.md
---

> [📚 Index](README.md) · [⬅️ Previous](14-behavioral-audit-agent-filter.md) · [Next ➡️](B-method-boundary.md)
> 🇨🇳 [Chinese full version of this appendix](../docs/A-附录A-24条行为金融风控规则.md)

# 🧾 Appendix A: 24 Behavioural-Finance Risk Rules

> **How to use this appendix**
> These 24 rules are the finished deliverable of the whole archive — four modules arranged in trading-decision order: read sentiment → entry gate → exit control → tail & emotional reset.
> **Every rule carries a confidence tag** — that tag comes from the source dialogue and measures **how solid the behavioural-economics mechanism is**, not whether the rule makes money.
> ⚠️ **Disclaimer:** a **personal decision-training record**, not investment advice. Logic-derived only, **never backtested** (see the [methodology boundary](B-method-boundary.md)).

### Module 1: Sentiment Identification & Liquidity Pricing (Rules 1–6)

| # | Rule | Mechanism | Conf. |
| :--: | :--- | :--- | :--: |
| 1 | **Break the marginal herding signal** | When non-professionals or the mainstream start discussing a specific asset at high frequency, treat it as the marginal-liquidity premium being exhausted — **no chasing longs** | Informational cascade: marginal buying is exhausted, no incremental capital remains, fragility peaks | High |
| 2 | **Availability discount** | Any buy thesis sourced from recent high-density headlines or social feeds gets a **mandatory 30% haircut** on expected future returns | Availability heuristic: heavily reported news is a lagging indicator; price already reflects the known | High |
| 3 | **Narrative-bubble & animal-spirits quarantine** | When valuation detaches from cash-flow or supply-demand models and runs on "new paradigm / grand narrative" — **no long-term heavy positions** | Keynes's animal spirits & narrative economics: sentiment-driven assets lack margin of safety; pricing power collapses on any liquidity tightening | High |
| 4 | **Capitulation catch** | Left-side staged accumulation is permitted **only** when "involuntary indiscriminate liquidation" appears (mass margin calls, liquidation cascades) | Loss aversion's extreme point: forced selling prices assets far below intrinsic value, forming a liquidity-vacuum bottom | Med |
| 5 | **One-sided consensus = short signal** | When analysts and participants form a fully aligned bullish consensus, treat it as an extreme risk alarm — **raise hedge ratio mandatorily** | Confirmation bias & groupthink: all short ammunition is already long; error tolerance is zero | High |
| 6 | **Hard intraday-volatility block** | When volatility (VIX or live ATR) breaches the alert line, **all manual entries and adjustments are forbidden** | Hot-cold empathy gap: extreme sessions light up the limbic system; the prefrontal cortex fails; expected value of decisions is negative | High |

### Module 2: Entry Gates & Position Discipline (Rules 7–13)

| # | Rule | Mechanism | Conf. |
| :--: | :--- | :--- | :--: |
| 7 | **Erase historical highs and cost anchors** | "Down X% from the high" is **never** a reason to buy; reprice only from current fundamentals and discount rates | Anchoring & adjustment: a big drawdown isn't safety; historical prices don't bind future cash flows | High |
| 8 | **24-hour cooling for unplanned trades** | Any buy idea not in the prior session's plan must cool for 24 hours before execution | System 1 → System 2 conversion: man-made friction cuts the dopamine-driven impulse order | High |
| 9 | **Mandatory premortem** | Before entry, list 3 concrete catalysts that would produce "−50% in 6 months"; **if you can't, you don't open the position** | Overconfidence & optimism bias (premortem, Gary Klein): pre-building failure scenarios pierces confirmation bias and exposes unpriced left-tail risk | Med |
| 10 | **Break mental-accounting segregation** | Unrealized profits, windfalls and small amounts use the **exact same risk-pricing formula** as core capital; "playing with profits" is banned | Mental accounting: money is fungible; loosening side accounts erodes the compound geometric return | High |
| 11 | **No subjective "it feels bottomed" left-side picks** | Entries must be triggered by explicit quantitative conditions or structural-change signals — **zero prediction-based bottom guessing** | Affect heuristic (Slovic): intuition of "cheapness" replaces expected-value computation and burns liquidity early | High |
| 12 | **Absolute averaging-down ban** | When a position is underwater, no adds to lower the average price outside a pre-planned left-side grid | Escalation of commitment & loss aversion: averaging down is a gambler's refusal to admit error; it multiplies blow-up risk geometrically | High |
| 13 | **No entry while the bear case stands unrebutted** | Before entry, extract the market's strongest short thesis and produce a data-backed rebuttal; **fail → no entry** | Confirmation bias (Wason): trading is zero-sum exchange; if you don't know the other side's logic, you *are* the liquidity provider | Med |

### Module 3: Exit Gates, Risk Control & Position Management (Rules 14–20)

| # | Rule | Mechanism | Conf. |
| :--: | :--- | :--- | :--: |
| 14 | **Bind the hard stop at entry** | The instant the entry order goes out, the system sets an automated conditional stop — **manual intraday cancellation forbidden** | Precommitment: lock maximum acceptable risk in the cold state; block hot-state wishful thinking | High |
| 15 | **Reverse the disposition effect: cut weak, keep strong** | Rebalancing must **first** remove losers that underperform the benchmark; selling strong trend leaders to "lock in book profits" is banned | Disposition effect: natural risk aversion in gains and risk seeking in losses — this rule forcibly corrects it | High |
| 16 | **Ladder scaling against the endowment effect** | After profit targets are hit, scale out in steps and raise the protective stop above cost — **let the winners run** | Endowment effect: over-treasuring owned gains triggers "giveback anxiety"; laddering provides psychological buffering | Med |
| 17 | **Daily zero-based question on every holding** | Pre-market: "If I held the equivalent cash today, would I buy this position at the current price?" **No → reduce or exit at market** | Status-quo bias & sunk cost: holding and buying at current price are the identical opportunity cost | High |
| 18 | **Account-level drawdown circuit breaker** | When total NAV drawdown in a cycle hits the red line (e.g. 10%), **flatten or lock all positions and stop live trading for at least 7 sessions** | Gambler's fallacy & win-back mindset: after major drawdowns traders take extreme risk to recover; the breaker resets the nervous system | High |
| 19 | **Attribution audit on every closed trade** | Every closed trade, win or lose, must be tagged: from the "standing system (System 2)" or an "intraday impulse (System 1)" | Self-serving bias: wins attributed to skill, losses to luck; the audit reveals the long-run true expected value | High |
| 20 | **Treat the stop as cost of goods** | Book every stop as a normal operating expense of the business — **not as a failure of intelligence or judgment** | Prospect-theory loss reframing: removes the ego damage of losses and keeps system execution consistent | High |

### Module 4: Extreme Probabilities & Game Failures (Rules 21–24)

| # | Rule | Mechanism | Conf. |
| :--: | :--- | :--- | :--: |
| 21 | **No naked far-OTM insurance** | Don't chase deep-OTM puts at panic-level IV; for downside protection use **vertical spreads that sell further-OTM legs to offset the small-probability premium**, or hard position limits on spot | Probability weighting function: humans systematically overweight tiny probabilities; paying elevated implied vol for far-OTM contracts is deeply negative EV | High |
| 22 | **Accumulate on the high-win-rate edge** | Focus resources on **repeated games with 60–75% win rates and positive expected value**; never allocate core capital to "100x" small-probability narratives | Probability weighting function: mid-to-high probabilities get subjectively discounted while small-probability jackpots get overweighted | High |
| 23 | **Erase anthropomorphic moral judgments** | The market has no "fairness," "morality," or "malicious manipulation." Price is the objective result of marginal matching. **Any resistance position justified by "the whales are rigging it" or "fundamentals don't deserve this price" is banned** | Social preference & altruistic punishment: unfair treatment fires the disgust center and produces self-destructive punish-at-any-cost decisions | High |
| 24 | **48-hour isolation after a stop-out** | A stop-out puts the instrument on an **automatic 48-hour no-entry blacklist**; same-day reversal or re-entry on the same instrument is forbidden | Revenge trading: physically blocks the "irrational win-back" and the spite reversal | High |

### Four-module structure

| Module | Rules | Problem solved | System intervention layer |
| :--- | :--- | :--- | :--- |
| **1. Sentiment identification** | 1–6 | Herding, news noise, consensus-stampede | Information filter |
| **2. Entry gates** | 7–13 | Cost anchoring, overconfidence, blind averaging | Entry gatekeeper |
| **3. Exit & position control** | 14–20 | Disposition effect, sunk cost, drawdown chasing | Automated position execution |
| **4. Extreme probability & games** | 21–24 | OTM premium traps, revenge trading, fairness bias | Tail risk & emotional reset |

> **Version note:** the source first produced a 20-rule version, then — after adding the probability-weighting function and social-preference modules — expanded to 24. **This appendix carries the final 24-rule version.** The Chinese edition also carries the full two-dimension expert review of rules 1–13 (theoretical mechanism × market micro logic); rules 14–24 lack the independent market-micro column — a known gap, see the [boundary page](B-method-boundary.md).
