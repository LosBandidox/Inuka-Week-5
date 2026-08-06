# Pod Feedback — Week 5 Diagnostics Presentation

**Presenter:** [Your Name]
**Format:** Pod meeting, findings presented from the Nairobi Bottleneck diagnostics report

## Skeptical Director Question

> "Your Pareto only has one machine in it — isn't that a trivially guaranteed 100%? What would make this analysis wrong?"

**In the moment**, I didn't have a good answer and admitted that to the group rather than bluffing one.

## How I've since strengthened the argument

Sitting with the question afterward, I think the honest answer has two parts:

1. **The critique is partly right.** With only one Nairobi machine carrying any missed-maintenance incidents, the Pareto loss calculation is mechanically guaranteed to attribute 100% of that specific loss figure to it. That's worth conceding outright rather than defending the number as if it were more meaningful than it is.

2. **But it doesn't make the root-cause conclusion circular**, because Pareto wasn't what established NBI-P03 as the cause in the first place — it only converts an already-established cause into a barrels-lost figure. The root cause itself comes from two independent, machine-agnostic checks that don't involve Pareto at all: the before/after-01-Feb time drill-down (which isolates Nairobi at the depot level, with no machine data involved), and the raw throughput gap between NBI-P03 (633 barrels) and the other three Nairobi pumps (~1,020–1,030 barrels). Pareto's real job here was sizing the loss, not proving it.

I also pushed myself to identify what *would* actually break the analysis, since that's the part I couldn't answer live: if the `missed_maintenance` flag were applied *after* throughput had already dropped (reverse causality — low output triggering the flag, rather than the flag's cause driving the drop), or if another Nairobi machine had a real, unflagged problem that the labeling simply missed, the whole approach would misattribute the cause. That's the genuine soft spot in the analysis — not the Pareto shape, but how much the conclusion leans on trusting `incident_type` as accurately and independently recorded.

## What I'd change next time

Rather than defending a number under pressure, I want to name a method's known limitation up front in the presentation itself — in this case, flagging early that a single-cause Pareto will always look like 100%, and explaining why that's still meaningful given the independent time- and machine-level evidence. That would have pre-empted the question instead of leaving me scrambling for an answer live.
