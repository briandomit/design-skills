# Usability Synthesis Reference

When the Research skill routes to usability synthesis, follow these instructions in order. This covers the full pipeline: pre-synthesis verification, section-by-section synthesis, output formatting, and publishing.

---

## Pre-Synthesis Checklist

Before synthesizing, verify all materials are present. Do not proceed with gaps.

**Required materials:**
- Research brief (research questions, goals, success criteria)
- Test script (tasks and scenarios tested)
- All participant transcripts, properly labeled:
  - Moderated: `[Name] usability test`
  - Unmoderated: `UserTesting.com test #[N]`
- Any follow-up questions: `[Name] [topic] follow-up`

**Supporting context (if available):**
- Prior research summaries (discovery synthesis, prior usability rounds)
- JTBD Canvas and Requirements Table (from design agent upstream artifacts)
- Design Rationale (which decisions were least confident)
- Prototype scope declaration (what is interactive vs. visual-only)

**Quality check before proceeding:**
- All expected sessions accounted for (expected X, have X)
- Transcripts are readable (not garbled auto-transcription)
- Participant names/IDs consistent across files
- Each research question has data from multiple participants
- Each test scenario was attempted by all participants

**Sample size assessment:**
- 3-5 participants: Enough for initial patterns
- 5-7 participants: Strong pattern confidence
- Fewer than 3: Flag as exploratory, not conclusive

---

## Synthesis Sections

Work through all 10 sections in order. Skip sections that do not apply. Do not invent data or fill gaps with assumptions.

### 1. Pattern Analysis

Identify usability issues by frequency:

- **Strong patterns (3+ participants):** [Issue] -- affects [X/Y] participants
- **Emerging patterns (2 participants):** [Issue] -- needs validation
- **One-offs (1 participant):** [Issue] -- may be edge case or trade-specific

Distinguish patterns in moderated vs. UserTesting.com sessions if behavior differs between formats.

### 2. Research Question Answers

For each research question in the brief:

```
RQ[N]: [Question from brief]

Finding: [Clear, direct answer]

Evidence:
- [Participant quote with source: name or "UserTesting #N"]
- [Observed behavior]
- Frequency: [X/Y participants]

Confidence: High / Medium / Low
```

If upstream JTBD and requirements exist, map each finding to the relevant job outcome or requirement it validates or challenges.

### 3. Task Success Analysis

For each scenario in the test script:

```
Task [N]: [Scenario name]

Success rate: X/Y completed successfully
Ease rating: [Average or qualitative summary]
Common friction: [What went wrong, who was affected]
Success factors: [What made it work when it did]
Best quote: "[Representative participant quote]"
```

### 4. Prioritized Issues

Rank by impact:

**Severity definitions:**
- Blocker: Prevents task completion
- Friction: Task completed but with difficulty
- Preference: Task completed, user suggests improvement

**User impact definitions:**
- Critical: Core workflow, all user types
- Moderate: Important workflow, some user types
- Low: Edge case or nice-to-have

Present as a prioritized list combining severity and impact. Highest priority = blocker + critical.

### 5. Positive Findings

What worked well and why. For each:

```
Feature/Design Element: [Name]
Evidence: [Quotes, behaviors, ease ratings, frequency]
Why it worked: [Root cause of success -- what to preserve]
```

### 6. Participant Segmentation

Identify differences by:
- Trade type (foodservice, telecom, low voltage, electrical, general)
- Experience level (novice vs. expert with similar tools)
- Session type (moderated vs. UserTesting.com)

Only include this section if meaningful differences exist. Do not force segmentation when all participants behaved similarly.

### 7. Key Quotes for Stakeholders

Select 5-7 quotes representing:
- Most critical usability issue
- Most impactful positive finding
- Participant mental model (revealing expectation)
- Trade-specific insight
- Surprising finding

Format: "[Quote]" -- [Participant name or UserTesting #X], [context]

### 8. Confidence Assessment

```
High confidence: [Finding] -- clear pattern across X/Y, consistent behavior
Medium confidence: [Finding] -- emerging pattern, needs validation
Low confidence: [Finding] -- conflicting signals or only 1-2 participants
Gaps needing more research: [Question] -- recommend [method]
```

### 9. Recommended Actions

**Must fix before launch** (blockers, high frequency):
1. [Action] -- [Why] -- Evidence: [Issue reference]

**Should fix soon** (friction, moderate-high frequency):
1. [Action] -- [Why] -- Evidence: [Issue reference]

**Consider for future** (preferences, low frequency, unclear signal):
1. [Action] -- [Why] -- Evidence: [Issue reference]

**Additional research needed:**
1. [Question to answer] -- [Method: more tests / different users / different scenario]

### 10. Comparison to Prior Research

If discovery synthesis or prior usability rounds exist:
- **Validated:** [What this round confirmed from prior research]
- **New insights:** [What we learned that was not in prior research]
- **Contradictions:** [Where findings differ from prior research]

If upstream JTBD and requirements exist:
- **Requirements validated:** [Which requirements passed based on observed behavior]
- **Requirements challenged:** [Which requirements failed or need revision]
- **Assumptions tested:** [Which assumptions from the assumption map were addressed]
- **New requirements surfaced:** [What emerged from testing that was not in the requirements]

---

## Output Format: Confluence Template

Structure the final synthesis using this template. This is what gets published and shared with stakeholders.

```markdown
# [Project Name] - Usability Test Synthesis: Round [N]

Date: [Month Year]
Researcher: [Name]
Participants: [X participants -- trades/roles]

## Quick Links
- [Link to prototype tested]
- [Link to research brief]
- [Link to related discovery research (if applicable)]

## Executive Summary

Research goal: [One sentence]

Key findings (top 3):
1. [Finding] -- [Brief evidence] -- Action: [What we're doing about it]
2. [Finding] -- [Brief evidence] -- Action: [What we're doing about it]
3. [Finding] -- [Brief evidence] -- Action: [What we're doing about it]

Recommendation: [Launch / Iterate / More Research] -- [Why]

## Participants

[Table or description of participants: ID, trade, role, experience level, session type]

## Research Questions and Findings

[Section 2 content: one block per research question]

## What Worked Well

[Section 5 content]

## Usability Issues

[Section 4 content, organized by priority tier]

## Key Participant Quotes

[Section 7 content]

## Task Performance

[Section 3 content: summary table or per-task blocks]

## Confidence Assessment

[Section 8 content]

## Design Implications

For next iteration:
1. [Design element] -- [Specific change based on finding]

Validated from prior research:
- [Discovery finding] -- [Usability confirmed/contradicted]

New insights:
- [What we learned that was not in prior research]

## Recommended Actions

[Section 9 content]

## Next Steps

Immediate actions:
- [Action] -- Owner: [Name] -- Due: [Date]

Follow-up research:
- [What to test] -- [Method] -- [Timeline]

## Appendix

- [Link to full session transcripts]
- [Link to individual session notes]
- Methodology: [Brief description, sample size, limitations]
```

## Labels for Confluence Discoverability

Add these labels:
- `[product-name]` (e.g., product-name)
- `usability-testing`
- `Q[X]-[YEAR]` (e.g., Q2-2026)
- `[researcher-name]`
- `[trade-type]` (if relevant)
- `research-synthesis`

---

## Common Issues

**If synthesis feels incomplete:**
- Missing participant diversity (all same trade/experience)
- Research questions too broad (need more specific sub-questions)
- Tasks in script do not map to research questions

**If synthesis has low confidence:**
- Small sample size (need more participants)
- Conflicting signals (need tie-breaker sessions)
- Unclear task instructions (participants confused about what to do)

**If synthesis does not lead to action:**
- Research questions were not decision-oriented
- Findings are interesting but not actionable
- Missing "so what?" -- what do we do with this?

Fix these in the next research round.
