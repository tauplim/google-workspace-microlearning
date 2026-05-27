# Step-by-Step Course Creation Workflow

This workflow creates a complete microlearning course through three steps: research → bridge → content creation. Each step produces an output file that feeds into the next step.

---

## Step 1: Run Industry Research

**Prompt file:** `prompt-industry-expert-course-topic-research.md`

**Run using:** Task tool with subagent_type `industry-research-expert`

**What you provide:**
```
Topic: [Describe the training topic]
Example: "Google Workspace with AI Microlearning Course"
```

**Output:** Strategic Context Document (e.g., `google-workspace-stragetic-document.md`)

---

## Step 2: Apply the Bridge

**Template file:** `strategic-context-to-course-design-bridge.md`

**Run using:** Manual process OR Task tool with subagent_type `general-agent`

**Inputs:**
1. Strategic Context Document from Step 1
2. The bridge template (`strategic-context-to-course-design-bridge.md`)

**Output:** `content-review-[topic].md`

---

### How to Fill the Bridge Template

The bridge transforms the strategic context document into actionable design parameters. Fill each section by extracting from the research document:

#### Section A: Target Learner Profile

| Field | What to Write |
|-------|---------------|
| Primary learner role | Who is this course for? (job title, industry, company size) |
| Experience level | Beginner, intermediate, or advanced in the subject? |
| Time constraints | Hours per year available for training? |
| Pain points | What 2-4 specific problems does this course solve? |
| Success definition | What does a learner look like after completing? |

#### Section B: Market Positioning

| Field | What to Write |
|-------|---------------|
| Opportunity gap | What is missing in the current training market? |
| Differentiation | What makes this course unique vs alternatives? |
| Competitor context | Who else offers similar training? What are their weaknesses? |

#### Section C: Format Constraints

| Field | What to Write |
|-------|---------------|
| Content format | Microlearning, video, hands-on labs, etc.? |
| Session length | How long is a typical learner session? (target: 20-30 min) |
| Learning hour allocation | Total learning hours available per year? |
| Delivery mode | Self-paced, instructor-led, or hybrid? |

#### Section D: Design Implications Mapping

For each key research finding, state the corresponding design implication:

| Research Finding | Design Implication |
|------------------|-------------------|
| [Market opportunity] | [How does this affect course scope?] |
| [Target learner pain point] | [How does this shape content priority?] |
| [Competitor gap] | [How does this create differentiation?] |
| [Format constraint] | [How does this limit design?] |
| [Pricing context] | [How does this affect tier or pilot offering?] |

#### Section E: Success Metrics

| Metric | Definition |
|--------|------------|
| Immediate | What can learner do after ONE session? |
| Short-term (30 days) | What improvement expected within 30 days? |
| Long-term | How does this affect business or outcome goals? |

#### Section F: Module Priority Guidance

| Priority | Topic | Rationale |
|----------|-------|-----------|
| Highest | [Core value prop] | [Why must be first/central] |
| Secondary | [Supporting topics] | [Important but not primary] |
| Tertiary | [Advanced/niche] | [Nice-to-have if time permits] |
| Exclusions | [Out of scope] | [Explicitly NOT covered] |

#### Section G: Differentiation Focus

1. **[Primary differentiator]** — [Why learner should choose this over alternatives]
2. **[Secondary differentiator]** — [Supporting unique value]
3. **[Tertiary differentiator]** — [Nice-to-have edge]

**Tips:**
- Extract don't interpret — Pull facts from the strategic document; don't invent new research
- Be specific on pain points — Generic pain points lead to generic course design
- Tie design implications to research findings — Every design decision traces back to research
- Priority rankings should be actionable — The course writer uses these to sequence modules
- Differentiators should be testable — Verify the course delivers on these claims

---

### Example Bridge Fill (Google Workspace)

| Bridge Field | What You Write |
|--------------|----------------|
| Primary learner role | Mid-market professionals (300-1000 employees) using Google Workspace daily but underutilizing AI features |
| Experience level | Basic to intermediate — familiar with core apps, AI/Gemini is new |
| Time constraints | 13.7 hours/year average learning budget |
| Pain points | Can't measure training ROI; 21-day productivity gap not solved by software alone |
| Opportunity gap | No purpose-built microlearning platform that integrates natively with Google Workspace workflows |
| Content format | Microlearning (explicitly dominant trend); AI-driven adaptive learning |
| Session length | 30 minutes max |
| Highest priority | Foundation (Gemini + core apps), AI integration across apps |
| Primary differentiator | Native Google + Gemini integration (no third-party wrapper) |

**Bridge Output:** `content-review-google-workspace-strategic-document.md`

---

## Step 3: Create Course Content

**Prompt file:** `prompt-course-content-creation-v2.md`

**Run using:** Task tool with subagent_type `adult-training-course-writer`

**What you provide (three inputs):**

| Input | Path |
|-------|------|
| 1. Strategic Context Document | `/plan/research/google-workspace-stragetic-document.md` |
| 2. Filled Bridge / Content Review | `/plan/research/content-review-google-workspace-strategic-document.md` |
| 3. Output folder | `/draft-1/` |

**What gets created:**
- `course-architecture.md`
- `module-01.md` through `module-08.md`
- `facilitator-guide.md`
- `participant-workbook.md`
- HTML slides (audience + presenter for each module)

---

## Visual Flow

```
┌─────────────────────────────────────────────────────────────┐
│ STEP 1: Industry Research                                    │
├─────────────────────────────────────────────────────────────┤
│ Run: prompt-industry-expert-course-topic-research.md         │
│ Input: "Google Workspace with AI Microlearning Course"      │
│ Output: google-workspace-stragetic-document.md               │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 2: Apply Bridge                                         │
├─────────────────────────────────────────────────────────────┤
│ Fill: strategic-context-to-course-design-bridge.md           │
│ Input: Strategic Context Document + Bridge Template         │
│ Output: content-review-google-workspace.md                  │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 3: Course Creation                                     │
├─────────────────────────────────────────────────────────────┤
│ Run: prompt-course-content-creation-v2.md                   │
│ Input:                                                      │
│   - /plan/research/google-workspace-stragetic-document.md   │
│   - /plan/research/content-review-google-workspace.md      │
│   - /draft-1/                                               │
│ Output:                                                     │
│   - course-architecture.md                                 │
│   - module-01.md through module-08.md                      │
│   - facilitator-guide.md                                    │
│   - participant-workbook.md                                │
│   - HTML slides                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Copy-Paste Commands

### Step 1 — Run Industry Research
```
Use Task tool with:
  subagent_type: "industry-research-expert"
  prompt: [contents of prompt-industry-expert-course-topic-research.md]
```

### Step 2 — Fill Bridge (Manual or General Agent)
```
Read: /plan/research/[strategic-context-document].md
Read: /plan/research/strategic-context-to-course-design-bridge.md
Fill the bridge template using the strategic context as source
Save as: /plan/research/content-review-[topic].md
```

### Step 3 — Create Course
```
Use Task tool with:
  subagent_type: "adult-training-course-writer"
  prompt: [contents of prompt-course-content-creation-v2.md]
  (include the two input file paths in the prompt)
```

---

## Example Input Reference

| Step | What You Type/Input |
|------|---------------------|
| 1 | "Google Workspace with AI Microlearning Course" |
| 2 | Extract from research: buyer profile, pain points, market gap, format constraints, success metrics, priorities, differentiators |
| 3 | `/plan/research/google-workspace-stragetic-document.md` + `/plan/research/content-review-google-workspace.md` + `/draft-1/` |
