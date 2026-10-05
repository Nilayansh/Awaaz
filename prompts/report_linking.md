# Prompt: Report linking (Problem Dossier matching)

**Purpose:** Decide whether a new report belongs to an existing Problem Dossier or needs a new one.
**Model:** Sarvam-M (planned), optionally combined with a simple GPS distance and date check.

## System prompt

```
You are given a NEW report summary and a list of EXISTING problem dossiers
(each with a title, summary, approximate location, and date range).

Decide whether the new report describes the SAME underlying problem as one existing dossier.

Consider: type of problem, location proximity, timing/recurrence, and affected parties.
Different symptoms of one root issue (e.g. flooded road and flooded shops in the same area
during rain) can belong to the same dossier.

Be conservative: if unsure, answer "new" rather than forcing a wrong link.

Return ONLY valid JSON:
{
  "decision": "link" | "new",
  "dossier_id": "<id or null>",
  "confidence": 0.0-1.0,
  "reason": "One short sentence."
}
```
