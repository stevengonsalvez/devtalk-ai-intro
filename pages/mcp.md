<h2 style="color: #046b79; font-size: 1.6rem; font-weight: bold;">5. Model Context Protocol (MCP)</h2>
<div style="margin-top: 1.5rem; font-size: 0.95rem; gap: 1.5rem; display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); align-items: start;">
  <div>
    <ul style="list-style-type: disc; margin-left: 1rem;">
      <li><strong>The "Wild West" of Tools</strong></li>
      <ul style="margin-left: 1rem;">
        <li>Every framework had its own tool format (LangChain, LlamaIndex, etc.)</li>
        <li>ChatGPT Plugins made tools mainstream, but created walled gardens</li>
        <li>Plugins lacked transparency, interoperability, and security</li>
      </ul>
      <li><strong>Why MCP?</strong></li>
      <ul style="margin-left: 1rem;">
        <li>Define a tool once, use it with any LLM or agent framework</li>
        <li>Clear, declarative format for what a tool does and needs</li>
        <li>Explicit permissions for better human controllability</li>
        <li>Smoother developer experience</li>
      </ul>
    </ul>
  </div>
  <div>
    <ul style="list-style-type: disc; margin-left: 1rem;">
      <li><strong>Why not just use APIs directly?</strong></li>
      <ul style="margin-left: 1rem;">
        <li>APIs are for humans and code, not LLMs</li>
        <li>MCPs act as wrappers around APIs, helping LLMs understand how to call them.</li>
        <li>Standardizes how LLMs discover, invoke, and get results from tools (apis) or commands</li>
        <li>Enables portability across agentic platforms</li>
      </ul>
      <li><strong>Vision</strong></li>
      <ul style="margin-left: 1rem;">
        <li>Define a tool once, use it with frameworks like langraph, autogen or developer tooling like cursor, windsurf or general AI chatbots claude desktop, goose.. anything and plug any LLM that supports function calling</li>
      </ul>
    </ul>
  </div>
</div>
<div style="margin-top: 1.5rem; padding: 0.2rem 1rem; background: #046b79; border-radius: 0.5rem; font-size: 0.92rem;">
  <strong>MCP is not reinventing the wheel:</strong> It builds on existing ideas, but standardizes them for a more open and interoperable AI ecosystem.
</div>

:: HIDE ::
:: NOTES ::
(3 mins for this slide, 4 mins for next = 7 mins for MCP)
So, we've seen that LLMs can use tools. But historically, *how* you tell an LLM about a tool has been a bit of a mess.
LangChain had its way, LlamaIndex another. Then ChatGPT plugins and Custom GPTs came along – great for showing the potential, but they created walled gardens. A plugin for ChatGPT is just for ChatGPT. And often, you're just pointing it at an OpenAPI spec, which can be a security concern if not carefully managed, and lacks fine-grained control.
This is where the **Model Context Protocol (MCP)** comes in.
The goal is to create an open, standardized way to declare tools, resources, and other contextual information for LLMs.
Think of it like this: if you define a tool using MCP, you should ideally be able to use that same tool definition with different LLMs (like models from OpenAI, Anthropic, Google) and different agent frameworks (like LangGraph or AutoGen, if they adopt it).
This means more transparency in what the tool does, better security by being explicit about permissions and data, and a much smoother developer experience.
It's about moving from ad-hoc integrations to a more engineered, interoperable ecosystem for AI tools.
---
layout: cover
background: https://images.unsplash.com/photo-1533134486753-c833f0ed4866?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

<h2 style="color: #046b79; font-size: 1.6rem; font-weight: bold;">MCP Components: What Makes Up?</h2>
<div style="margin-top: 1.5rem; font-size: 0.95rem; gap: 1.5rem; display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); align-items: start;">
  <div>
    <ul style="list-style-type: disc; margin-left: 1rem;">
      <li><strong style="color: #e5ec03;">🛠️ Tools</strong>: Functions an LLM can call—these can be APIs, commands, data tools, or any thing encapsulated standard function.</li>
      <li><strong style="color: #e5ec03;">📦 Resources</strong>: Assets pretty much:  Data, files.. static stuff!</li>
      <li><strong style="color: #e5ec03;">💬 Prompts</strong>: Prompts , prompt templates that are related to the tool invocation</li>
      <li><strong style="color: #e5ec03;">🎛️ Sampling</strong>: Fairly new addition Controls for temperature, top-p, and other generation settings. Can dynamically control how clever and less precise or how pedantic and precise you want the LLM to be - eg: when you ask about "API integration" it may lower "creativity". It could do further more with adding bias to context etc.</li>
      <li><strong style="color: #e5ec03;">📑 Schemas</strong>: Structured definitions for inputs/outputs (validation, safety)</li>
    </ul>
  </div>
  <div>
    <ul style="list-style-type: disc; margin-left: 1rem;">
      <li><strong style="color: #e5ec03;">🔗 Connections: How do the clients call these thingies</strong>:</li>
      <ul style="margin-left: 1rem;">
        <li>Local (stdio/stdout): Run tools on your machine</li>
        <li>HTTP/SSE: Connect to remote APIs, support for server-sent events (like having two phones to chat to the same person - http one way and SSE the other) </li>
        <li>Fairly new : Streaming: Real-time data and responses - this is probably going to be the future</li>
      </ul>
      <li><strong style="color: #e5ec03;">🔐 OAuth support</strong>: Fairly new, Secure authentication for protected APIs and resources</li>
      <li>...and more (versioning, metadata, access control)</li>
    </ul>
  </div>
</div>
<div style="margin-top: 8.5rem; padding: 0.2rem 1rem; background:#e5ec03; color: #046b79; border-radius: 0.5rem; font-size: 0.92rem;">
  For a deep dive into MCP's ecosystem and evolving features, see the <a href="https://dev.to/stevengonsalvez/series/31579" style="color: #046b79; text-decoration: underline;">MCP Series on DEV</a>.
</div>

:: NOTES ::
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


---