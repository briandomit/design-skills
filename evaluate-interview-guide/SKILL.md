---
name: evaluate-interview-guide
description: Analyze a discovery or generative interview guide and return inline edit recommendations. Evaluates against 7 dimensions: purpose clarity, open-ended questions, non-leading questions, use of stories and examples, avoidance of hypotheticals, avoidance of solution-seeking, and past-behavior focus. Use when the user shares an interview guide (pasted text, Word file, Excel file, or Confluence link) and wants feedback before running fieldwork. Also triggers on: 'check my interview guide', 'review my discussion guide', 'is this a good interview guide', 'fix my interview questions'. To generate a new interview guide from scratch, use the research skill first.
---

# Interview Guide Analysis

Analyzes a discovery or generative **interview guide** (not a usability test script) and returns **inline edit recommendations**: for each issue, the original question/section, the dimension violated, and a suggested rewrite. No code; Markdown/text only. Researcher remains responsible for final edits.

**Confidentiality:** Analyze only the guide and optional research objectives. Do not include real participant data or PII.

---

## How to use

1. **Provide the guide** in one of these ways:
   - Paste the guide text into the chat, or
   - Attach a Word (`.docx`), Excel (`.xlsx`), or text (`.txt`) file, or
   - Paste a link to a Confluence page (or to the Word/Excel doc if your environment supports it).
2. **Optional:** Add a line or two on "What we're trying to learn" or research objectives so the analysis can check purpose and alignment.
3. **Ask for analysis** — e.g. "Analyze this interview guide" or "Run the interview guide analysis."
4. **Use the output** — Inline recommendations give you the original line, the issue, and a suggested rewrite; apply edits in your guide. You can ask for clarification or alternative rewrites in chat, or narrow scope (e.g. "only the screening section").

**As a skill:** Invoke the *interview-guide-analysis* skill and then provide the guide (paste, attach, or link). Same steps as above.

---

## Getting the guide content

The user may provide the guide in any of these ways:

- **Pasted text** — Use the content directly.
- **Attached file** — Word (`.docx`), Excel (`.xlsx`), or text (`.txt`). Read the file contents and analyze the text (for binary formats, use whatever text representation is available from the attachment).
- **Link** — Confluence: user pastes the page URL. Fetch the page with `read_document` (e.g. Glean MCP) when the URL is an internal Confluence link; if fetching is not possible, ask the user to paste the page content. Word/Excel: user may paste a link to the document; fetch if the environment supports it, otherwise ask for attachment or pasted content.

If the user provides a short "What we're trying to learn" or "Research objectives" blurb, use it to check purpose clarity and alignment.

---

## Analysis dimensions

Evaluate the guide against these seven dimensions. For each violation, produce an **inline** recommendation (see Output format below).

| # | Dimension | Check for | Flag and suggest |
|---|-----------|-----------|-------------------|
| 1 | **Purpose clarity** | Is it clear what the team is trying to learn? Is the purpose stated (e.g. intro or research objectives)? | Missing or vague purpose → suggest adding or tightening a "What we're trying to learn" statement. |
| 2 | **Open-ended + follow-ups** | Open-ended questions? Planned follow-ups (e.g. "Tell me more," "Can you give an example?")? | Closed or leading questions; missing follow-ups → suggest open-ended rewrites and follow-up prompts. |
| 3 | **No leading questions** | Does wording suggest a "right" answer or steer the participant? | Leading phrasing → suggest neutral alternatives. |
| 4 | **Stories and examples** | Does the guide ask for specific stories, situations, or examples (not just opinions)? | Opinion-only prompts → suggest asking for a recent time, a specific example, or a concrete situation. |
| 5 | **Avoid hypotheticals / future** | "What would you do if…?" "How would you react when…?" Asking them to predict future behavior? | Hypothetical or future-prediction questions → suggest reframing to past behavior or current context. |
| 6 | **Avoid solution-seeking** | Does the guide ask the participant to solve problems, design features, or suggest fixes? | Questions that ask participants to solve their own problems → suggest shifting to current behavior, pain points, and context. |
| 7 | **Past behavior over opinions** | Does the guide prioritize what people actually did over what they think or prefer? | Opinion-focused questions where behavior would be more reliable → suggest "Tell me about the last time…" or "Walk me through what you did when…". |

---

## Output format

1. **Inline recommendations**  
   For each issue, output in order of appearance in the guide:
   - **Original** — Quote or clearly reference the question/section (e.g. section title + first few words).
   - **Issue** — Which dimension (e.g. "Leading question," "Hypothetical") and a one-line explanation.
   - **Suggested rewrite** — Edit-ready wording the researcher can drop in or adapt.

   **Rule for suggested rewrites:** Every rewrite must ask about **past experience / a specific instance** (e.g. "the last time you…," "walk me through what you did when…"). Never suggest wording that asks "how do you generally…," "what's your usual approach…," "what would you…," or "how would you…" — those are hypothetical or general-behavior asks, not past-behavior. If the original is leading or hypothetical, the rewrite must still anchor in a concrete moment or past action.

   Keep each recommendation grouped (original → issue → rewrite) so it's easy to edit in place.

2. **Summary**  
   A short paragraph: 2–3 strengths and 2–3 main gaps (e.g. "Strong on stories and examples; add a purpose statement and replace three hypotheticals with past-behavior questions.").

Do not add scores or grades. Focus on actionable edits.

**Example 1 (hypothetical → past behavior):**

> **Original:** "Would you use a feature that let you compare bids side by side?"
> **Issue:** Hypothetical / future anticipation — asks them to predict future behavior.
> **Suggested rewrite:** "Tell me about the last time you had to compare two or more bids. What did you do, and what was frustrating or helpful?"

**Example 2 (leading / general behavior → past behavior):**

> **Original:** "If not, how do you know you're not missing out on valuable projects?"
> **Issue:** Leading question — assumes they might be "missing out"; also asks how they *generally* decide, not what they *did*.
> **Suggested rewrite:** "Think about one of the times you didn't look at every project. What did you do that time to decide which ones to skip or how many to look at? Walk me through that."

---

## Optional: scope or follow-ups

If the user asks to focus on part of the guide (e.g. "only the screening section") or to ignore a section, apply the analysis only to the in-scope parts and say what was excluded.

In chat, the user can ask for clarification on any recommendation or request alternative rewrites.

---

## Reference

Full spec: [interview-guide-agent-spec.md](interview-guide-agent-spec.md) in this folder.


---

## Cross-Skill Note

This skill evaluates existing interview guides. To **generate** a new discovery interview guide or usability test script from scratch, use the `research` skill first — then bring the output here for a quality check before fieldwork.
