# MCP Slide Notes

(3 mins for this slide, 4 mins for next = 7 mins for MCP)
So, we've seen that LLMs can use tools. But historically, *how* you tell an LLM about a tool has been a bit of a mess.
LangChain had its way, LlamaIndex another. Then ChatGPT plugins and Custom GPTs came along – great for showing the potential, but they created walled gardens. A plugin for ChatGPT is just for ChatGPT. And often, you're just pointing it at an OpenAPI spec, which can be a security concern if not carefully managed, and lacks fine-grained control.
This is where the **Model Context Protocol (MCP)** comes in.
The goal is to create an open, standardized way to declare tools, resources, and other contextual information for LLMs.
Think of it like this: if you define a tool using MCP, you should ideally be able to use that same tool definition with different LLMs (like models from OpenAI, Anthropic, Google) and different agent frameworks (like LangGraph or AutoGen, if they adopt it).
This means more transparency in what the tool does, better security by being explicit about permissions and data, and a much smoother developer experience.
It's about moving from ad-hoc integrations to a more engineered, interoperable ecosystem for AI tools.
---

(Showcase: Loop MCP & Prompt Registry)

We're building out a real-world implementation of MCP called **Loop MCP**. It's an open-source reference implementation that demonstrates how to define, register, and use tools, resources, and prompts in a standardized way—across different LLMs and agent frameworks.

A key feature is the **Prompt Registry**: instead of scattering prompts and templates throughout your codebase, you register them centrally. This means:
- You can version, audit, and reuse prompts.
- Prompts are discoverable and can be linked to specific tools or workflows.
- You can swap out or update prompts without redeploying your whole app.

Loop MCP lets you:
- Define tools and resources in a single place.
- Register prompts and templates, and associate them with tools or tasks.
- Expose everything via a standard API (OpenAPI, JSON-RPC, etc).
- Plug into any LLM or agent framework that supports MCP.

This approach makes it much easier to build, maintain, and scale AI-powered systems—no more prompt spaghetti, and no more tool lock-in.

For more, check out the Loop MCP repo and see how the prompt registry works in practice!

So what does MCP actually look like? It's essentially a structured document, often JSON or YAML, that defines the "context" for an LLM.
Let's look at the key components with a simplified example:
tools: This is where you define the actual functions the LLM can call.
Each tool has a name (how the LLM refers to it).
A description (crucial for the LLM to understand when to use the tool).
And parameters defined using JSON Schema, telling the LLM what inputs the tool expects.
Optionally, you can also define the schema of what the tool returns.

resources: These describe external things the tools might need or interact with.
This could be an OpenAPI specification for an API the tool calls, a database schema, or even pointers to RAG knowledge bases.
It helps the LLM (and developers) understand the dependencies of the tools.

prompts: You can include pre-defined prompt segments.
This is great for system messages ("You are a helpful AI assistant that specializes in X..."), or few-shot examples to guide the LLM's responses when using certain tools or discussing certain topics.

samplingConfig: This allows you to specify default LLM generation parameters.
Things like temperature (creativity vs. determinism), topP, max_tokens. This helps ensure consistent behavior when this context is used. 