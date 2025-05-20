---
layout: cover
class: text-center
background: https://source.unsplash.com/collection/94734566/1920x1080 # Or a cool AI-generated abstract
---

# AI Roundup: Time to Vibe!
## From Prompts to Production-Ready Agentic Systems

<div class="pt-12">
  <span class="px-2 py-1 rounded bg-primary bg-opacity-20">DevTalk</span>
  <span class="px-2 py-1 rounded bg-secondary bg-opacity-20">Your Name / Team</span>
</div>

:: HIDE ::
:: NOTES ::
Welcome everyone! Today, we're diving into the exciting world of AI, specifically focusing on how we can move beyond just "vibing" with cool demos to becoming "Engineering Vibists" – folks who build robust, scalable, and truly useful AI-powered applications.

The goal isn't just to use AI, but to use it *smartly*. We'll cover the basics, explore agentic systems, and then really dig into the practical aspects of making AI work for us in software development. Let's get started!
---

## 1. Generative AI: The Spark

<div class="grid grid-cols-2 gap-8 items-center">
<div>

- **What is it?** AI that *creates* new, original content.
  - Text, images, code, audio, video...
- **How?** Learns patterns from vast datasets.
- **Key Enablers:** Large Language Models (LLMs), Diffusion Models, GANs (Generative adversarial networks) - videos etc.
- **Impact:** Revolutionizing content creation, problem-solving, and automation.

</div>
<div>

<!-- You can use an image here, e.g., a collage of AI-generated art/text -->
<img src="https://images.unsplash.com/photo-1677756119517-756a188d2d94?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" class="rounded-lg shadow-lg max-h-80 mx-auto" alt="Generative AI concept"/>

</div>
</div>

:: HIDE ::
:: NOTES ::
(1-2 mins)
Alright, let's start with a quick baseline. Generative AI – you've all heard of it, probably used it.
Think ChatGPT, Midjourney, GitHub Copilot.
It's not just about regurgitating information; it's about synthesizing knowledge to produce something novel.
Under the hood, these are complex models trained on terabytes of data, allowing them to understand and generate human-like (or even superhuman) outputs.
This is the foundation for much of what we'll discuss today.
---

## 2. Enter the Agents: AI with Agency

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
---