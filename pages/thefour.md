## 4.1 Product Management: Think Product, Not Just Prompt

- **Don't just start prompting away— Do Proper Software Engineering:**

  <span class="text-sm text-gray-600 mb-4 block">
    Define requirements (PRDs, Epics, Features) → Design architecture → Write tests → Implement code → Review & refactor → Deploy & monitor. AI augments each step, but doesn't replace the discipline. Structure beats chaos, even with the smartest AI.
  </span>

<ul class="space-y-4 text-sm">
  <li class="transition-transform duration-300 hover:scale-105 flex items-center">
    <span class="animate-bounce text-xl mr-2">🤖</span>
    LLMs (ChatGPT, Gemini, Claude—pick your favorite) are fantastic at helping you draft and iterate on PRDs. Go back and forth until you actually like what you see.
  </li>
  <li class="transition-transform duration-300 hover:scale-105 flex items-center">
    <span class="animate-spin text-xl mr-2">🪄</span>
    Once you have a PRD, break it down into small, manageable chunks. This is classic software engineering—no different from how you’d tackle any project.
  </li>
  <li class="transition-transform duration-300 hover:scale-105 flex items-center">
    <span class="animate-pulse text-xl mr-2">🧩</span>
    If you’re not used to breaking things down, there are plenty of tools (see appendix) that can help you turn big ideas into bite-sized tasks.
  </li>
  <li class="transition-transform duration-300 hover:scale-105 flex items-center">
    <span class="animate-bounce text-xl mr-2">🗂️</span>
    For engineers, some of these tools might feel like overkill—use your judgment. The key is to organize: use GitHub issues, Todoist, Linear, Jira, whatever works for you. Structure your work, or frustration will hit fast.
  </li>
  <li class="transition-transform duration-300 hover:scale-105 flex items-center">
    <span class="animate-pulse text-xl mr-2">✅</span>
    Then, go task by task, marking things off and iterating as you go. That’s probably how you build anything AI or not.
  </li>
</ul>

:: HIDE ::
:: NOTES ::
(2 mins)
The first step to effective AI use, especially in development, is solid product thinking.
A "pure viber" might throw a vague idea at an AI and hope for the best. This rarely works for anything complex.
An "Engineering Vibist" starts like any good software project: with clear requirements.
Write a PRD, or at least a clear spec. Use your favorite template, or ask an LLM to help you generate one based on best practices.
Then, the crucial step: break it down. If you know what you're building, you can guide an AI (or yourself) much more effectively.
AI chat engines like Claude, ChatGPT, or Gemini are excellent for this brainstorming and decomposition phase.
Internally, Copilot can also be quite helpful for initial task breakdown, though for engineering, this naturally flows into Jira.
The point is: invest effort in defining *what* needs to be built before asking the AI *how* to build it.
A well-structured problem is much easier for an LLM to "understand" and assist with.
---
layout: cover
background: https://images.unsplash.com/photo-1484950763426-56b5bf172dbb?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

## 4.2 Prompts: Your Dialogue with AI

<div class="mt-6"></div>

<div class="grid grid-cols-2 gap-6 items-start">
  <div>
    <div class="grid grid-cols-2 rounded-lg overflow-hidden shadow-lg mb-4">
      <div style="background-color: #046b79; color: #e5ec03;" class="p-4 text-sm font-semibold">
        <div class="mb-2 text-lg">Prompt Engineering Essentials</div>
        <table class="w-full text-left text-xs">
          <tbody>
            <tr>
              <td class="pr-2 align-top">🎯</td>
              <td>Define the goal</td>
            </tr>
            <tr>
              <td class="pr-2 align-top">📝</td>
              <td>Specify the output format</td>
            </tr>
            <tr>
              <td class="pr-2 align-top">⚠️</td>
              <td>Set warnings for accuracy</td>
            </tr>
            <tr>
              <td class="pr-2 align-top">📚</td>
              <td>Provide context</td>
            </tr>
            <tr>
              <td class="pr-2 align-top">🔍</td>
              <td>Be specific and detailed</td>
            </tr>
            <tr>
              <td class="pr-2 align-top">💡</td>
              <td>Use examples</td>
            </tr>
            <tr>
              <td class="pr-2 align-top">🔁</td>
              <td>Iterate and refine</td>
            </tr>
          </tbody>
        </table>
      </div>
      <div style="background-color: #e5ec03; color: #046b79;" class="p-4 text-sm font-semibold">
        <div class="mb-2 text-lg">How to Apply</div>
        <ul class="space-y-2">
          <li><span class="font-bold">Be clear:</span> Say exactly what you want.</li>
          <li><span class="font-bold">Give context:</span> Add any needed background.</li>
          <li><span class="font-bold">Set a role:</span> "You are a Python expert."</li>
          <li><span class="font-bold">Show examples:</span> Demonstrate the format.</li>
          <li><span class="font-bold">Add constraints:</span> "Reply in JSON."</li>
          <li><span class="font-bold">Iterate:</span> Tweak and improve as you go.</li>
        </ul>
      </div>
    </div>
  </div>
  <div>
    <div style="background-color: #fffbe6; color: #046b79;" class="p-4 text-sm font-semibold rounded-lg shadow-lg">
      <div class="mb-2 text-lg">Vibe and Manage Your Prompts</div>
      <ul class="space-y-2">
        <li>
          <span class="font-bold">Vibe Your Prompts (Iterate!):</span>
          <ul class="list-disc ml-5">
            <li>Ask your LLM to create a prompt using a clear structure (if you don't have your own, use the one on the left).</li>
            <li>
              Go full vibe on your prompt first—it's the difference between playing Tetris on a Game Boy and trying to stack random shapes in a cardboard box.
            </li>
          </ul>
        </li>
        <li>
          <span class="font-bold">Manage Your Prompts:</span>
          <ul class="list-disc ml-5">
            <li>Don't let good prompts get lost in chat history.</li>
            <li>Store, version, and reuse effective prompts (prompt libraries, snippets).Treat them like code!</li>
            <li>Look in the appendix for some more tips</li>
            <li>
              brave? Go full prompt engineering! Run evals, compare across models, and experiment to find what works.
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</div>

:: HIDE ::
:: NOTES ::
Not going to talk this to death—there’s a ton of material out there on prompt engineering. But it’s still wildly underrated how much difference good prompts make.

Honestly, the biggest thing that separates really good AI-augmented IDEs (like Cursor or Windsurf) from the rest is just really, really good prompt engineering. That’s it. Otherwise, it’s all the same tools, the same VSCode wrappers, the same everything. The effectiveness of the prompts is what makes the big difference.

So, don’t sleep on this. If you want better results, focus on your prompts. That’s where the magic is.
