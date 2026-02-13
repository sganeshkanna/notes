### The Art of System Context

To recap what we saw in the introduction to this course, system context (also known as a system prompt or system instructions) is the persistent context that defines your agent's identity and behavior. System context is typically included in every conversation turn you'll have with an LLM and tells it the following:

1.  Who it is (Role and identity)
2.  What it can do (Capabilities and tools)
3.  How it should behave (Personality and constraints)
4.  What it knows (Domain knowledge and context)

As you'll get to experience in this notebook and in your journey of building AI applications, setting system context can sometimes feel more of an art than a science. 

Anthropic shared some of their advice in what they find to be effective system prompts. In their guide on [Effective Context Engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents), Anthropic emphasizes that system prompts should be "extremely clear and use simple, direct language that presents ideas at the right altitude for the agent."

They describe this "right altitude" as a *Goldilocks Zone*:

> "At one extreme, we see engineers hardcoding complex, brittle logic in their prompts... At the other extreme, engineers sometimes provide vague, high-level guidance... The optimal altitude strikes a balance: specific enough to guide behavior effectively, yet flexible enough to provide the model with strong heuristics to guide behavior."

<img src="https://www.anthropic.com/_next/image?url=https%3A%2F%2Fwww-cdn.anthropic.com%2Fimages%2F4zrzovbb%2Fwebsite%2F0442fe138158e84ffce92bed1624dd09f37ac46f-2292x1288.png&w=3840&q=75" alt="Calibrating the system prompt" width="800"/>

*Image Source: Anthropic*

To achieve this balance, Anthropic recommends organizing prompts into distinct sections (like `<background_information>`, `<instructions>`, `## Tool guidance`, etc.) using XML tags or Markdown headers. 
