# Hackathon #1 Reflection — Apex Innovators

**Problem Statement 10, Domain E: Secure, Deployable AI Tooling | Score: 84/100**

Our biggest technical hurdle was building a trustworthy data-quality gate under real time pressure, without a confirmed KPC dataset to validate against. We didn't know in advance which anomalies would show up in a real operational feed, so our rules risked being too loose to catch genuine problems or too strict to pass legitimate data. We resolved it by pulling a representative pilot feed ourselves, writing explicit, testable range checks for each field, and adding automated tests around every rule before wiring them into the pipeline — so we could prove the gate worked (500 rows in, four flagged, zero silently dropped) instead of just claiming it did.

Time constraint compounded this: with only days to ship ingest, clean-and-validate, anonymize, and CI, we had little slack left to polish the pitch narrative, which shows in the judges' feedback on pacing and demo depth. Uneven contribution made it worse — build work concentrated on fewer people than planned, which compressed testing and rehearsal time.

Next hackathon, we'd agree explicit ownership and daily check-ins on day one, not just a task list, and rehearse the demo as a full user workflow early enough to trim it, rather than finishing the build and the pitch at the same time.
