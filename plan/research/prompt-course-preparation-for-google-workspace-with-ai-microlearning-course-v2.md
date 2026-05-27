# Prompt: Course Content Creation from Strategic Research

**For Agent:** adult-training-course-writer (Mode A)
**Input:** Strategic Context Document (from `industry-research-expert` agent)
**Output:** Course content files and presentation materials

---

## Purpose

This prompt transforms a **Strategic Context Document** produced by the `industry-research-expert` agent into a complete, production-ready course. The course writer uses the research findings to make all pedagogical decisions rather than having them specified in the prompt.

---

## Input: Strategic Context Document

The `industry-research-expert` agent produces a strategic context document containing:

- **Market Opportunity** - Size, growth rate, key trends, segments
- **Competitive Landscape** - Who competes, their positioning, gaps
- **Target Buyer Profile** - Demographics, pain points, decision criteria
- **Pricing Benchmarks** - Current market rates for comparable offerings
- **Go/No-Go Recommendation** - Investment recommendation with rationale
- **Risk Factors** - Key obstacles and mitigation strategies

The specific file location will be provided when the prompt is invoked.

---

## Your Task

### 1. Analyze the Strategic Context

Extract from the strategic context document:

- **Who is the target learner?** (role, experience level, pain points)
- **What is the market opportunity?** (size, urgency, willingness to pay)
- **What competitive gaps exist?** (what's missing from current offerings)
- **What is the recommended positioning?** (how should the course be framed)
- **What pricing benchmarks apply?** (market-based pricing context)

### 2. Design the Course Structure

Based on your expertise in adult learning and instructional design, determine:

- **Total course duration** - What fits the target audience's time constraints?
- **Number of modules** - How many to effectively cover the topic?
- **Module length** - Can span multiple sessions; each session is 30 minutes
- **Session structure** - Each session totals 30 minutes; modules may span sessions
- **Learning framework** - What pedagogical approach best suits the content and audience?
- **Module sequence** - What order builds skills progressively?
- **Workshop-to-lecture ratio** - How much hands-on practice?

Document your rationale in the **Course Architecture** document.

### 3. Create the Course Content

Develop all required materials:

#### Course Architecture Document
- Pedagogical framework and rationale
- Module sequence with learning objectives
- Assessment and evaluation approach
- Compression artifacts and takeaways

#### Module Content Files (one per module)
Each module should include:
- **Learning Objective** - What learners will achieve
- **Success Criteria** - Measurable outcomes (3-5 items)
- **LEARN Phase** - Concept introduction with timing
- **CONSOLIDATE Phase** - Hands-on practice activities
- **COMPRESS Phase** - Key pattern takeaway
- **Session Notes** - Reflection questions for learners
- **Compression Artifact** - Practical deliverable (playbook, template, checklist)

#### Facilitator Guide
- Session plan with timing
- Preparation notes
- Activity instructions
- Troubleshooting guidance

#### Participant Workbook
- Exercise worksheets
- Note-taking sections
- Workspace templates
- Reference materials

### 4. Create Presentation Materials

For each module, produce dual-screen HTML slides:

**Audience View:**
- Clean 16:9 display optimized for projection
- Slide counter
- Arrow key navigation
- Dark theme with accent colors

**Presenter View:**
- Live preview of audience display
- Speaker notes with:
  - Slide cue
  - Timing box
  - Key message
  - Trainer action guidance
  - Full facilitator script
- Reference desk with hyperlinks

**Technical Requirements:**
- BroadcastChannel sync between presenter and audience
- Responsive design for different screen sizes
- Consistent visual styling throughout

---

## Quality Standards

All content must meet these requirements:

- **Production-ready** - No placeholder text, no "[insert]" or "[example]" sections
- **Specific examples** - Real-world scenarios, actual prompts, actionable steps
- **Practical application** - Learners doing, not just watching
- **Accessible** - Clear navigation, readable text, sufficient contrast
- **Facilitator-ready** - Speaker notes complete enough for new facilitators

---

## Output Structure

The course writer determines the optimal folder structure based on module count and content type. Typical structure:

```
/draft-1/
  course-architecture.md
  facilitator-guide/
    facilitator-guide.md
  participant-workbook/
    participant-workbook.md
  modules/
    [module-01]/
      module-01.md
    [module-02]/
      module-02.md
    ...
/slides/
  module-01-audience.html
  module-01-presenter.html
  module-02-audience.html
  module-02-presenter.html
  ...
```

---

## Workflow

1. **Receive** the strategic context document path
2. **Analyze** market opportunity, target audience, competitive gaps
3. **Design** course structure and module sequence
4. **Create** Course Architecture document first
5. **Develop** modules sequentially with slides
6. **Build** facilitator guide and participant workbook
7. **Validate** each deliverable against quality standards

---

## Notes

- **Mode A only** - This prompt produces course content. Marketing collateral (One-Pager, Landing Page, Course Overview) is created separately in Mode B after all modules are approved.
- **Flexible structure** - The course writer determines module count, duration, and pedagogical approach based on the research. Do not impose arbitrary constraints.
- **AI integration** - If the subject matter includes AI tools or features, ensure practical AI prompts are included throughout (copy-paste ready for participants).
- **Compression artifacts** - Each module should produce a tangible takeaway learners can use immediately after the session.

---

## Decision Authority

The course writer has full authority to determine:

- Number of modules (not pre-specified)
- Module length (may span multiple 30-minute sessions)
- Specific learning activities (based on content type)
- Slide count per module (based on content density)
- Workshop-to-lecture ratio (optimized for learning outcomes)
- How to split module content across sessions if needed

Your expertise guides these decisions. Trust your judgment.