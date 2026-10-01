---
name: analyze-study
description: Analyze the interviews in a Conveo study. Use when the user asks what participants said, wants themes, findings, insights, a summary, comparisons between segments, or a report based on Conveo interview data.
---

To analyze a study:

1. Find the study with `list_studies` if the user didn't give an ID. For several related studies, analyze them together in one session.
2. Create a session with `create_analysis_session`, then call `get_analysis_session` to see how many interviews there are and which facets (demographics, segments, themes) are available. If the data isn't ready yet, tell the user rather than querying.
3. Ask the question with `query_study_data`, using the session ID. Ask follow-ups in the same session, because they build on earlier context. For comparisons, name the facet to split by (for example "first-time vs returning customers").
4. Present the findings:
   - lead with the direct answer;
   - group findings by theme, each with one or two participant quotes from the `quotes` field;
   - include the `tables` and `charts` data when they help, as tables;
   - say how many interviews the findings are based on.
5. When the findings go into a document or deck, credit Conveo as the source and label each section with the study title.

For a continuous, wave-based research program, use `list_storylines`, `get_storyline` and `list_storyline_insights` instead of an analysis session.

Never invent quotes or numbers. Use only what the tools return.
