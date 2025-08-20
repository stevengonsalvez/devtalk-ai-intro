---
layout: cover
class: text-center
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%)
---

# AI Roundup: Just one more prompt!
## From Prompts to Production-Ready Agentic Systems

<div class="pt-12">
  <span class="px-2 py-1 rounded bg-primary bg-opacity-20">DevTalk</span>
  <span class="px-2 py-1 rounded bg-secondary bg-opacity-20">steven gonsalvez</span>
  <div class="mt-4 text-sm text-gray-500">
    <a href="https://github.com/stevengonsalvez/devtalk-ai-intro" target="_blank" rel="noopener">
      View this slide deck at github.com/stevengonsalvez/devtalk-ai-intro
    </a>
  </div>
</div>

:: HIDE ::
:: NOTES ::
Welcome everyone! Today, we're diving into the exciting world of AI, specifically focusing on how we can move beyond just "vibing" with cool demos to becoming "Engineering Vibists" – folks who build robust, scalable, and truly useful AI-powered applications.

The goal isn't just to use AI, but to use it *smartly*. We'll cover the basics, explore agentic systems, and then really dig into the practical aspects of making AI work for us in software development. Let's get started!

Error: Raw mode is not supported on the current process.stdin, which Ink uses as input stream by default.
Read about how to prevent this error on https://github.com/vadimdemedes/ink/#israwmodesupported
    at handleSetRawMode (file:///home/claude-user/.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:807:3853)
    at file:///home/claude-user/.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:816:259
    at eF (file:///home/claude-user/.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:332:21530)
    at oX (file:///home/claude-user/.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:332:41141)
    at file:///home/claude-user/.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:332:39313
    at XF0 (file:///home/claude-user/.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:326:8828)
    at Immediate.DF0 [as _onImmediate] (file:///home/claude-user/.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:326:9247)
    at process.processImmediate (node:internal/timers:483:21)
╭──────────────────────────╮
│ ✻ Welcome to Claude Code │
╰──────────────────────────╯


  ERROR  Raw mode is not supported on the current process.stdin, which Ink uses as input stream by default.
        Read about how to prevent this error on https://github.com/vadimdemedes/ink/#israwmodesupported

 - Read about how to prevent this error on https://github.com/vadimdemedes/ink/#israwmodesupported
 - handleSetRawMode (.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:807:3853)
 -  (.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:816:259)
 - eF (.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:332:21530)
 - oX (.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:332:41141)
 -  (.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:332:39313)
 - XF0 (.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:326:8828)
 - Immediate.DF0 (.npm-global/lib/node_modules/@anthropic-ai/claude-code/cli.js:326:9247)
 - process.processImmediate (node:internal/timers:483:21)
<div class="mt-8 columns-2 gap-8">

- **What are AI Agents?** Systems that can perceive their environment, make decisions, and take actions to achieve specific goals.
- **Agentic Workflows:** Sequences of tasks orchestrated by one or more agents.
  - Think: Plan → Execute → Observe
    - If needed, branch or loop: Adjust Plan → Execute → Observe
    - Multiple tasks or agents can run in parallel, merge results, and continue
- **Types of Agents:**
  - **Chat Agents:** Conversational (e.g., ChatGPT, Claude). Great for Q&A, summarization, brainstorming.
  - **Autonomous Agents:** More proactive, can operate with less direct human intervention (trading systems, customer service chatbots). Can use tools, access internet.
- **Frameworks (Orchestrators):**
  - LangChain / LangGraph: Building blocks & graphs for complex agentic chains.
  - AutoGen: Multi-agent conversation framework.
  - CrewAI: Role-playing agent crews for collaborative tasks.
  - ...and many more! They help manage state, tools, and agent interactions.

</div>

:: HIDE ::
:: NOTES ::
(4-5 mins)
So, Generative AI gives us the "brain." Agents give that brain "hands and feet."
An agent isn't just a model; it's a system designed to *do* things.
Agentic workflows are where the real power comes in – breaking down a complex problem into steps that an agent (or multiple agents) can tackle.
Chat agents are what most of us are familiar with. You give a prompt, it gives a response.
Autonomous agents take this further. They can be given a high-level goal and attempt to achieve it by performing multiple steps, even using external tools or information.
Frameworks like LangChain, AutoGen, and CrewAI provide the plumbing to build these more sophisticated systems. They handle things like:
- How agents communicate.
- How they access and use tools (like a calculator, a search engine, or your codebase).
- How they remember previous steps (memory).
This is moving from just generating text to accomplishing complex tasks.
