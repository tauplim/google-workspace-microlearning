# Tech Brief: Three Steps Workflow — Research → Bridge → Course Writing

## Overview

This document explains the architecture of a multi-agent workflow for creating professional training courses. The workflow uses three distinct steps — each handled by a different agent or process — to transform a training topic into a complete, market-aligned course with slides, guides, and workbooks.

**The core principle:** Separate three types of cognitive work that require different expertise and produce different outputs.

---

## The Three Steps

### Step 1: Industry Research
**Agent:** `industry-research-expert`
**Output:** Strategic Context Document (`.md`)

### Step 2: Design Bridge
**Agent:** Human or `general-agent`
**Output:** Content Review / Design Brief (`.md`)

### Step 3: Course Content Creation
**Agent:** `adult-training-course-writer`
**Output:** Course modules, facilitator guide, participant workbook, HTML slides

---

## Step 1: Industry Research Agent

### Purpose
Research the external landscape — market opportunity, competitor landscape, target buyer profile, pricing context — to answer the business question: **"Is there a training product business here?"**

### Expertise Used
- Market analysis
- Competitor research
- Buyer psychology
- Training industry trends

### Output Format
Strategic Context Document (`google-workspace-stragetic-document.md`)

### What It Contains

| Section | Example (Google Workspace) |
|---------|---------------------------|
| Market size | $400B+ corporate training market |
| Growth rate | 18.5% CAGR for e-learning |
| Competitor landscape | Google Cloud Skills Boost, Coursera, Intellezy, Netskill |
| Opportunity gap | No native Google microlearning platform |
| Target buyer profile | Mid-market (300-1000 employees) |
| Buyer pain points | 85% can't measure ROI; 21-day productivity gap |
| Learning hour constraints | 13.7 hours/employee/year |
| Pricing benchmarks | $8-15/user/month |

### What It Does NOT Contain
- How to use specific Google Workspace features
- Technical workflows or tutorials
- Instructional design decisions
- Course structure or module sequences

### Why It's Separated
A market researcher is not trained to make pedagogical decisions. Keeping research pure ensures the course writer later receives actual market data, not assumptions dressed up as research.

---

## Step 2: Design Bridge

### Purpose
Transform the raw strategic context into an actionable design brief. Maps each research finding to a design implication, extracting target learner profile, format constraints, success metrics, module priorities, and differentiators.

**Answers:** "What should we prioritize and why?"

### Who Runs It
Human operator OR `general-agent` (no specialized training required)

### Input
1. Strategic Context Document from Step 1
2. Bridge template: `strategic-context-to-course-design-bridge.md`

### Output
Content Review / Design Brief (`content-review-google-workspace-strategic-document.md`)

### Bridge Template Sections

| Section | What It Extracts |
|---------|-------------------|
| A: Target Learner Profile | Who learns, experience level, time constraints, pain points, success definition |
| B: Market Positioning | Opportunity gap, differentiation, competitor context |
| C: Format Constraints | Content format, session length, learning hour allocation, delivery mode |
| D: Design Implications | Tables mapping each research finding to a design implication |
| E: Success Metrics | Immediate, short-term (30 days), long-term outcomes |
| F: Module Priority Guidance | Highest, secondary, tertiary priorities + explicit exclusions |
| G: Differentiation Focus | 2-3 key differentiators with rationale |

### Why It's Separated
- A course writer needs **actionable parameters**, not raw research to interpret
- This step prevents the course writer from cherry-picking research to justify pre-conceived designs
- Creates a **traceable chain**: every design decision traces back to a specific research finding

### Key Principle: "Extract Don't Interpret"
Fill the bridge by pulling facts from the strategic document. Do not add new research or opinions.

---

## Step 3: Course Content Creation Agent

### Purpose
Take the strategic context AND the filled bridge, then make all course design decisions and generate the actual course artifacts.

**Answers:** "How do we teach it?"

### Agent: `adult-training-course-writer`
**Mode:** Mode A (course creation — not marketing collateral)

### Inputs
1. Strategic Context Document (`/plan/research/google-workspace-stragetic-document.md`)
2. Content Review / Design Brief (`/plan/research/content-review-google-workspace-strategic-document.md`)
3. Output folder location (`/draft-1/`)

### What Gets Created

| Artifact | Description |
|----------|-------------|
| `course-architecture.md` | Overall course structure and design rationale |
| `module-01.md` through `module-08.md` | Individual module content files |
| `facilitator-guide.md` | Instructor notes and delivery guidance |
| `participant-workbook.md` | Learner-facing exercises and takeaways |
| `slides/*.html` | HTML slides (audience + presenter versions per module) |

### Design Decisions Made By This Agent
- Number of modules
- Module length and sequence
- Pedagogical approach
- Activity selection
- Slide design
- Timing allocation

### Why It's Separated
An instructional designer working from raw market research will either (a) ask you to interpret the research for them, or (b)\ make up assumptions. By providing an already-interpreted brief, the course writer focuses on what they do best — designing learning experiences.

---

## Visual Flow

```
                    ┌─────────────────────┐
                    │   TRAINING TOPIC    │
                    │ "Google Workspace  │
                    │   with AI"         │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │  STEP 1: INDUSTRY  │
                    │     RESEARCH        │
                    │                     │
                    │ industry-research-  │
                    │      expert          │
                    └──────────┬──────────┘
                               │ Strategic Context
                               ▼
                    ┌─────────────────────┐
                    │ STEP 2: BRIDGE /     │
                    │  CONTENT REVIEW     │
                    │                     │
                    │ general-agent or    │
                    │      HUMAN          │
                    └──────────┬──────────┘
                               │ Design Brief
                               ▼
                    ┌─────────────────────┐
                    │ STEP 3: COURSE      │
                    │   CREATION          │
                    │                     │
                    │ adult-training-     │
                    │ course-writer        │
                    │    (Mode A)         │
                    └──────────┬──────────┘
                               │ Course Artifacts
                               ▼
                    ┌─────────────────────┐
                    │  ✓ course-architecture.md
                    │  ✓ module-01.md ... │
                    │  ✓ facilitator-guide │
                    │  ✓ participant-     │
                    │    workbook         │
                    │  ✓ HTML slides      │
                    └─────────────────────┘
```

---

## The Core Principle

**Separation of "What's true?" from "What do we do about it?" from "How do we teach it?"**

| Question | Who Answers It | Output |
|----------|----------------|--------|
| Is there a training business here? | Industry Research Agent | Research facts: market size, competitors, buyer pain points |
| What should we prioritize and why? | Bridge (Human/General) | Design brief: target learner, format, priorities, differentiators |
| How do we structure and teach it? | Course Writer Agent | Course content: modules, guides, slides |

This chain ensures:
1. **Research is not biased by design preferences** — market analyst doesn't know what the course will look like
2. **Design decisions are grounded in research** — every choice traces to a specific finding
3. **Course writer operates from a clear brief** — no ambiguity, no reinterpretation needed

---

## Metadata

- **Document name:** 0-explainer-three-steps-workflow.md
- **Location:** `/plan/research/`
- **Related files:**
  - `1-instructions-end-to-end.md` — Step-by-step workflow commands
  - `strategic-context-to-course-design-bridge.md` — Bridge template
  - `prompt-industry-expert-course-topic-research.md` — Research prompt
  - `prompt-course-content-creation-v2.md` — Course creation prompt
- **Intended audience:** Course creation team, workflow operators
