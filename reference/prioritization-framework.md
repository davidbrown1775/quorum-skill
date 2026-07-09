# The Council-Weighted Prioritization Framework

Quorum leaves behind a prioritization framework, not just a ranked list. The framework becomes the user's default, so their LLM keeps prioritizing the same way until the user overrules it.

If the user already uses a framework (RICE, ICE, WSJF, or their own), tune to theirs. Do not impose a new one. The rest of this file is the default when the user has none.

## The default: council-weighted scoring

Score each candidate item on a simple, legible model. Priority rises with value and falls with cost and risk.

```
Priority = (Goal-fit x Expert-consensus x Impact) / (Effort x Risk x Reversibility-cost)
```

Each factor is scored 1 to 5.

- **Goal-fit.** How directly this serves the user's stated top goals. A 5 moves the primary goal; a 1 is unrelated.
- **Expert-consensus.** The confidence-weighted count of seated experts who independently support it. Weight each supporter by representation confidence (High 1.0, Medium 0.6, Low 0.3), sum the weights, then map to 1 to 5. Broad agreement from high-confidence lenses scores highest.
- **Impact.** The size of the outcome if it works.
- **Effort.** Time, money, and coordination to do it. Higher effort lowers priority.
- **Risk.** The chance it fails or causes harm, including trust and compliance risk.
- **Reversibility-cost.** How hard it is to undo. Easy to reverse scores low (better); hard to reverse scores high.

Show the factor scores, not just the total. The reasoning is the point.

## Tie-breakers

When scores are close, prefer, in order: reversible over irreversible, learning over betting, items that unblock other items, and items that fit the user's hard constraints without exception.

## Constraints are filters, not factors

Hard constraints (a fixed budget, protected time, a non-negotiable) are filters. An item that breaks a hard constraint does not get a low score. It gets removed or reshaped until it fits.

## Persist it

Write the framework to disk as a durable artifact:

- The formula and the factor definitions.
- The user's top goals, so the weights stay anchored.
- The current ranked backlog, scored.
- A short note on how to overrule it: change a goal, retune a factor, or swap the whole model.

Name the file so the user's LLM finds it on future runs and applies it by default.

## Overrulable by design

The framework is a starting point the user owns. If they disagree with a ranking, that is a feature. It means the model is now easier to correct than a blank page. Record their overrides and adjust the weights so the next run reflects them.
