---
hide:
  - toc
---

# ADK Skills

Skills are self-contained units of functionality that ADK agents can use. An agent Skill encapsulates instructions, resources, and tools required for a task, based on the [Agent Skill specification](https://agentskills.io/specification).

## Coding Agent Integration

ADK ships as both a **Skill** and an **MCP server**, so coding agents like Claude Code and Gemini CLI can scaffold, extend, and test your agents automatically.

### As a Skill
Coding agents can load ADK as an AgentSkill to get context about the ADK API, patterns, and best practices.

### As an MCP Server
The ADK MCP server exposes tools for creating agents, adding tools, running evaluations, and more — all accessible from any MCP-compatible coding agent.

## Using Skills in Your Agents

Use the `SkillToolset` class to include Skills in your agent:

```python
from google.adk import Agent
from google.adk.skills import load_skill_from_dir
from google.adk.tools import skill_toolset

weather_skill = load_skill_from_dir("skills/weather_skill")
toolset = skill_toolset.SkillToolset(skills=[weather_skill])

agent = Agent(
    model="gemini-2.5-flash",
    name="skill_user",
    tools=[toolset],
)
```

!!! note "Experimental"
    The Skills feature is experimental. [Share feedback](https://github.com/google/adk-python/issues/new?template=feature_request.md&labels=skills).
