---
name: design-study
description: Design a new Conveo study and its interview guide. Use when the user wants to set up, draft, or plan a qualitative study, interview guide, or discussion guide in Conveo, or turn a research brief into interview questions.
---

To design a study in Conveo:

1. Get the brief first. If the user hasn't said, ask for the research question, the audience, and roughly how long the interview should be. Don't ask about anything you can sensibly default.
2. Create the study with `create_study`. Put the brief in `context` so Conveo's AI interviewer understands the goal. Default the tone to neutral.
3. Build the interview guide with `add_section` and `add_question`. Aim for 3 to 5 sections that move from broad context to specifics. Prefer open-ended questions; the AI interviewer probes on them. Use multiple choice only for facts you will want to segment by later (for example usage frequency or plan type).
4. Add 2 to 4 research objectives with `add_research_objective`. On section-based studies these are the analytical layer the insights are organized around, so phrase each as a question the study must answer.
5. Read the study back with `get_study` and summarize the structure for the user: sections, question count, and objectives. Point them to the study editor in Conveo to review it before launch.

Don't launch recruitment or change study settings unless the user asks. `chat_with_setup_assistant` edits the study in place and accepts every change it makes, so use it only on a draft the user has said you may change.
