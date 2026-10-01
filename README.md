# Conveo for Claude

![Conveo](assets/icon.png)

[Conveo](https://conveo.ai) is an AI-native qualitative research platform: it runs AI-moderated video interviews at scale and turns them into evidence-backed insights. This plugin connects Claude to your Conveo workspace and teaches it the research workflows that make the connection useful.

## What's included

- **Conveo connector**: the remote MCP server at `https://app.conveo.ai/api/mcp`. You sign in with your Conveo account through OAuth; no API key is stored in the plugin.
- **Skills** that tell Claude how to use the connector well:
  - `design-study`: draft a study and its interview guide (sections, questions, research objectives) from a research brief.
  - `check-recruitment`: report fieldwork health against quotas, and flag screener questions that disqualify too many people.
  - `analyze-study`: answer questions across a study's interviews with themes, tables and cited participant quotes.
  - `find-quotes`: find verbatim quotes and video clips that support a finding, and prepare them for download.

## Use it

Install the plugin, then connect Conveo from the plugin's **Connectors** tab and sign in. Then ask, for example:

- "List my active studies and summarize how recruitment is going against the quotas for each one."
- "Draft a 20-minute study exploring why people cancel meal-kit subscriptions."
- "In my Onboarding Friction study, what are the top three reasons people dropped off? Back each one with quotes."
- "Find clips where participants say price is a barrier, and get me downloadable videos of the best five."

Claude can only see studies your Conveo account can see, and every change it makes (for example creating a study or editing questions) is made as you and shows up in Conveo's study editor.

## Data

The plugin has no code of its own. It sends nothing anywhere except through the Conveo connector. That connector sends your requests (study IDs, the questions you ask, and the edits you approve) to Conveo at `app.conveo.ai`, and returns study content, interview transcripts, participant quotes and video links from your workspace. Conveo processes this data under its [privacy policy](https://conveo.ai/privacy-policy). The plugin stores nothing on your machine.

## Support

- Documentation: https://conveo.ai/docs/api-reference/mcp
- Privacy policy: https://conveo.ai/privacy-policy
- Terms of service: https://conveo.ai/terms-of-service
- Contact: support@conveo.ai
