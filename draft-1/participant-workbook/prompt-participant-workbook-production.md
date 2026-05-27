# Prompt: Participant Workbook Production

## Objective

Convert the participant workbook Markdown file into a formatted DOCX file suitable for Google Docs distribution, where participants can make a copy and fill in their own responses.

## Source Material

- **Source file:** `participant-workbook.md` (in the same folder as this prompt)
- **Anchor files:** Each module has an anchor file in `../modules/01-foundation-google-workspace/module-01.md` through `../modules/08-ai-integration-final-project/module-08.md`

## Output

- **Output file:** `participant-workbook.docx`
- **Script file:** `create_workbook_docx.py`

## Requirements

### Page Format
- Paper size: A4 (21cm × 29.7cm)
- Margins: 2cm top/bottom, 2.5cm left/right
- Font: System default (Calibri in Word, Google Docs handles font rendering)

### Pagination
Each major section must start on a fresh page:
- Module 1
- Module 2
- Module 3
- Module 4
- Module 5
- Module 6
- Module 7
- Module 8
- Course Reflection
- Notes Section

### Document Structure

```
COVER PAGE
- Title: "Google Workspace with AI" (Heading 1)
- Subtitle: "Participant Workbook" (Heading 2)
- Name: _______________________
- Date: _______________________
- Session: 1 of 8

MODULE TABLE
- Table listing all 8 modules with columns: Module, Topic, My Notes
- Leave "My Notes" column blank for writing

MY LEARNING GOALS
- 3 numbered lines with underscores for writing

MODULE 1 (starts new page)
- Session Objectives (bulleted list)
- The 5 Core Apps table (3 columns: App, My Purpose, Gemini Location)
- My First AI Prompts section (Gmail, Docs, Sheets lines)
- Session Notes (3 lines with underscores)
- Module 1 Compression Artifact (Gemini Hotkeys Quick Reference table)
- My Commitment section

MODULE 2 (starts new page)
- Session Objectives (bulleted list)
- Collaboration Modes table (Editing, Suggesting)
- My AI-Enhanced Comments section
- Session Notes
- Module 2 Compression Artifact (AI Collaboration Checklist with checkboxes)
- My Commitment section

MODULE 3 (starts new page)
- Session Objectives
- My Template Sections (5 numbered lines)
- AI Variation Results (Original + 3 variations)
- Session Notes
- Module 3 Compression Artifact (Template Starter Kit table)
- My Commitment section

MODULE 4 (starts new page)
- Session Objectives
- Research Synthesis (Topic, 3 Key Findings with Evidence, Source Conflicts)
- Session Notes
- Module 4 Compression Artifact (Research Workflow checklist)
- My Commitment section

MODULE 5 (starts new page)
- Session Objectives
- My AI-Generated Agenda (Meeting Type, 4 Agenda Items)
- Post-Meeting AI Extraction (Decisions Made, Action Items table with Owner/Due Date)
- Session Notes
- Module 5 Compression Artifact (Meeting Automation Script checklist)
- My Commitment section

MODULE 6 (starts new page)
- Session Objectives
- My AI Searches table (3 rows: Search route, Results, Accuracy)
- My Folder Structure (5 subfolder lines with ├── notation)
- Session Notes
- Module 6 Compression Artifact (Drive Organization System)
- My Commitment section

MODULE 7 (starts new page)
- Session Objectives
- My Repetitive Tasks table (4 columns: Task, Frequency, Time/Instance, Total Time)
- My Prompt Chain (Automation Name + 3 steps with Prompt/Output lines)
- Session Notes
- Module 7 Compression Artifact (Top 3 Automation Patterns)
- My Commitment section

MODULE 8 (starts new page)
- My AI Workspace Playbook
- Document Title line
- Workflow 1-5 templates, each containing:
  - Workflow name
  - Trigger
  - Apps Used
  - 5 Steps
  - Time Saved
  - 3 Gemini Prompt lines

COURSE REFLECTION (starts new page)
- Biggest Breakthrough (2 lines)
- Most Challenging Module (Module + Why lines)
- How I'll Continue Learning (2 lines)
- My Commitment to Continued Practice (This week, This month, This quarter)

NOTES SECTION (starts new page)
- 20 blank lines with underscores

FINAL MESSAGE
- Thank you message (centered, bold)
```

### Table Styling
- All tables should use `Table Grid` style (borders visible)
- Header row should be bold

### Checkbox Items
Use the unicode checkbox character: `☐`

### Fill-in Lines
Use underscores with spaces: `_________________________________`

### Divider Lines
Use em dash: `─` repeated 60 times: `─` * 60

## Python Script

The script should:
1. Import python-docx
2. Define helper functions: `set_cell_shading()`, `add_page_break()`
3. Set A4 page dimensions
4. Build the document section by section
5. Save to the output path

## Distribution Notes

Once the DOCX is created:
1. Upload to Google Drive
2. Right-click → Open with Google Docs
3. File → Make a Copy (participants do this themselves)
4. Participants fill in their own copy during the course