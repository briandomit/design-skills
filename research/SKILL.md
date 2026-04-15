---
name: research
description: Generate usability test scripts, discovery interview scripts, research briefs, session notes templates, UserTesting.com study plans (including comparison studies, screeners, demographic filters, and decision frameworks), and research synthesis. Use when the user asks to create a usability test, discovery interview, test script, research brief, moderated test plan, UserTesting.com script or study plan, preference test, comparison study, nomenclature test, screener questions, session notes template, or synthesize research findings into Confluence-ready output. Applies Carol Barnum, Steve Krug, NNGroup, Teresa Torres, IDEO, and Stanford d.school methodologies.
---

# Usability test script generation

## When to use

- User asks to create a usability test script, research plan, or test materials
- User needs to convert a prototype or design into testable scenarios
- User wants to audit an existing script against a prototype
- User asks for moderated or unmoderated (UserTesting.com) test plans
- User asks to build a UserTesting.com study plan with screeners, filters, and comparison groups
- User needs a preference test, comparison study, or nomenclature test
- User asks to create a discovery interview, discovery script, or exploratory research plan
- User needs to understand a problem space before designing a solution

## Discovery vs. usability testing: when to use which

| Signal | Use Discovery | Use Usability |
|--------|--------------|---------------|
| Do we have a prototype? | No | Yes |
| What are we learning? | Problems, needs, workflows | Whether our solution works |
| Question style | Open-ended, storytelling | Task-based, observation |
| Output | Journey maps, pain points, opportunities, JTBD refinements | Completion rates, time-on-task, severity ratings |
| Methodology | Teresa Torres, IDEO, Stanford d.school | Barnum, Krug, NNGroup |
| Typical duration | 45-60 min | 30-60 min |

**Rule of thumb:** If you're exploring a problem space, use discovery. If you're validating a solution, use usability testing.

## Research type routing: always determine first

Before asking any other clarifying questions, always determine whether the user needs discovery research or usability testing. Never assume one or the other — even if the request sounds obvious.

### Routing questions (ask these first)

1. "Do you have a prototype, design, or specific solution to test? Or are we exploring a problem space, workflow, or user need?"
2. "What's the goal — to understand how people currently do something (discovery) or to evaluate whether a design works (usability)?"

### Decision rule

- **They have a prototype/solution to evaluate** → Usability testing path → proceed to the usability clarifying questions below
- **They're exploring problems/needs/workflows with no solution yet** → Discovery path → proceed to the discovery clarifying questions below
- **Still unclear** → Ask one more question: "Are you trying to learn WHAT to build, or test something you've already designed?"

After routing is determined, proceed to the relevant clarifying questions section.

## Upstream context

Before asking clarifying questions, check whether upstream artifacts from the design agent are available. If they are, use them as starting context and only ask about what is missing or ambiguous.

**If a JTBD Canvas is available:**
- The job performer answers "who are the participants"
- The main job and desired outcomes shape your research questions
- Skip clarifying questions that are already answered

**If a Discovery Research Request is available (from the JTBD skill):**
- Research questions, target participants, known context, and decision criteria are pre-answered
- Skip routing questions (research type is discovery)
- Skip most clarifying questions -- only ask about gaps or ambiguities
- Preserve assumption references so synthesis can map back

**If an Assumption Map is available (discovery path):**
- High-impact, low-confidence assumptions become your primary research questions
- Include the assumption reference in each research question so synthesis can map back
- Skip "what do we need to learn" -- the assumption map answers it

**If JTBD + Requirements + Design Rationale + Prototype are available (usability path):**
- The JTBD outcomes shape research questions ("Can users accomplish [outcome]?")
- Low-confidence requirements become observation focus areas
- Risky assumptions from the assumption map become specific probing targets
- Least-confident design decisions (from the rationale) become risk areas
- Prototype limitations inform moderator notes
- Skip most clarifying questions -- the upstream artifacts answer them

If no upstream artifacts are available, proceed with the standard routing and clarifying questions as written.

## Workflow: always ask before generating

Before creating any research brief or test script, ALWAYS ask clarifying questions. Never assume or guess. If upstream artifacts from the design agent are available, defer to the Upstream Context section above and only ask about what is missing or ambiguous.

### Required questions (always ask)

1. **What are we testing?** Feature/product name, what it does in one sentence, new functionality or redesign?
2. **Who are the participants?** Target user type/role, experience level, trade-specific needs?
3. **What decision does this inform?** What we're trying to learn, what we'll do with findings, competing design approaches?
4. **Format needed?** Moderated, UserTesting.com, or both? Time constraint (30/45/60 min)?
5. **Current state context?** How do users do this today, what problem does this solve, what are we comparing against?

### Conditional questions (ask if relevant)

**If testing AI/automation features:**
- What does the AI do automatically?
- Can users override or correct it?
- What's the trust/accuracy concern?
- Opt-in vs opt-out default?

**If testing new workflow:**
- What's the existing workflow being replaced/improved?
- Are we measuring time savings?

**If testing multiple variations:**
- How many design approaches? What differs between them?

**If unclear what to test:**
- What are the biggest risks/unknowns?
- What would cause us not to ship this?

### Example clarifying question flow

User: "Create a usability test for our new document viewer"

AI should respond:

"Before I create the test materials, I need to clarify a few things:

1. What specifically are we testing — page navigation, markup tools, search, something else?
2. Who are the target participants — which trades, what experience level?
3. What decision does this test inform — validating before dev, choosing between approaches, finding issues to fix?
4. Format — moderated (45-60 min), UserTesting.com (30 min), or both?
5. How do users view documents today, and what problems are we solving?

Once I have these, I'll create the research brief, test script(s), and session notes template."

### When to skip questions

Only skip if the user provides ALL required information upfront in their request, or if upstream artifacts (JTBD Canvas, Assumption Map, Requirements, Design Rationale) already answer the question.

If user says "just use defaults" or "you decide," push back: "I need these specifics to create an effective test. Making assumptions about [X] could lead to testing the wrong things. Can you clarify [specific question]?"

## Methodology foundation

Based on:
- **Carol Barnum** (_Usability Testing Essentials_): Rigorous, systematic task design with clear success criteria
- **Steve Krug** (_Rocket Surgery Made Easy_): Practical, lightweight scripts that prioritize natural discovery
- **Nielsen Norman Group** (Usability Testing 101): Industry-standard question framing and facilitation principles

Reference: https://www.nngroup.com/articles/usability-testing-101/

## Output generation order

Always generate materials in this order:

1. **Research brief** — what we need to learn and how we'll decide
2. **Test script** — introduction, warm-up, scenarios, follow-up
3. **Session notes template** — structured observation capture aligned to script
4. Offer both moderated and UserTesting.com versions if relevant

## Research brief structure

Follow the research brief template in the template examples section. Key requirements:
- Research questions must be **decision-oriented**, not "learn about users"
- Success criteria must describe **what you can decide**, not just "gather feedback"
- Tie to a specific timeline or milestone

## Test script structure

Follow the usability test script template in the template examples section. Key structural requirements:

- **Introduction (2-3 min):** Introduce team, set context ("testing the design, not you"), request think-aloud, recording consent. Keep concise — don't over-explain.
- **Warm-up (5 min):** 3-5 open-ended questions on role, current workflow, tools, pain points. Never yes/no.
- **Task scenarios:** Realistic scenario → observe silently → note critical factors → probe unclear behavior → record quantitative data. See "Expert critique" section for scenario structure.
- **Follow-up (5 min):** Anchored ease rating, what's missing, comparison to current workflow, adoption barriers.
- **Wrap-up (1 min):** Thank participant, explain incentive, ask if they have questions.

## Task design rules

### Do

- **Create realistic scenarios**: Place users in a context where they'd actually use the product
- **Describe goals, not paths**: Tell them WHAT to accomplish, never HOW
- **Use active verbs**: "Find," "Set up," "Organize," "Complete"
- **Include clear success criteria**: Observable completion, not subjective
- **Request think-aloud**: Explicitly in the introduction and reinforce during tasks

### Do not

- Give navigation hints ("Try clicking the menu at the top")
- Use exact interface labels in task descriptions (this leads users to the answer)
- Create tasks that are too simple (no insight) or too complex (confusion)
- Ask users to "pretend" elaborate scenarios — keep it natural
- Make tasks that don't match the current prototype state

### Examples

Wrong: "Click the search bar and type a project name"
Right: "You need to find a project called 'Mario's Bistro.' How would you do that?"

Wrong: "Use the Create New Project button to start a project"
Right: "You just won a bid for a restaurant renovation. Set up this project so you're ready to begin work."

## Writing rich task scenarios

### Scenario structure

Every task scenario must include three components:

1. **Context/setup** — sets the stage
   - Specific date/time if relevant
   - User's current situation or need
   - Background that makes the task realistic

2. **Goal statement** — what they need to accomplish
   - Action-oriented verb (Find, Buy, Update, Compare, Book, Organize, Upload)
   - Specific constraints (budget, deadline, requirements)
   - Clear success criteria (when is the task "done"?)

3. **Realistic motivation** — why they're doing this
   - Personal or work need
   - Time pressure or deadline
   - Decision criteria

### Example scenarios by domain

**E-commerce:** "It's December 15th, and you need a birthday gift for a friend who loves photography. You want to buy a camera backpack under $100, and it needs to arrive within 5 days. Find a suitable bag and proceed to checkout to see shipping options."

**Construction contractor:** "You just won a bid for a restaurant kitchen renovation. The project starts Monday and you need to organize 47 documents from the architect — floor plans, equipment specs, electrical drawings, plumbing schedules. Upload these documents and prepare them for takeoff work."

### What makes these well-written

- Starts with scenario, not command — "You need to..." not "Click the..."
- Provides realistic context — tells a story, helps user act naturally
- Action-oriented — uses verbs: Find, Buy, Update, Compare, Book, Organize
- Avoids label-matching — doesn't use exact interface wording
- Includes necessary constraints — budget, deadline, requirements
- Defined end goal — clear when the task is finished

### Poor vs. well-written comparison

**Poor:** "Click the 'Search' button, type 'Nike,' and click the first result to buy it."
- Tells them exactly what to do
- No context or motivation
- Step-by-step instructions

**Well-written:** "You want a new pair of running shoes for under $40. Show me how you would find them."
- Describes goal, not path
- Includes constraint (budget)
- Lets user discover interface naturally

### Construction domain scenarios

When writing scenarios for construction contractors:
- Reference real project types (restaurant kitchen, office buildout, hospital wing)
- Include realistic document counts and types (47 sheets, 120-page spec book)
- Mention bid deadlines and project start dates for natural urgency
- Reference trade-specific needs (electrical load calculations, HVAC tonnage, equipment schedules)
- Use natural time pressure ("bid due tomorrow," "project starts Monday")

## Output requirements

When generating test scripts, every scenario must:
1. Follow the complete template structure (research brief → test script → notes template)
2. Include rich, contextual scenarios with all three components (context, goal, motivation)
3. Provide moderator notes for intentional prototype limitations
4. Include observation points and dig-deeper questions per scenario
5. Match the exact template format provided in the template examples section

## Question design rules

### Do

- Ask open-ended questions (how/what/why)
- Use neutral framing: "What are your impressions?" not "How did this help you?"
- Probe after tasks: "What was confusing?" / "How could this improve?" / "Why did you do that?"
- Redirect user questions: If they ask "Does this button do X?", respond "What do you expect?"

### Do not

- Ask yes/no questions (50/50 guess, no qualitative data)
- Ask leading questions: "How much did you like this?" → "What are your thoughts?"
- Answer user questions with answers — always redirect
- Use closed-ended questions that limit response

## Expert critique: Barnum and Krug principles

### Carol Barnum's rigor standards

**Measurable success criteria** — Define quantitative thresholds in the research brief:
- Task completion target: "4/5 users complete without assistance"
- Time-on-task benchmark: "Upload completes in under 2 minutes"
- Error recovery rate: "3/5 recover without moderator help"

Wrong: "Users should understand the error message"
Right: "4/5 users dismiss error and continue without assistance"

**Sample size justification** — Always state in research brief:
- Formative testing (finding problems): 5 participants sufficient
- Summative testing (validating it works): 10+ participants needed

**Anchored rating scales** — Never use bare 1-5 scales without anchors:
- Wrong: "Rate ease from 1-5"
- Right: "Compared to uploading one at a time: 1=much harder, 3=same, 5=much easier"

Always anchor to current workflow with specific definitions per number.

### Steve Krug's practical testing principles

**Behavior > Explanations** — Don't ask what they'd do. Watch what they do.
- Wrong: "Without clicking, tell me what you see" (passive)
- Right: "You have 65 documents to upload. Go ahead." (active — orientation reveals itself through action)
- Probe only when behavior is unclear, not as routine

**Let errors happen naturally** — Don't telegraph problems:
- Wrong: "It looks like not everything went through. What happened?"
- Right: Trigger the error, say nothing. Observe: Do they notice? Read it? Recover?
- Only ask "What just happened?" if stuck for 30+ seconds

**Focus on 3 critical things per scenario** — Everything else is noise:
- Completed task? Y/N
- Struggled? Where? (brief note)
- Time to complete: ___ min

Reserve detailed checklists only for error recovery, complex multi-step workflows, or safety-critical interfaces.

**Probe only unclear behavior** — Most problems are visible (hesitations, backtracking, re-reading, wrong clicks). Only probe when:
- Behavior is ambiguous (why did they skip that?)
- They succeed but look uncertain
- You need to understand their mental model

Good probes: "Talk me through what just happened" / "Why did you hesitate there?" / "I noticed you went back — what were you looking for?"
Bad probes: "What do you expect?" / "What are your thoughts?" (asking before observing)

### Applying both: balanced scenario structure

1. **Give realistic task** (Krug: let them do)
2. **Observe silently first** (Krug: behavior reveals problems)
3. **Note 3 critical factors** (Barnum: measurable — completion, time, struggle points)
4. **Probe only unclear behavior** (Krug: targeted, not routine)
5. **Record quantitative data** (Barnum: completion rate, time, anchored ease rating)

### When to use each approach

| Situation | Approach |
|-----------|----------|
| Early prototypes, iterative design | Krug's speed (find obvious problems fast) |
| Before major investment, stakeholder buy-in | Barnum's rigor (numbers required) |
| Before launch (most common) | Both — find problems + measure success |

## Facilitation rules (moderated sessions)

- **Do not talk too much.** Resist filling silence. Silence is productive.
- **Do not defend the design.** User struggles are learning opportunities.
- **Do not guide the user.** If stuck, ask "What would you expect?" not "Try clicking there."
- **Do not be overly friendly.** Brief rapport, then focus on tasks.
- **Do not ignore negative feedback.** That's the goal of the test.
- **Do not skip pilot testing.** Run through once before real sessions.
- **Leave 30 min between sessions** for cleanup, notes, delays.

## Moderator notes

Add bracketed moderator notes after questions that test intentional prototype limitations:

```markdown
**[Moderator note: [Feature] is [limitation description]. This is intentional —
capture what the user expects to happen, not what they can actually do.]**
```

Use these when:
- Prototype has non-functional elements the script asks about
- Features are visually present but don't work (tabs that don't filter, folders that don't organize)
- Intentional scope boundaries (can't switch projects from takeoff, etc.)

## Moderated vs. UserTesting.com

| Aspect | Moderated | UserTesting.com |
|--------|-----------|-----------------|
| Duration | 45-60 min | 30 min max |
| Flexibility | Adapt questions in real time | Must be crystal clear upfront |
| Probing | Follow-up based on behavior | Pre-written prompts only |
| Task clarity | Can clarify if confused | No course correction |
| Quote capture | Richer context, body language | Verbal only |
| Format | Conversational, adaptive | Structured, sequential |

When generating for **UserTesting.com**:
- Tasks must be unambiguous without moderator clarification
- Remove "prompt if needed" sections — replace with self-contained instructions
- Simplify observation checklists to what's visible in recording
- Add explicit screen-share instructions at the start
- Keep total task count lower (3-4 scenarios max)

---

## UserTesting.com Study Builder

Use this section when the user is planning an **unmoderated study on UserTesting.com** — whether it is a usability test, preference test, comprehension test, comparison study, or any other study type that runs on the platform. This section covers platform-specific mechanics that go beyond the general usability test guidance above.

### Study design principles

**Eliminate priming bias.** If the study involves comparing options (labels, layouts, flows, icons, or any two alternatives), always recommend showing a **neutral version first**. Showing a labeled or styled version first primes participants. The neutral version captures organic language and unprimed reactions before introducing either option.

**Use UserTesting's balanced comparison feature.** For within-subjects comparisons, use the **balanced comparison** feature (not two separate tests). Create Group A and Group B — UserTesting randomizes order automatically across participants. This prevents order effects without managing multiple tests.

**Keep it short.** Target **10–15 minutes**. Every question must justify its presence. Ask: does this question give us data we can't get from another question? If two questions measure the same thing, cut one.

### Participant targeting

#### Demographic filters (set in Audience Builder)

Apply filters broadly — they narrow the pool before screeners run. Over-filtering at both stages leaves too few candidates.

**Recommended filters:**
- Industry: select 1–2 relevant categories
- Job Role: select roles that consume the product's output
- Employment Status: Employed full-time
- Operating System: Mac + Windows (for desktop products)
- Country: United States (+ Canada if pool is small)
- Web Browsers: Chrome (best Figma compatibility + enables enhanced metrics)

**Skip unless relevant:** Age, Gender, Household Income, Parental Status, Company Size, Job Level, Web Expertise, Social Networks — these rarely matter and shrink the pool.

**Niche audience fallback:** If recruitment stalls after 2 days, drop demographic filters and rely on screener questions alone. The screener does the qualifying work; the filters just pre-narrow the pool.

#### Screener questions

Always include:
1. **Industry qualifier** — multiple choice, qualify/disqualify per option
2. **Tool/data usage frequency** — how often they use relevant software (qualify: daily/weekly/monthly; disqualify: rarely/never)
3. **Tool familiarity** — multi-select of relevant tools (disqualify only if "none of the above" is sole answer)

### Question types available in UserTesting

- **Website task** — shows a URL, participant interacts or observes
- **Verbal response** — participant speaks their answer (recorded)
- **Written response** — participant types their answer (good for clean quotable data points)
- **Rating scale** — use 1–5 (the UserTesting default; sufficient granularity for detecting a ≥1.0 point gap between options)
- **Multiple choice** — single or multi-select

### Task instruction character limit

UserTesting's task instruction field has a **200-character limit**. Write instructions to fit. If an instruction works across multiple groups in a balanced comparison, it must be non-sequential in language (no "first version" / "second version" references).

### Comparison study structure

Use this structure for any study comparing two or more alternatives — labels, layouts, flows, icons, or concepts. The 3-phase approach eliminates priming bias and captures both unprimed reactions and direct preferences.

**Phase 1 — Unprimed reaction (neutral stimulus)**
- Task: show a neutral or unlabeled version of the design
- Q1: Without describing the content — what type of [page/screen/element] is this? (Verbal)
- Q2: What word or label would you use to describe this? (Verbal — captures organic language)
- Q3: If you were sharing this with a colleague, what would you call it? (Verbal — sharing language)
- Q4: In one or two words, what would you call this? (Written — clean quotable data point)

> **Stimulus note:** The neutral stimulus must be abstract enough that participants think about the *type* of thing, not just the subject matter. If the stimulus shows recognizable data, participants will anchor to the content. Either use a stripped-down stimulus or add an explicit framing statement before Q1.

**Phase 2 — Balanced comparison (labeled/styled alternatives)**
- Use balanced comparison feature: Group A sees Option 1 first, Group B sees Option 2 first
- Each group: task (show alternative) → rating scale question (1–5, how well does this [label/layout/approach] work for you?)
- After both groups: forced preference (multiple choice) → reasoning (verbal) → confidence (1–5 rating, optional) → alternative suggestions (verbal)

**Phase 3 — Mental model debrief**
- One verbal question: "Is there a difference between [Option A] and [Option B] to you? What does each one mean to you?"
- One question is enough — it covers definition, distinction, and closing thoughts simultaneously.

### Analysis plan for UserTesting studies

#### Quantitative signals

| Metric | Source | Signal threshold |
|---|---|---|
| Unprompted term/preference frequency | Phase 1 verbal + written | ≥60–70% converge on one option = clear winner |
| Option-content match scores | Rating scale per option (1–5) | ≥1.0 point gap between means = meaningful |
| Forced preference split | Multiple choice | ≥70% = strong; 55–69% = moderate; 50/50 = inconclusive |
| Preference confidence | Rating scale (1–5) | Mean ≥4 = distinction matters to users |

#### Qualitative themes to code in video review

- Natural language used unprompted in Phase 1
- Mental model associations participants reveal
- Sharing framing — what word do they use when describing sending it to a colleague?
- Industry-specific norms — do they reference how their company/industry uses the term or pattern?
- Alternative suggestions — any third option that recurs across 3+ participants

### Success metrics and decision framework

**Define success before launching.** State explicitly: what result would constitute a clear recommendation? What would be inconclusive?

- **Strong signal:** ≥70% unprompted alignment in Phase 1 OR ≥70% forced preference + ≥1.0 point match score gap
- **Moderate signal:** 55–69% preference, mixed qualitative themes → go with the leaning, flag confidence level
- **Inconclusive:** 50/50 split, low confidence → document it as "no strong user preference" and make the decision on other grounds (technical, business, convention)

**Always note:** an inconclusive result is a valid answer — it means the choice won't confuse or frustrate users either way.

**Alternative suggestion protocol:** If 3+ participants independently suggest the same alternative not in the study, flag it for follow-up. Don't dismiss it.

### UserTesting study output files

For each study, produce:
1. `[StudyName]-Plan.md` — full study plan (markdown)
2. `[StudyName]-Plan.html` — Confluence storage format with panels, code blocks, collapsible screeners, status lozenges, and task-list checkboxes
3. `[StudyName]-Results.md` — results document following the same phase structure as the plan, with quantitative analysis, qualitative themes, decision framework applied, and next steps
4. `[StudyName]-Results.html` — Confluence storage format matching the plan's visual style, with status badges (Green PASS / Yellow moderate / Red FAIL), collapsible participant key, and panel macros for qualitative themes

### UserTesting setup checklist

Before launching:
- [ ] All prototype links set to "Anyone with the link can view" — test in incognito
- [ ] Pilot test run internally (verify links load, timing is accurate, questions are clear)
- [ ] Demographic filters set — not over-filtered
- [ ] Screener questions entered with correct qualify/disqualify logic
- [ ] Balanced comparison groups configured correctly (if comparison study)
- [ ] Task instructions are under 200 characters
- [ ] Screen + audio recording enabled
- [ ] First 2–3 responses monitored before full run completes

## Session notes template structure

Generate a notes template aligned to the test script with these sections:
- **Header:** Participant #, date, trade/role, facilitator
- **Warm-up summary:** Current workflow, tools, key quote
- **Per scenario:** Completed (Y/N), ease rating (1-5), observation checklist mirroring script, behavior notes (free-form), quotes
- **Follow-up responses:** One entry per follow-up question
- **Key insights:** Numbered with supporting evidence
- **Severity assessment:** Critical (🔴), Moderate (🟡), Minor (🟢)

## Domain context: construction contractors

When generating scripts for construction/takeoff products:
- Participants span trades: foodservice, telecom, low voltage, HVAC, electrical, general contracting
- **Multi-monitor workflows are standard** — takeoff on one screen, reference docs and estimate software on others
- **Document-heavy processes** — bid packages can be 1000+ pages
- **Time-sensitive** — bid deadlines drive urgency
- **Tool fragmentation** — users juggle BlueBeam, Excel, trade-specific takeoff software
- **Technical sophistication varies widely** — avoid jargon like "UI," "UX," "sprint"
- **Manual naming is the universal bottleneck** — 1.5-2 days before takeoff begins
- **AI trust is mixed** — contractors want automation but need override control and verification

## Quality checklist

Before finalizing any generated script, verify:

- [ ] Research questions are decision-oriented
- [ ] Success criteria are quantitative (X out of Y users must complete)
- [ ] Rating scales are anchored (compared to current workflow, specific definitions)
- [ ] Sample size is justified (formative 5 vs summative 10+)
- [ ] Tasks start with action, not passive observation
- [ ] Scenarios let users discover naturally (no telegraphing errors)
- [ ] Observation notes focus on 3 critical things per scenario
- [ ] Probes are reserved for unclear behavior (not routine)
- [ ] Moderator notes explain when to stay silent vs. when to probe
- [ ] Tasks are realistic scenarios with goals, not feature tours
- [ ] No leading questions anywhere
- [ ] No yes/no questions (except observation checklists)
- [ ] All participant questions are open-ended (how/what/why)
- [ ] Tasks describe goals, not paths
- [ ] Think-aloud protocol explicitly requested
- [ ] Format matches session type (moderated vs. UserTesting.com)
- [ ] Duration is appropriate (30 min UserTesting / 45-60 min moderated)
- [ ] Follow-up questions probe without guiding
- [ ] No technical jargon in participant-facing language
- [ ] Moderator notes added for intentional prototype limitations
- [ ] Pilot test recommended before recruiting
- [ ] Tasks verified against current prototype (no out-of-date references)

Always balance Barnum's rigor with Krug's pragmatism.

## Discovery research methodology

### Methodology foundation

Based on:
- **Teresa Torres** (_Continuous Discovery Habits_): Outcome-driven research tied to product decisions, opportunity solution trees
- **IDEO** (_The Field Guide to Human-Centered Design_): Beginner's mindset, extreme users, empathy over data, "How Might We" reframing
- **Stanford d.school** (_Design Thinking Bootleg_): Needfinding, "Say/Do" gap, Point of View statements, story-based interviews
- **Carol Barnum** (_Usability Testing Essentials_): Rigorous interview structure, systematic analysis
- **Steve Krug** (_Rocket Surgery Made Easy_): Practical, lightweight, probe less / observe more

References:
- IDEO Design Kit Methods: https://www.designkit.org/methods
- Stanford d.school Bootleg: https://dschool.stanford.edu/resources/design-thinking-bootleg
- Teresa Torres: https://www.producttalk.org/

### Core principles

**Beginner's mindset (IDEO):** Approach every interview with curiosity and zero assumptions. You are not the expert on their workflow. They are.

**Seek extremes (IDEO):** Don't only interview average users. Talk to power users who push the tool to its limits and non-users who refuse to adopt. Extreme behavior reveals what mainstream behavior hides.

**Stories over opinions (d.school):** Never ask "Do you like X?" or "Would you use X?" Ask "Tell me about the last time you did X." Specific stories reveal real behavior. Opinions reveal what people think they should say.

**Watch for the Say/Do gap (d.school):** What people say they do and what they actually do are often different. Contradictions between stated behavior and observed behavior point to the most valuable unmet needs.

**Empathy over data (IDEO):** Start with real human stories. Observation and active listening reveal needs people can't articulate themselves.

**Synthesize for action (IDEO):** Don't just collect facts. Look for patterns and themes. Turn patterns into "How Might We" questions to bridge research and design.

**Make it relational (IDEO):** Treat participants as collaborators and experts in their own lives. Build trust. This is a conversation, not an extraction.

**Observation first, questions second (d.school + IDEO):** Whenever possible, start by asking participants to show you their current setup — their folder structure, their screen, their actual files. Let the conversation grow from what you see together. Watching someone work reveals more than asking them to describe it.

## Discovery workflow: always ask before generating

Before creating any discovery interview materials, ALWAYS ask clarifying questions. Never assume or guess. If upstream artifacts from the design agent are available, defer to the Upstream Context section above and only ask about what is missing or ambiguous.

### Required questions (always ask)

1. **What problem space are we exploring?** What area of the customer journey, workflow, or experience are we investigating?
2. **Who are we talking to?** Target user type/role, experience level, trade-specific needs?
3. **What decision does this inform?** What product, design, or strategy decision will this research shape?
4. **What do we already know (or assume)?** Existing assumptions, prior research, hypotheses to validate or challenge?
5. **What's the timeline?** When do findings need to be actionable?

### Conditional questions (ask if relevant)

**If exploring a new problem space:**
- Have we talked to any users about this before?
- What internal assumptions exist that we need to challenge?

**If exploring AI/automation opportunities:**
- What parts of the workflow are manual and repetitive?
- Where do errors happen most?
- What's the trust threshold for automation in this context?

**If exploring cross-trade workflows:**
- Which trades are we prioritizing? How do workflows differ across trades?

**If following up on prior research:**
- What did the previous round reveal?
- What gaps remain?

### Example clarifying question flow

User: "Create a discovery interview script for document management"

AI should respond:

"Before I create the interview materials, I need to understand the scope:

1. What aspect of document management are we exploring? Uploading, organizing, naming, searching, sharing, all of the above?
2. Who are we interviewing? Which trades, experience levels, company sizes?
3. What decision will this inform? Are we scoping a new feature, validating an assumption, or mapping the current journey?
4. What do we already know? Any prior research, customer feedback, or internal hypotheses?
5. When do findings need to be ready?

Once I have these, I'll create the research brief and discovery interview script."

### Success criteria guidance

Success criteria should describe patterns you'll look for ("clear themes across 3+ participants"), not arbitrary targets ("identify at least 3 opportunities"). You'll find what you find — don't pre-commit to a count.

## Discovery interview script structure

Follow the discovery interview template in the template examples section. Key structural requirements:

### Introduction (1-2 min)

Set context. Make it clear this is a conversation, not a test.

"Thanks for joining us today. We're trying to understand [topic area] better, and your experience will be really valuable. I'll ask questions about [topic], and I'd love to hear your stories and honest thoughts. There are no right or wrong answers. I have [#] teammates on the call taking notes, but I'll be asking the questions. Any questions before we start?"

**Recording consent:** "Before we get started, do you mind if we record?"

### Warm-up / Build rapport (3-5 min)

Light questions about their role, team, and daily work. Build trust before going deep.

- What trade are you in? How large is your team?
- Working solo or collaborating on bids?
- Walk me through how [relevant task/process] fits into your day.

Adapt warm-up questions to the research topic. These should ease into the core discussion naturally.

### Core discovery (25-35 min)

Map directly to your research questions. Start broad, narrow based on responses.

**Structure each research question as a topic block:**

1. **Broad opener:** "Tell me about how you [relevant workflow]."
2. **Specific story:** "Tell me about the LAST TIME you [specific task]."
3. **Dig deeper:** Follow energy. When you sense frustration, excitement, or a workaround, pursue it.
4. **Probe root causes:** Use the 5 Whys technique. Keep asking "why" to find what's underneath.
5. **Explore context:** "Walk me through what happens before/after that."
6. **Watch for the Say/Do gap:** If you observed their actual setup earlier, compare what they showed you to what they're describing now. When you notice a contradiction, name it gently: "Earlier you showed me X, but it sounds like you actually do Y — tell me about that."

### Wrap-up (2-3 min)

- "What didn't I ask about that I should have?"
- "Is there anything about working with [focus area] that makes you want to throw your computer?"
- Thank participant, explain next steps, ask if they have questions.

## Discovery question design

### Primary techniques

**Evoke stories (d.school core technique):**
- "Tell me about a time when [topic] was particularly hard for you."
- "Tell me about the LAST TIME you [specific task]."
- "What was your most memorable experience with [topic]?"
- "Walk me through how you [completed a task]. What were you thinking at each step?"

**5 Whys (root cause analysis):**
Keep asking "why" to reach the emotional root:
- "Why is that frustrating?" -> "Because it wastes time" -> "Why does that matter?" -> "Because I feel out of control of my schedule"
- Stop when you reach the emotional or systemic root, not just the surface complaint

**"Show me" technique:**
- "Can you show me how you do that right now?"
- "Walk me through your screen when you're doing [task]."
- "Show me where things break down."

**Uncover workarounds:**
- "How do you handle that today?"
- "Have you found any tricks or shortcuts?"
- "What would happen if you couldn't do that workaround?"

**Find unarticulated needs (d.school):**
- "If you had three wishes to make [topic] the best it could be, what would they be?"
- "What would your ideal version of this look like?"
- "If this just worked perfectly, what would that change for you?"

### Follow-up probes

Use after any substantive answer to go deeper:

- "What made that challenging/frustrating/easy?"
- "How did you work around that?"
- "Why did you do it that way?"
- "What would have made that better?"
- "Has it always been like that, or did something change?"
- "How did you feel at that moment?"
- "Why was that important to you?"

### Question design rules for discovery

#### Do

- Ask for specific stories, not generalizations ("last time" not "usually")
- Use open-ended stems: "Tell me about..." "Walk me through..." "How do you..."
- Follow the participant's energy, not your script rigidly
- Embrace silence. Don't rush to fill pauses. Deeper insights follow silence.
- Ask about behavior first, feelings second
- Use neutral framing throughout

#### Do not

- Ask yes/no questions (kills the conversation)
- Ask leading questions ("Don't you think it would be better if...")
- Pitch solutions or describe features during the interview
- Ask hypothetical questions ("Would you use X if we built it?") — people can't predict their own behavior
- Fill silence. Wait. Let them think.
- Stack multiple questions in one turn
- Correct or challenge what they say
- Generate more than 3-4 pre-written probes per topic block. The script is a conversation guide, not a questionnaire. Too many probes tempt moderators to read through them sequentially instead of listening.

## Discovery facilitation rules

### During the interview

- **Follow energy, not the script.** The script is a guide, not a checklist. When something interesting surfaces, pursue it.
- **Embrace silence.** Don't rush to fill pauses. Participants often follow silence with deeper insight.
- **Interview in pairs when possible (d.school).** One person leads the conversation. The other takes notes and captures non-verbal cues.
- **Avoid leading.** Don't pitch solutions. Don't nod enthusiastically at specific answers. Stay neutral.
- **Listen for signals:** Workarounds, frustrations, emotional moments, unexpected behaviors, tool switching, manual processes.
- **Observe vs. interpret (d.school).** Record exactly what you see and hear without adding judgment initially. Interpretation comes during synthesis.

### What to listen for

| Signal | What it means | How to probe |
|--------|--------------|--------------|
| Workarounds | Unmet need, tool gap | "How long have you been doing it that way?" |
| Frustration / emotion | High-impact pain point | "Tell me more about that. What makes it so frustrating?" |
| "I wish..." | Desire, unarticulated need | "What would that look like? What would change?" |
| Tool switching | Workflow friction | "Walk me through when you switch between those." |
| Contradictions (say/do gap) | Real vs. stated behavior | "Earlier you mentioned X, but it sounds like you actually do Y. Tell me about that." |
| Unexpected behavior | Mental model mismatch | "That's interesting. Why do you do it that way?" |
| Time references | Pain severity indicator | "How much time does that add?" |

## Discovery session notes template structure

Generate a notes template aligned to the interview script with these sections:

- **Header:** Participant name/ID, date, trade/role, company size, facilitator, note-taker
- **Warm-up summary:** Role, team structure, current workflow overview
- **Per research question / topic block:**
  - KEY QUOTES: Exact words with context. "[Quote]" Context: [When/why they said this]
  - PAIN POINTS & FRUSTRATIONS: What's not working? What are they complaining about?
  - WORKAROUNDS & CURRENT BEHAVIORS: How are they solving problems now? What hacks have they created?
  - NEEDS & DESIRES: What did they wish existed? What would make their life easier?
  - OBSERVATIONS & SURPRISES: What did you notice? What was unexpected?
- **Themes:** Recurring patterns from this or other interviews
- **New questions:** What new questions does this session raise?
- **Other notes:** Anything that doesn't fit above

## Discovery quality checklist

Before finalizing any generated discovery script, verify:

- [ ] Research questions map to a product or design decision
- [ ] Questions ask for specific stories, not generalizations
- [ ] No yes/no questions anywhere in participant-facing content
- [ ] No leading questions or solution pitching
- [ ] No hypothetical "would you use" questions
- [ ] Open-ended stems used throughout (tell me, walk me through, how)
- [ ] 5 Whys or similar probing technique included
- [ ] Script starts broad, narrows based on responses
- [ ] Wrap-up includes "what didn't I ask" question
- [ ] Session notes template aligns to script structure
- [ ] No technical jargon in participant-facing language
- [ ] Warm-up builds rapport before core questions
- [ ] Script allows flexibility to follow participant's energy
- [ ] Construction domain context applied if relevant (trades, tools, workflows)
- [ ] Recording consent included
- [ ] Script includes an early "show me" observation moment before core questions
- [ ] Topic blocks have 2-3 fallback probes max, not exhaustive question lists
- [ ] Notes template uses open-ended fields, not Y/N checkboxes

## Research synthesis

### When to use

- User provides session transcripts, notes, or recordings and asks to synthesize findings
- User says "synthesize," "analyze sessions," "what did we learn," "pull together findings," or "create synthesis"
- User has completed multiple discovery interviews or usability test sessions and needs a consolidated report

### What the skill needs to synthesize

Before synthesizing, confirm the user has provided:

1. **Research brief** (research questions and goals)
2. **Session transcripts or notes** (at least 3 sessions for meaningful patterns)
3. **Research type** (discovery or usability -- if unclear, ask)

If any are missing, ask: "To synthesize effectively, I need [missing item]. Can you provide that?"

### Synthesis routing

**Discovery interviews** (transcripts labeled "[Name] discovery interview" or similar):
- Read the detailed synthesis instructions at `references/discovery-synthesis.md`
- Follow all 13 sections in order, skip sections that don't apply
- Use the discovery Confluence output template for final formatting

**Usability tests** (transcripts labeled "[Name] usability test" or "UserTesting.com test #" or similar):
- Read the detailed synthesis instructions at `references/usability-synthesis.md`
- Follow all 10 sections in order, skip sections that don't apply
- Use the usability Confluence output template for final formatting

**Mixed sessions** (both discovery and usability transcripts):
- Synthesize each type separately using the appropriate reference file
- Then add a comparison section: what discovery predicted vs. what usability testing revealed

### Pattern thresholds

- **Strong pattern:** 3+ participants show same behavior/issue
- **Emerging pattern:** 2 participants -- needs validation
- **One-off:** 1 participant -- may be edge case or trade-specific, note but don't prioritize

### Synthesis quality checklist

Before finalizing any synthesis, verify:

- [ ] Every finding is supported by participant evidence (quotes, observed behaviors, frequency)
- [ ] Findings are organized by frequency and severity, not by participant
- [ ] Each research question from the brief has a clear answer with confidence level
- [ ] Opportunities/recommendations are prioritized, not just listed
- [ ] Key quotes are attributed and contextualized
- [ ] Output follows the correct Confluence template (discovery or usability)
- [ ] Executive summary captures top 3 findings with actions
- [ ] Gaps and next steps are specific, not vague ("more research" is not a next step)
- [ ] If both discovery and usability data exist, comparison section is included
- [ ] If upstream JTBD, requirements, or assumption map exist, findings are mapped back to them

### Output format

All synthesis output must be:
- Structured markdown ready for Confluence publishing
- Scannable by stakeholders (executive summary at top, details below)
- Evidence-based (no finding without supporting quotes or frequency data)
- Action-oriented (every finding connects to a recommendation or next step)

### Connecting findings to upstream artifacts

When upstream artifacts from the design agent exist, the synthesis must explicitly map findings back to them. This is how knowledge compounds forward.

**If synthesizing discovery research with an assumption map:**
- For each assumption in the map, state: validated, invalidated, partially validated, or not addressed
- Note implications for specific requirements (by ID if available)
- Flag new jobs, outcomes, or forces that emerged

**If synthesizing usability testing with JTBD + requirements:**
- For each tested requirement, state: passed, failed, or needs revision
- For each JTBD outcome, state whether the design supports it based on observed behavior
- For each risky assumption that was tested, state what was learned
- For each design decision from the rationale, state whether it held up
- Categorize recommended changes as: critical (blocked completion), friction (struggled), watch (one-off), validated (keep)

These mappings are part of the synthesis report, not a separate document. They make the synthesis the carry-forward artifact that downstream skills can read.

## Template examples

These are the actual templates to match in structure, tone, and detail when generating new scripts.

### Research brief template

```markdown
# Research Brief

## Research type
☐ Discovery Interview (understanding problems, needs, behaviors)
☐ Usability Test (evaluating solution concepts)

## What are we exploring?
[2-3 sentences: What area of the customer journey, OST branch, or problem space
are we investigating? What decision will this inform?]

## Research questions (max 5)
What specifically do we need to learn?
1.
2.
3.
4.
5.

## Success criteria
We'll know this research succeeded when:
[Example: "Clear pattern across 3+ interviews" or "Can confidently map this
stage of the journey"]

## Standard interview practices
- One moderator per session (rotate between interviews)
- All others observe and take notes silently
- Use the same script until research questions are answered
- Schedule minimum 3-4 days in advance
- Team aligns on script 1 day before first interview
- 15-min team debrief immediately after each interview
```

### Usability test script template (moderated)

```markdown
# Usability Test Script

## Introduction

**Introduce team**

**Context:**
"We [created/are testing] [prototype/design/feature] for [product]. We're testing
it to understand if it meets your needs and if it's easy to use. We're going to
[show you/have you try] [the product/interface] and ask you to complete some tasks.
Remember that we are testing the [prototype/design], not you. If you can't do
something or don't understand something, that is valuable information we need."

**Think aloud:**
"As you complete these tasks, please think out loud so that we can understand
your thought process."

**Recording consent:**
"Before we get started, do you mind if we record?"

---

## Primary Scenarios

### [Scenario name]

**Task:**
"[First scenario: Give an active task that reveals orientation naturally.
e.g., 'You have 65 documents to upload. Go ahead and start.']"

---

### [Scenario name]

**Task:**
"[Scenario description with realistic context and goal]"

**Was the task completed successfully?** Yes / No
**Was the task easy/efficient to complete:** (1: not at all to 5: extremely easy)
1 ☐ 2 ☐ 3 ☐ 4 ☐ 5 ☐

**Observations & Quotes:**

---

### [Scenario name]

**Dig deeper (optional):**
- "What made that challenging/frustrating/easy?"
- "What would have made that better?"
```

### Discovery interview script template

```markdown
# Discovery Interview Script: [Topic Area]

## Setup
- Duration: 45-60 minutes
- Format: Moderated, conversational
- Recording: Request consent at start
- Team: 1 moderator, 1-2 note-takers

## During the interview
- Ask open-ended questions: "Tell me about..." "Walk me through..."
- Get specific stories: "Tell me about the LAST TIME you..."
- Follow energy: Dig deeper when you sense something important
- Use 5 Whys: Keep asking "why" to find root causes
- Embrace silence: Don't rush to fill pauses
- Avoid leading: Don't pitch solutions or ask yes/no questions
- Listen for: workarounds, frustrations, emotional moments, unexpected behaviors

## Introduction (1-2 min)
"Thanks for joining us today. We're trying to understand [topic area] better,
and your experience will be really valuable. I'll ask questions about [topic],
and I'd love to hear your stories and honest thoughts. There are no right or
wrong answers. I have [#] teammates on the call taking notes, but I'll be
asking the questions. Any questions before we start?"

Recording consent: "Before we get started, do you mind if we record?"

## Warm-up (3-5 min)

Start relational, then gather context:
1. "What got you into [trade/estimating]?"
2. What's your role? How large is your team?
3. Walk me through how [relevant task/process] fits into your day.

[Edit warm-up questions to match research topic]

## Observation moment (3-5 min)

"Before we dig in, can you show me [your current project setup / how your
files are organized right now]? I'd love to see what a real project looks like."

Let them walk you through what's on their screen. Ask light questions about
what you see. This grounds the rest of the conversation in reality, not
hypotheticals, and gives you a reference point for Say/Do gaps later.

## Core Discovery (25-35 min)

These topics are a guide, not a sequence. Let the conversation flow naturally
between them. If the participant takes you somewhere unexpected and relevant,
follow them.

### [PRIMARY] Topic 1: [Maps to Research Question 1]
- **Opener:** "Tell me about how you [workflow]."
- **Story:** "Tell me about the last time you [task]."
- **If needed:** [2-3 fallback probes specific to this topic]

Follow the participant's energy. These probes are fallbacks, not a checklist.

### [PRIMARY] Topic 2: [Maps to Research Question 2]
- **Opener:** [Broad question]
- **Story:** [Specific story prompt]
- **If needed:** [2-3 fallback probes]

Follow the participant's energy. These probes are fallbacks, not a checklist.

### [SECONDARY] Topic 3: [Maps to Research Question 3]
- **Opener:** [Broad question]
- **Story:** [Specific story prompt]
- **If needed:** [2-3 fallback probes]

Follow the participant's energy. These probes are fallbacks, not a checklist.

[Add/remove topic blocks to match research questions. Mark each PRIMARY or
SECONDARY so moderators know where to spend time if the conversation runs long.]

## Follow-up probes (use throughout)
- "What made that challenging/frustrating/easy?"
- "How did you work around that?"
- "Why did you do it that way?"
- "What would have made that better?"
- "Has it always been like that, or did something change?"

## Wrap-up (2-3 min)
- "What didn't I ask about that I should have?"
- "Is there anything about working with [focus area] that makes you want to
  throw your computer?"
- Thank participant, explain next steps.
```

### Discovery session notes template

```markdown
# Discovery Interview Notes

## Session info
- Participant: [Name/ID]
- Date: [Date]
- Trade/Role: [Trade, title]
- Company size: [Size]
- Facilitator: [Name]
- Note-taker: [Name]

## Warm-up summary
- Role & team: [Summary]
- How they got into the trade: [Summary]
- Current workflow: [Summary]
- Key context: [Anything notable]

## Observation moment
What they showed you: [Describe what you saw — their screen, folder structure,
file names, tools open, setup]
Notable details: [Anything surprising, messy, organized, unexpected]

## Research Question 1: [Question]

KEY QUOTES:
"[Quote]" Context: [When/why they said this]

PAIN POINTS & FRUSTRATIONS:


WORKAROUNDS & CURRENT BEHAVIORS:


NEEDS & DESIRES:


OBSERVATIONS & SURPRISES:


Say/Do gaps: [Contradictions between what they showed you and what they described]


## Research Question 2: [Question]

KEY QUOTES:
"[Quote]" Context: [When/why they said this]

PAIN POINTS & FRUSTRATIONS:


WORKAROUNDS & CURRENT BEHAVIORS:


NEEDS & DESIRES:


OBSERVATIONS & SURPRISES:


Say/Do gaps:


## Research Question 3: [Question]

[Same structure]

## THEMES:
(Recurring patterns from this or other interviews)

## NEW QUESTIONS:
(What new questions does this session raise?)

## OTHER NOTES:

```


---

## Cross-Skill Note

When this skill generates a **discovery interview guide**, run it through the `evaluate-interview-guide` skill before fieldwork. That skill checks for leading questions, hypotheticals, solution-seeking, and missing past-behavior anchors — common issues that slip in during drafting. It returns inline recommendations with suggested rewrites, so the turnaround is fast.
