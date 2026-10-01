---
name: find-quotes
description: Find verbatim participant quotes and video clips in a Conveo study. Use when the user wants quotes, clips, soundbites, video evidence, or a showreel of what participants said about a topic.
---

To find quotes and clips:

1. Search with `search_clips`, using the study ID and a short keyword or phrase. Try two or three synonyms if the first search returns little, for example "price", "expensive" and "cost".
2. Pick the strongest quotes: specific, vivid, and on topic, from different participants. Show each one verbatim with whatever participant context is returned.
3. If the user wants video, call `prepare_snippet_download` with the quote's `messageId`. Extraction can take a moment; if the snippet isn't ready, call `get_snippet_download_status` and tell the user it's in progress rather than waiting silently.
4. For ready-made compilations, call `list_quote_reels` for the study and `download_quote_reel` for the one the user picks. Quote reels are created in Conveo, not through this plugin.

Never edit or paraphrase a quote and present it as verbatim.
