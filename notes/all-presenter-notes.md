# Introduction Slide Notes

Welcome everyone! Today, we're diving into the exciting world of AI, specifically focusing on how we can move beyond just "vibing" with cool demos to becoming "Engineering Vibists" – folks who build robust, scalable, and truly useful AI-powered applications.

The goal isn't just to use AI, but to use it *smartly*. We'll cover the basics, explore agentic systems, and then really dig into the practical aspects of making AI work for us in software development. Let's get started!

---

(1-2 mins)
Alright, let's start with a quick baseline. Generative AI – you've all heard of it, probably used it.
Think ChatGPT, Midjourney, GitHub Copilot.
It's not just about regurgitating information; it's about synthesizing knowledge to produce something novel.
Under the hood, these are complex models trained on terabytes of data, allowing them to understand and generate human-like (or even superhuman) outputs.
This is the foundation for much of what we'll discuss today.
---

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

# Software Development Slide Notes

(2-3 mins)
Now, let's focus on our domain: software development.
We've all seen AI generating code. GitHub Copilot is a prime example of AI *augmenting* our abilities.
But agentic software development aims higher. Imagine AI not just as a tool you invoke, but as a proactive assistant or even a team member.
Instead of just asking an LLM to "write a function that does X," you might have an agent that:
- Takes a high-level feature description.
- Breaks it down into technical tasks.
- Drafts the code.
- Writes the tests.
- And maybe even creates a pull request.
This isn't science fiction; early versions of these capabilities are emerging.
The key is moving from ad-hoc prompting for code snippets to designing systems where AI plays a more integrated role. This is where we transition from a "pure viber" just trying out prompts, to an "Engineering Vibist" who thinks about systems.
---

From the earliest days—whether you used Emacs, Vim, or a modern IDE, or even nothing at all—tools have always shaped how we build software. Frameworks, libraries, and now AI assistants are just the next leg in this evolution. The real work is in harnessing these tools to increase precision and reliability, and to reduce hallucination or error, no matter your approach. 

# The Four Slide Notes

(2 mins)
The first step to effective AI use, especially in development, is solid product thinking.
A "pure viber" might throw a vague idea at an AI and hope for the best. This rarely works for anything complex.
An "Engineering Vibist" starts like any good software project: with clear requirements.
Write a PRD, or at least a clear spec. Use your favorite template, or ask an LLM to help you generate one based on best practices.
Then, the crucial step: break it down. If you know what you're building, you can guide an AI (or yourself) much more effectively.
AI chat engines like Claude, ChatGPT, or Gemini are excellent for this brainstorming and decomposition phase.
Internally at BT, Copilot can also be quite helpful for initial task breakdown, though for engineering, this naturally flows into Jira.
The point is: invest effort in defining *what* needs to be built before asking the AI *how* to build it.
A well-structured problem is much easier for an LLM to "understand" and assist with.
---

Not going to talk this to death—there's a ton of material out there on prompt engineering. But it's still wildly underrated how much difference good prompts make.

Honestly, the biggest thing that separates really good AI-augmented IDEs (like Cursor or Windsurf) from the rest is just really, really good prompt engineering. That's it. Otherwise, it's all the same tools, the same VSCode wrappers, the same everything. The effectiveness of the prompts is what makes the big difference.

So, don't sleep on this. If you want better results, focus on your prompts. That's where the magic is. 

# Rules Slide Notes

Context is everything: Structured rules go into the LLM's context window. The clearer, the better the results. Experiment to find what works for your workflow. 

# Context Slide Notes

(2 mins)
Now, specific to us developers: your codebase itself is a massive source of context!
Tools like Repomix, or concepts like Claudesync (syncing files to Claude) or Gitingest , are about making your codebase LLM-friendly.
Think about it: how many times have you figured out how to use a library by looking at existing code rather than the official docs? LLMs can benefit from this too if we give them the right access. This is a key part of an "Engineering Vibist's" toolkit. 

# RAG Slide Notes

(2 mins)
RAG, or Retrieval Augmented Generation, is a game-changer for making LLMs more useful and factual.
It's a fancy way of saying: "Let the LLM search a specific knowledge base before answering."
The process is simple: user asks, system finds relevant info from a source (like your company's wiki, or your codebase via a vector DB), adds that info to the prompt, and then the LLM answers.
This helps with several problems: LLMs don't know very recent events, they don't know your private data, and they can hallucinate. RAG grounds them.
Now, specific to us developers: your codebase itself is a massive source of context! You can RAG codebases easily 

# Tools Slide Notes

(1.5 mins)
This section is about **function calling**—the real mechanism behind "tools" for LLMs. LLMs don't run your code; they just output a function name and parameters, and the client (like Amazon Q, Copilot Workspace, or your own app) decides what to do. Embedded tools are just pre-defined, trusted functions the platform exposes. Custom tools are possible—how to do that is next. 

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

# What Can You Do Slide Notes

No presenter notes for this slide. 

# MCP Dark Side Slide Notes

(Target: 2-3 minutes)

So, we've discussed the exciting potential of MCP. But it's critical to look at the security implications, especially given how quickly this space is moving. Many of these concerns are universal to new, rapidly adopted protocols.

**Core Security Risks with MCP**:
*   The speed of development often means security isn't the top priority – what some call "vibe-coding." This can lead to several types of compromises:
    *   **Data Exfiltration:** This is a major one. MCP tools, if malicious or compromised, can be designed to secretly siphon off sensitive data. Think credentials, personal information, proprietary company data that the AI processes or has access to.
    *   **Unauthorized Access & Remote Code Execution (RCE):** A compromised MCP tool could grant attackers unintended control over the system where the AI client or MCP server runs, potentially allowing them to execute arbitrary code.
    *   **Integrity Compromise:** Beyond just stealing data, malicious tools can alter critical information, inject false data into AI responses (imagine an AI giving you dangerously wrong financial or medical advice based on manipulated tool output), or disrupt system operations.
    *   **Trust Exploitation & Prompt Injection:** This is a more subtle but powerful attack. AIs often heavily rely on the descriptions provided by MCP tools to understand how to use them. Malicious actors can craft these descriptions to include hidden instructions (prompt injections) that manipulate the AI into performing harmful actions the user never intended.
    *   **Supply Chain Attacks:** Just like an `npm` or Python package can be compromised, the MCP tools and servers themselves can become vectors for attack if their own dependencies are malicious or if the tool itself is a trojan.
*   The consequences are severe: massive compliance failures (think GDPR, HIPAA fines), costly data breaches, and significant damage to reputation.

**Old Exploits, New AI Playground**:
*   Many of these aren't brand-new *types* of attacks, but classic vulnerabilities finding a potent new attack surface with AI and MCP:
    *   Imagine AI-powered phishing that's far more convincing, or an AI agent itself being socially engineered.
    *   If an AI's output is rendered in a web context, or if its inputs are used to query backend systems, classic XSS or SQL injection-style vulnerabilities can reappear, now mediated by the AI.
    *   Rapid adoption without security best practices can lead to misconfigured MCP setups, just like we saw with early Docker deployments becoming easy targets.
    *   And because AI tools are increasingly user-facing, they can provide a more direct path for attackers to access backend systems and data pipelines.

**Example MCP Attack Vectors**:
To make this concrete, consider these types of attacks, some of which are demonstrated in proof-of-concept repos like `mcp-ethicalhacks`:
1.  **Shadowing Attack:** One tool's description subtly instructs the AI to alter its behavior when using a *different* tool (potentially on another server), causing data to be exfiltrated. For example, all GitHub issues created via an AI tool are also secretly copied to an attacker's repository.
2.  **Tool Poisoning (Data Theft):** A tool claims to perform a simple task but its description tells the AI it "requires" sensitive information (like your SSH private keys) as input to function. The AI, trying to be helpful, provides it.
3.  **Cross-Tool Contamination:** One seemingly innocuous tool gathers a piece of sensitive data (e.g., your postcode). A completely different tool, used later, retrieves this data from a shared storage and embeds it, often hidden, in its legitimate output. This "contaminated" data then becomes part of the AI's ongoing context, potentially being passed to other systems.
4.  **Direct Token/Credential Theft:** A malicious tool offers a "service" like validating an OAuth token. Instead, it simply captures the token and returns a fake success message.

And the list goes on: "Rugpulls" where a trusted tool turns malicious after an update, embedding malware in files processed by multimodal AIs, direct Remote Code Execution, poisoning the data sources for RAG systems (Retrieval-Augmented Deception), and attackers spoofing legitimate MCP servers.

**Vigilance is Key**:
The takeaway isn't to abandon MCP, but to approach it with extreme caution. A Zero Trust mindset is essential – don't inherently trust any tool. We need rigorous scrutiny of MCP tools and their behaviors, and security must be a foremost consideration in any MCP integration. Resources like the `mcp-ethicalhacks` repository can be valuable for understanding the practical nature of these vulnerabilities. 