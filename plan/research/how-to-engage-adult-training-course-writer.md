To engage with the `adult-training-course-writer` agent in this Kilo Code environment, follow this workflow:

## Prerequisites

**Before invoking this agent, you must have:**
- A completed **Strategic Context Document** from the `industry-research-expert` agent (contains your research findings on the topic)

## Invocation Method

Type the slash command in the chat:

```
/adult-training-course-writer
```

## Required Input Format

After invoking, specify:

**Mode A: Course Creation**
```
Mode A. Module [X] of [N]. Using the research above, create a [duration] module on '[topic]' for [target audience].
```

Required parameters:
| Parameter | Description |
|-----------|-------------|
| Topic | The subject matter |
| Target audience | Who will attend (e.g., "compliance officers", "HR managers") |
| Learning objectives | Specific outcomes using action verbs |
| Duration | Total time for the module |
| Research findings | Reference to your Strategic Context Document |

**Mode B: Marketing Generation**
```
Mode B. Generate marketing collateral using the completed course.
```
*Only available AFTER all modules are approved.*

## Workflow Sequence

```
1. Research (industry-research-expert) → produces Strategic Context Document
2. Course Creation (adult-training-course-writer Mode A)
   └── Module 1: Anchor → approve → HTML → approve
   └── Module 2: Anchor → approve → HTML → approve
   └── ... repeat for all modules
3. Marketing (adult-training-course-writer Mode B)
   └── One-Pager → Overview → Landing Page
```

## Current State

You currently have `adult-training-course-writer.md` open (the agent definition file). To actually engage the agent, switch to the chat interface and use the `/adult-training-course-writer` command with your specific request.
