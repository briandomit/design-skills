# Discovery Interview Synthesis Reference

Read this file when synthesizing discovery interview results. Follow all 13 sections in order. Skip sections that do not apply to the current study. Discovery interviews are exploratory, focused on understanding current workflows, pain points, and needs, not testing a specific solution.

---

## Pre-Synthesis Checklist

Before synthesizing, verify all materials are present. Do not proceed with gaps.

**Required materials:**
- Research brief (research questions, goals, success criteria)
- Discovery interview script (question guide)
- All participant transcripts, properly labeled: `[Name] discovery interview`
- Any follow-up questions: `[Name] [topic] follow-up`

**Supporting context (if available):**
- JTBD Canvas and Assumption Map (from design agent upstream artifacts)
- Prior research summaries
- Screener data (participant background, trade, experience level)

**Quality check before proceeding:**
- All expected sessions accounted for (expected X, have X)
- Transcripts are readable (not garbled auto-transcription)
- Participant names/IDs consistent across files
- Each research question has data from multiple participants

**Sample size assessment:**
- 3-5 participants: Enough for initial patterns
- 5-7 participants: Strong pattern confidence
- Fewer than 3: Flag as exploratory, not conclusive

**Diversity check:**
- Multiple trades represented (if relevant)
- Range of experience levels (if relevant)
- Mix of workflows and contexts

---

## Synthesis Sections

Work through all 13 sections in order. Skip sections that do not apply. Do not invent data or fill gaps with assumptions.

### 1. Participant Overview

Create a table summarizing each participant: name/ID, trade, role, company size, experience level, key context.

### 2. Current State Workflow Mapping

For the main workflow discussed:

**Common workflow steps:**
```
[Step] -- [How many participants mentioned] -- [Tools used]
```

**Variations by trade:**
```
[Trade]: [Their unique approach]
```

**Workflow descriptions from participants:**
```
"[Direct quote describing their process]" -- [Participant]
```

### 3. Pain Points and Needs

Organize by frequency:

**High frequency (4+ participants):**
```
Pain point: [Description]
Impact: [How it affects their work]
Current workaround: [What they do now]
Evidence: [Quotes from X participants]
Opportunity: [What this suggests we should solve]
```

**Medium frequency (2-3 participants):**
Same structure.

**Emerging / trade-specific (1-2 participants):**
Same structure. Note which trade.

### 4. Jobs to Be Done

Extract the underlying jobs participants are trying to accomplish:

```
Job: When I [situation], I want to [motivation], so I can [expected outcome]
Mentioned by: [X participants]
Current solutions: [Tools/approaches they use]
Unmet needs: [What current solutions do not do]
Success criteria: [How they know it worked]
```

If an upstream JTBD Canvas exists, map these findings back to it: which jobs were validated, which were refined, and which are new.

### 5. Tool Landscape

What tools do participants currently use?

**Tool switching patterns:**
```
[Participant] switches between [Tool A] and [Tool B] for [reason]
This causes [friction/time loss]
```

### 6. Mental Models and Expectations

How do participants think about the problem space?

**Key metaphors/analogies:**
```
"[Quote]" -- [Participant] -- reveals they think of [X] as [Y]
```

**Expected behaviors:**
```
When [situation], participants expect to [action]
Based on: [their experience with similar tools/workflows]
```

**Terminology used:**
```
Participants call [thing] by these names: [list]
(Note if this differs from what we call it internally)
```

### 7. Contextual Factors

**Multi-monitor usage:**
- X/Y use multiple monitors
- Typical arrangement and reasoning

**Team collaboration patterns:**
- Solo work vs. collaborative vs. handoff to others

**Time pressures:**
- Deadline patterns mentioned
- Impact on workflow

**Other environmental factors:**
- Job site vs. office, mobile vs. desktop, internet reliability

### 8. Opportunity Prioritization

**Highest value (frequent pain + high impact + we can solve):**
```
Opportunity: [Description]
Evidence: [X/Y participants mentioned]
Impact: [Time saved / errors prevented / frustration reduced]
Feasibility: [Why we are positioned to solve this]
```

**Medium value:**
Same structure.

**Lower priority / future considerations:**
Same structure.

### 9. Quotes for Design Principles

Select quotes that should guide design decisions, organized by theme:

```
Efficiency: "[Quote about speed/time]" -- [Participant]
Accuracy: "[Quote about errors/trust]" -- [Participant]
Flexibility: "[Quote about customization/adaptation]" -- [Participant]
Integration: "[Quote about tool switching/workflow]" -- [Participant]
```

Add other principle themes based on what emerged.

### 10. Research Question Answers

For each question in the discovery brief:

```
Question: [Original question]
Answer: [What we learned]
Evidence: [Participant quotes, frequency]
Confidence: High / Medium / Low
Follow-up needed? [If unclear, what to ask next]
```

If an upstream Assumption Map exists, map each answer to the specific assumptions it validates, invalidates, or partially addresses.

### 11. Hypotheses for Testing

Based on discovery, what should we validate through design and usability testing?

```
Hypothesis: If we [proposed solution], then [user outcome], because [insight from discovery]
Test approach: [How to validate]
Success metric: [What indicates this is right]
```

### 12. Design Implications

**Must have (table stakes):**
- [Feature/capability] -- without this, tool will not be adopted

**Should have (differentiation):**
- [Feature/capability] -- this would set us apart

**Could have (delight):**
- [Feature/capability] -- would exceed expectations

If upstream requirements exist, note which requirements are supported by discovery evidence and which need revision.

### 13. Gaps and Next Steps

**What we still do not know:**
- [Question] -- need to research: [specific user type / scenario / context]

**Recommended follow-up research:**
- [Type of research] with [participants] to answer [question]

---

## Upstream Artifact Updates

When upstream JTBD and requirements artifacts exist, the synthesis must explicitly update them:

**JTBD Canvas updates:**
- Jobs validated, refined, or newly discovered
- Outcomes validated or revised
- Forces of progress (push/pull/anxiety/habit) updated with evidence
- Job map stages validated or reordered based on observed workflows

**Assumption Map updates:**
- For each assumption: validated, invalidated, partially validated, or not addressed
- New assumptions surfaced by discovery

**Requirements Table updates:**
- Requirements promoted to high confidence based on evidence
- Requirements revised based on contradicting findings
- New requirements added with discovery evidence

These mappings are part of the synthesis report, not a separate document.

---

## Output Format: Confluence Template

Structure the final synthesis using this template:

```markdown
# [Project Name] - Discovery Research Synthesis

Date: [Month Year]
Researcher: [Name]
Participants: [X participants -- trades/roles]

## Quick Links
- [Link to research brief]
- [Link to related prior research (if applicable)]

## Executive Summary

Research goal: [One sentence]

Key findings (top 3):
1. [Finding] -- [Brief evidence] -- Action: [What we're doing about it]
2. [Finding] -- [Brief evidence] -- Action: [What we're doing about it]
3. [Finding] -- [Brief evidence] -- Action: [What we're doing about it]

Recommendation: [Design / More Research / Pivot] -- [Why]

## Participants

[Table: ID, trade, role, company size, experience level]

## Research Questions and Findings

[Section 10 content: one block per research question]

## Current State Workflows

[Section 2 content: workflow steps, trade variations]

## Pain Points and Needs

[Section 3 content: organized by frequency]

## Jobs to Be Done

[Section 4 content]

## Tool Landscape

[Section 5 content]

## Mental Models and Expectations

[Section 6 content]

## Opportunity Prioritization

[Section 8 content]

## Key Participant Quotes

[Section 9 content]

## Design Implications

[Section 12 content: must have, should have, could have]

## Hypotheses for Testing

[Section 11 content]

## Gaps and Next Steps

[Section 13 content]

Immediate actions:
- [Action] -- Owner: [Name] -- Due: [Date]

Follow-up research:
- [What to investigate] -- [Method] -- [Timeline]

## Appendix

- [Link to individual session notes]
- [Link to research brief]
- Methodology: [Brief description, sample size, limitations]
```

## Labels for Confluence Discoverability

Add these labels:
- `[product-name]` (e.g., product-name)
- `discovery-research`
- `Q[X]-[YEAR]` (e.g., Q2-2026)
- `[researcher-name]`
- `[trade-type]` (if relevant)
- `research-synthesis`

---

## Common Issues

**If synthesis feels incomplete:**
- Missing participant diversity (all same trade/experience)
- Research questions too broad (need more specific sub-questions)
- Interview questions did not map to research questions

**If synthesis has low confidence:**
- Small sample size (need more participants)
- Conflicting signals (need tie-breaker sessions)
- Participants gave opinions instead of stories (interviewer may have asked hypotheticals)

**If synthesis does not lead to action:**
- Research questions were not decision-oriented
- Findings are interesting but not actionable
- Missing "so what?" -- what do we do with this?

Fix these in the next research round.
