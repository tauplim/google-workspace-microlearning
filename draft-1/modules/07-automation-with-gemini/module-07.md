# Module 7: Automation with Gemini
**Duration:** 30 minutes | **Framework:** Learn, Consolidate, Compress
**Prerequisites:** Modules 1-6

---

## Learning Objective

Identify and execute automation opportunities using Gemini prompt patterns for repetitive work tasks.

## Success Criteria

By the end of this session, you will be able to:
1. Identify automation opportunities in daily workflows
2. Write effective multi-step Gemini prompts
3. Execute prompt chains for compound tasks
4. Build a personal automation playbook

---

## Session Overview

```
┌─────────────────────────────────────────────────────────────┐
│ MODULE 7: Automation with Gemini                           │
├─────────────────────────────────────────────────────────────┤
│ LEARN (12 min)                                              │
│ • Automation mindset (3 min)                                │
│ • Prompt chaining patterns (4 min)                          │
│ • Live demonstration (4 min)                                 │
│                                                             │
│ CONSOLIDATE (18 min)                                        │
│ • Guided workshop: Automate 3 tasks (10 min)                │
│ • Personal playbook creation (3 min)                         │
│ • Share-back and debrief (2 min)                            │
│                                                             │
│ COMPRESS (2 min)                                            │
│ • Automation playbook with 10 patterns                      │
│ • Bridge to Module 8                                         │
└─────────────────────────────────────────────────────────────┘
```

---

## LEARN Phase

### Part 1: Automation Mindset (3 minutes)

**The Automation Principle:**

> "If you do something more than twice, there's likely a way to automate it."

**What Can Be Automated?**

| Category | Examples |
|----------|----------|
| **Information tasks** | Summarize, extract, compare, translate |
| **Writing tasks** | Draft emails, generate reports, create content |
| **Organization** | Sort files, rename batches, tag content |
| **Communication** | Generate responses, schedule messages, follow-ups |

**What Cannot (Yet) Be Fully Automated:**

- Decisions requiring judgment
- Tasks with changing requirements
- Anything requiring physical actions
- Creative breakthroughs

**Automation vs. Delegation vs. Elimination:**

| Strategy | When to Use | AI Tool |
|----------|-------------|---------|
| **Automate** | Same task, predictable output | Gemini prompt chains |
| **Delegate** | Someone else should own it | Assign to human |
| **Eliminate** | Task no longer valuable | Simply stop doing |

---

### Part 2: Prompt Chaining Patterns (4 minutes)

**What is Prompt Chaining?**

Breaking a complex task into sequential AI operations where output becomes input for the next step.

**Chain 1: Research → Summarize → Draft**

```
INPUT: 3 articles on remote work
  ↓
STEP 1: Gemini extracts key findings from all sources
  ↓
STEP 2: Gemini synthesizes findings into comparison
  ↓
STEP 3: Gemini drafts executive brief from synthesis
  ↓
OUTPUT: Ready-to-share research brief
```

**Chain 2: Draft → Review → Refine → Send**

```
INPUT: Meeting notes
  ↓
STEP 1: Gemini extracts decisions and actions
  ↓
STEP 2: Gemini drafts team email summary
  ↓
STEP 3: Gemini adjusts tone (formal/casual)
  ↓
STEP 4: Copy to Gmail, send
  ↓
OUTPUT: Professional team update
```

**Chain 3: Gather → Analyze → Visualize**

```
INPUT: Spreadsheet data
  ↓
STEP 1: Gemini summarizes data trends
  ↓
STEP 2: Gemini identifies top 5 insights
  ↓
STEP 3: Gemini suggests chart types
  ↓
OUTPUT: Analysis ready for presentation
```

**Effective Chain Design Principles:**

1. **One transformation per step** - Don't ask for too much at once
2. **Clear output format** - Tell Gemini what format to produce
3. **Verification point** - Check output before proceeding
4. **Error handling** - Ask Gemini to flag if input is insufficient

---

### Part 3: Live Demonstration (4 minutes)

**Watch the trainer perform these actions:**

1. **Simple Chained Task**
   - Open sample email thread
   - Prompt 1: "Summarize this email thread in 3 bullets"
   - Prompt 2: "Based on these bullets, draft a response confirming our action items"
   - Prompt 3: "Make this email more concise (under 100 words)"

2. **Multi-Step Document Processing**
   - Take a long document
   - Prompt 1: "Extract all dates and deadlines mentioned"
   - Prompt 2: "Create a calendar event description from these dates"
   - Prompt 3: "Draft a follow-up email referencing these deadlines"

3. **Bulk Content Generation**
   - Show template variable approach
   - Generate 3 variations with different parameters
   - Demonstrate batch mindset

---

## CONSOLIDATE Phase

### Guided Workshop: Automate 3 Tasks (10 minutes)

**Task 1: Identify Your Automation Opportunities (2 minutes)**

Look at your work from the past week. What tasks did you repeat?

| Task You Repeated | Frequency | Time per Instance | Total Time |
|-------------------|-----------|-------------------|------------|
| | | | |
| | | | |
| | | | |

**Select ONE task to automate with Gemini.**

**Task 2: Build Your First Prompt Chain (4 minutes)**

Using your selected task, create a 3-step chain:

```
CHAIN NAME: [Name your automation]

STEP 1: [What to extract/gather]
  Prompt: "[Exact prompt to use]"

STEP 2: [What to transform/process]
  Prompt: "[Exact prompt to use]"

STEP 3: [What to generate/output]
  Prompt: "[Exact prompt to use]"
```

**Task 3: Execute and Test (4 minutes)**

1. Run your prompt chain
2. Evaluate output quality
3. Refine prompts based on results
4. Document what worked and what needs adjustment

---

### Personal Playbook Creation (3 minutes)

**Create your Automation Playbook:**

1. Open new Google Doc titled: "My Automation Playbook"
2. Add the template below
3. Fill in your 3 most valuable automation chains from the course:

```
MY AUTOMATION PLAYBOOK
========================

1. [AUTOMATION NAME]
   Task: [What it automates]
   Chain:
   - Step 1: [Prompt]
   - Step 2: [Prompt]
   - Step 3: [Prompt]
   
2. [AUTOMATION NAME]
   ...

3. [AUTOMATION NAME]
   ...
```

---

### Share-Back and Debrief (2 minutes)

**Discussion:**

1. What automation did you build that could save you time weekly?
2. What limitations did you encounter?
3. What additional automations would you like to explore?

---

## COMPRESS Phase

### Pattern Recap (1 minute)

**The ONE thing to remember:**

> "Prompt chaining turns AI from a one-off assistant into an automated workflow engine. Break complex tasks into simple, sequential steps."

**Chain Building Rules:**
1. Each step does ONE thing well
2. Tell Gemini what format to output
3. Review output before next step
4. Save successful chains as templates

---

### Take-Away: Automation Playbook with 10 Patterns

Save these battle-tested prompt patterns:

```
╔═══════════════════════════════════════════════════════════════════╗
║           GEMINI AUTOMATION PATTERN PLAYBOOK                      ║
╠═══════════════════════════════════════════════════════════════════╣
║                                                                   ║
║  PATTERN 1: SUMMARIZE + EXTRACT                                   ║
║  "Summarize [source] in [X] bullets, then extract [specific data]" ║
║  Use: Research, meeting notes, long documents                     ║
║                                                                   ║
║  PATTERN 2: COMPARE + RECOMMEND                                   ║
║  "Compare [A] and [B] on [criteria], then recommend [decision]"    ║
║  Use: Vendor selection, approach evaluation                        ║
║                                                                   ║
║  PATTERN 3: DRAFT + POLISH                                        ║
║  "Draft [document type], then polish for [audience/tone]"        ║
║  Use: Emails, reports, presentations                              ║
║                                                                   ║
║  PATTERN 4: LIST + PRIORITIZE                                    ║
║  "List [items], then prioritize by [criteria]"                   ║
║  Use: Task lists, action items, project planning                 ║
║                                                                   ║
║  PATTERN 5: EXPLAIN + EXAMPLE                                    ║
║  "Explain [concept], then give 3 practical examples"            ║
║  Use: Training materials, documentation                           ║
║                                                                   ║
║  PATTERN 6: TRANSLATE + LOCALIZE                                  ║
║  "Translate to [language], then adapt for [cultural context]"    ║
║  Use: Global communications, client materials                     ║
║                                                                   ║
║  PATTERN 7: ANALYZE + VISUALIZE                                   ║
║  "Analyze [data] for [insight type], then suggest visualization]" ║
║  Use: Reports, dashboards, presentations                          ║
║                                                                   ║
║  PATTERN 8: REVIEW + IMPROVE                                      ║
║  "Review [work] for [criteria], then suggest 3 improvements"     ║
║  Use: Document review, code review, content editing               ║
║                                                                   ║
║  PATTERN 9: RESEARCH + SYNTHESIZE                                ║
║  "Research [topic], synthesize key findings into [deliverable]"   ║
║  Use: Market research, competitive analysis                      ║
║                                                                   ║
║  PATTERN 10: TEMPLATE + GENERATE                                  ║
║  "Fill [template] with [data/input], generate [output type]"      ║
║  Use: Standardized documents, repetitive reports                 ║
║                                                                   ║
╚═══════════════════════════════════════════════════════════════════╝
```

---

### Bridge to Module 8 (1 minute)

**Next Module Preview:**
In Module 8 (Final Project), you'll demonstrate everything you've learned by building a complete **AI Workspace Playbook** that integrates at least 3 Google Workspace apps with Gemini.

**This is your capstone project — bring all your learning together.**

---

## Session Notes

**Automation I'll use most often:**

___________________________________________________________________

**Pattern I want to try that we didn't cover:**

___________________________________________________________________

**Chain I'll build next:**

___________________________________________________________________

---

## Compression Artifact Checklist

- [ ] Identified 3 automation opportunities
- [ ] Built and tested one prompt chain
- [ ] Created Personal Automation Playbook
- [ ] Saved 10 Pattern Playbook
- [ ] Documented one chain to reuse

---

**End of Module 7**