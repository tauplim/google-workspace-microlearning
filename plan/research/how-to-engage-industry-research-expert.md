To engage with the `industry-research-expert` agent, use the **Task tool** with `subagent_type="industry-research-expert"`.

## How to Invoke

1. **Use the Task tool** with these parameters:
   - `subagent_type`: `"industry-research-expert"`
   - `description`: Brief summary of the research topic (3-5 words)
   - `prompt`: Detailed description of what to research and what to return

2. **According to the workflow in AGENTS.md**, this agent should be used **first** before `adult-training-course-writer` for market/industry analysis.

## Example Usage

```json
{
  "subagent_type": "industry-research-expert",
  "description": "Research Google Workspace market trends",
  "prompt": "Research the current market trends for Google Workspace training in the corporate learning and development sector. Focus on: 1) Market size and growth projections, 2) Key competitors and their offerings, 3) Target audience demographics and pain points, 4) Pricing models in the microlearning space. Return a concise strategic context document with findings and recommendations."
}
```

## Research Agent Mode

This agent operates in **research advisory mode** and does not write code. Its output is analysis, not implementation. It will ask clarifying questions about the business decision your research is meant to inform before proceeding.
