## Step-by-Step Workflow

---

### Step 1: Run Industry Research (One-time setup per topic)

**Prompt to run:** `prompt-industry-expert-course-topic-research.md`

**Input you provide:**
```
Topic: [Describe the training topic]
Example: "Google Workspace with AI Microlearning Course"
```

**Output you'll receive:** Strategic Context Document
```
Example output: google-workspace-stragetic-document.md
```

---

### Step 2: Apply the Bridge (Fill the template)

**Prompt to use:** (No agent needed - you do this manually or use general agent)

**Input you provide:**
- The Strategic Context Document from Step 1
- Fill in the `strategic-context-to-course-design-bridge.md` template

**Example for Google Workspace:**

| Bridge Field | What you write |
|-------------|----------------|
| Primary learner role | Mid-market professionals (300-1000 employees) |
| Time constraints | 13.7 hours/year |
| Pain points | Can't measure ROI; 21-day productivity gap |
| Opportunity gap | No native Google microlearning platform |

**Output:** `content-review-google-workspace-strategic-document.md`

---

### Step 3: Create Course Content

**Prompt to run:** `prompt-course-content-creation-v2.md`

**Inputs you provide:**
1. Path to Strategic Context Document
   ```
   /plan/research/google-workspace-stragetic-document.md
   ```

2. Path to Filled Bridge/Content Review
   ```
   /plan/research/content-review-google-workspace-strategic-document.md
   ```

3. Output folder location
   ```
   /draft-1/
   ```

**What the prompt does:**
- Reads the strategic context
- Reads your filled bridge
- Makes all course design decisions (module count, length, sequence)
- Creates Course Architecture
- Creates Module content files
- Creates Facilitator Guide
- Creates Participant Workbook
- Creates HTML slides

---

## Visual Flow

```
┌─────────────────────────────────────────────────────────────┐
│ STEP 1: Industry Research                                    │
├─────────────────────────────────────────────────────────────┤
│ You run: prompt-industry-expert-course-topic-research.md     │
│ You input: "Google Workspace with AI"                       │
│ You get:   google-workspace-stragetic-document.md            │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 2: Apply Bridge (Manual or General Agent)                │
├─────────────────────────────────────────────────────────────┤
│ Use: strategic-context-to-course-design-bridge.md            │
│ Fill in: Target learner, format, implications, priorities    │
│ You get:   content-review-[topic].md                        │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 3: Course Creation                                     │
├─────────────────────────────────────────────────────────────┤
│ You run: prompt-course-content-creation-v2.md                │
│ You input:                                                 │
│   - /plan/research/google-workspace-stragetic-document.md   │
│   - /plan/research/content-review-google-workspace.md      │
│   - /draft-1/                                              │
│ You get:                                                   │
│   - course-architecture.md                                 │
│   - module-01.md through module-08.md                     │
│   - facilitator-guide.md                                    │
│   - participant-workbook.md                                │
│   - slides (audience + presenter for each module)          │
└─────────────────────────────────────────────────────────────┘
```

---

## Copy-Paste Commands

**Step 1 - Run Industry Research:**
```
Use Task tool with:
  subagent_type: "industry-research-expert"
  prompt: [contents of prompt-industry-expert-course-topic-research.md]
```

**Step 2 - Fill Bridge (manual or with general agent):**
```
Read: /plan/research/google-workspace-stragetic-document.md
Fill: /plan/research/strategic-context-to-course-design-bridge.md
Save as: /plan/research/content-review-[your-topic].md
```

**Step 3 - Create Course:**
```
Use Task tool with:
  subagent_type: "adult-training-course-writer"
  prompt: [contents of prompt-course-content-creation-v2.md]
  (include the two input file paths in the prompt)
```

---

## Example Input Summary

| Step | What you type/input |
|------|---------------------|
| 1 | "Google Workspace with AI Microlearning Course" |
| 2 | "Mid-market, 300-1000 employees, 13.7 hrs/year learning budget, 30-min sessions, ROI pain point" |
| 3 | File paths: google-workspace-stragetic-document.md + content-review-google-workspace.md + output folder |

---

Want me to create a simple checklist file you can follow for each new topic?
