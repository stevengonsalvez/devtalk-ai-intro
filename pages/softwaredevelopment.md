---
layout: cover
background: https://images.unsplash.com/photo-1478760329108-5c3ed9d495a0?q=80&w=1548&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D # A very dark AI/technology themed image
---

## 3. AI and agents in Software Development: Beyond Code Gen

<div class="mt-8 columns-2 gap-8">

<div class="text-sm">

- **Augmented Development:** AI as a pair programmer, a design assistant, a test automator, a documentation writer.
- **Agentic Software Development:**
  - **Vision:** AI agents assisting or even autonomously handling parts of the development lifecycle.
  - **Examples:**
    - An agent that can:
      - Write code from prompts, images, or Figma designs.
      - Generate and run tests for new or changed code.
      - Build and run the application.
      - Fix type errors automatically.
      - Access and interact with the running web application.
      - Stream logs from both terminal and browser console.
      - Identify, diagnose, and fix problems as they arise.
      - Commit code, raise pull requests, and review PRs—repeating this cycle as needed.
      - Access monitoring tools like Sentry or Dynatrace, investigate issues, and fix code based on real errors.
      - See and understand your database schema, write and validate queries, and check your data.
      - Search the internet for the latest documentation or best practices.
      - Always keep a human in the loop to interrupt, control, or interrogate the agent at any step—think <span class="font-bold text-primary-600 italic">Pair Programmer</span>
- **The Shift:** From "AI writes code snippets" to "AI participates in the development *process*."
  - This requires more than just a good LLM; it requires thoughtful integration and workflow design.
  - This is where the "Engineering Vibist" mindset shines.

</div>

</div>


:: HIDE ::
:: NOTES ::
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

# 4. Key Parts to "crafting" Like an Engineer

## Mastering the Craft of AI Integration

From "Amateur Viber" to "Engineering Craftsman":

<div class="grid grid-cols-2 gap-8 items-start">

  <div>
    <div class="font-bold text-lg mb-2 text-primary-700">Amateur Viber</div>
    <div>
      Experiments with AI by tossing in prompts and seeing what comes out. Cares most about the UI and the surface, often ignoring structure, process, or deeper engineering. Treats AI like a magic 8-ball: ask, get something, move on.
    </div>
  </div>

  <div>
    <div class="font-bold text-lg mb-2 text-primary-700">Software Craftsman</div>
    <div>
      Composes software with massive aid from tools—treats AI as a collaborator. Uses prompts, context, and structure to guide the AI, integrating its output into robust workflows and systems.
    </div>
  </div>

</div>

<div class="my-6 border-t border-gray-300"></div>

<div class="text-center mb-4">
  <span class="font-semibold">Whichever role you are, the main challenge is taming this beast: increasing precision, reducing hallucination.</span>
</div>

<div class="flex flex-row justify-center gap-4">
  <div style="background-color: #046b79; color: #e5ec03;" class="rounded px-4 py-2 font-semibold">Tasks</div>
  <div style="background-color: #046b79; color: #e5ec03;" class="rounded px-4 py-2 font-semibold">Prompts</div>
  <div style="background-color: #046b79; color: #e5ec03;" class="rounded px-4 py-2 font-semibold">Rules</div>
  <div style="background-color: #046b79; color: #e5ec03;" class="rounded px-4 py-2 font-semibold">Context</div>
    <div style="background-color: #046b79; color: #e5ec03;" class="rounded px-4 py-2 font-semibold">RAG</div>
  <div style="background-color: #046b79; color: #e5ec03;" class="rounded px-4 py-2 font-semibold">Tools</div>
</div>

:: NOTES ::
From the earliest days—whether you used Emacs, Vim, or a modern IDE, or even nothing at all—tools have always shaped how we build software. Frameworks, libraries, and now AI assistants are just the next leg in this evolution. The real work is in harnessing these tools to increase precision and reliability, and to reduce hallucination or error, no matter your approach.



