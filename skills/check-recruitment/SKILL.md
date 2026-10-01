---
name: check-recruitment
description: Check fieldwork and recruitment health for Conveo studies. Use when the user asks how recruitment, fieldwork, quotas, completes, incidence, or screeners are going, or why a study isn't filling.
---

To report on recruitment:

1. If the user didn't name a study, call `list_studies` and ask which one they mean, or cover all active studies if they asked for an overview.
2. Call `get_recruitment_overview` for each study. It returns interview counts by status, the incidence rate, the screener breakdown, disqualification reasons, and quota targets.
3. Lead with the answer: completes against target, and whether the study is on track.
4. Then flag problems, most serious first:
   - quota groups that are far behind their target, or already full;
   - a low incidence rate;
   - a screener option that disqualifies an unusually large share of people (often a sign the screener is stricter than intended).
5. If the user asks about interview quality, use `list_interviews` with its quality and fraud filters, and report counts rather than listing every interview.

Keep it short: a few lines per study, with a table only when you are comparing several studies.
