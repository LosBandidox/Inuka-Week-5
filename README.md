# Week 5 — Operational Diagnostics Report & Stakeholder Defense

**Student:** David Muthui
**Assignment:** Week 5 — Operational Diagnostics Report & Stakeholder Defense (Oil & Gas Pod)

This repository contains the required deliverables for Week 5, Parts A, B, C, and D.

## Deliverables

| # | Requirement | File | Description |
|---|---|---|---|
| 1 | **Part A — Jupyter Notebook** | [`week5_diagnostics_analysis.ipynb`](./week5_diagnostics_analysis.ipynb) | Full diagnostics investigation on the Nairobi Bottleneck: univariate/bivariate profiling, anomaly detection (IQR + time-series), root-cause drill-down by time and machine, Pareto analysis, and correlation analysis ruling out temperature/voltage as drivers. |
| 2 | **Part B — Diagnostics Report (PDF)** | [`Week5_Diagnostics_Report_DavidMuthui.pdf`](./Week5_Diagnostics_Report_DavidMuthui.pdf) | 7-page written report for an Operations Director: context, root cause (pump NBI-P03, 34.4% depot throughput loss), supporting charts, and a concrete maintenance-intervention recommendation. |
| 3 | **Part B — Video Presentation** | [`Week5_Presentation_DavidMuthui.mp4`](./Week5_Presentation_DavidMuthui.mp4) | 5-7 minute stakeholder presentation of the findings above, including a simulated skeptical-director Q&A segment. |
| 4 | **Part C — Pod Feedback** | [`pod_feedback.md`](./pod_feedback.md) | Summary of the skeptical-director question received during the pod role-play (challenging the single-cause Pareto result) and how the argument was strengthened afterward using independent time- and machine-level evidence. |
| 5 | **Part D — Hackathon Reflection** | [`hackathon_reflection.md`](./hackathon_reflection.md) | 200-word reflection on Hackathon #1 (Team Apex Innovators, Problem 10): the data-quality-gate validation challenge, how it was resolved, and teamwork changes for next time. |

## Supporting data

- [`Mystery_Ops.csv`](./Mystery_Ops.csv) — the dataset used in `week5_diagnostics_analysis.ipynb`.

## How to run the notebook

```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook week5_diagnostics_analysis.ipynb
```
