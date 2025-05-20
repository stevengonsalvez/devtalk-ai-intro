<div class="p-0 rounded-lg shadow-lg" style="background: #111;">
  <table class="w-full">
    <thead>
      <tr>
        <th colspan="2" class="text-xl font-extrabold py-3" style="color: #e5ec03; background: #111; text-shadow: 1px 1px 0 #046b79;">
          4.4 Context: The Secret Sauce <span class="text-lg">🧂</span> (and the Achilles Heel <span class="text-lg">🦶)</span>
        </th>
      </tr>
    </thead>
    <tbody class="text-[0.95rem]">
      <tr>
        <td class="align-top w-3/5 p-5" style="color: #fff; font-size: 0.65rem;">
          <ul class="list-disc ml-5">
            <li>
              Context is everything for LLMs. 🧠 The right info = magic. Too much = confusion. The difference between a great answer and a hallucination is often just the right context.
            </li>
            <li>
              Benchmarks show: More context isn’t always better—too much = chaos, too little = missed connections. The sweet spot is targeted, relevant info.
            </li>
            <li>
              How do tools help you hit that sweet spot?
              <ul class="ml-5 list-[circle]">
                <li>
                  <span class="font-semibold">Vector DBs 📚:</span> Store code, docs, and data as embeddings. Fetch only what’s relevant to your query using NN style. (cursor, windsurf etc)
                </li>
                <li>
                  <span class="font-semibold">Tree-sitter + Search 🌳🔍:</span> Use Tree-sitter to build a detailed syntax tree of your codebase—this lets tools understand code structure (functions, classes, variables) in any language. Combine with search to precisely extract and inject only the most relevant code snippets or definitions for your task. (cline, roo, aider)
                </li>
                <li>
                  <span class="font-semibold">Human-powered 🧑‍💻:</span> You curate what matters most. As an engineer - your judgment is still the best filter.
                </li>
                <li>
                  <span class="font-semibold">Hybrid approaches:</span> Mix automated retrieval with manual curation for best results, especially on complex projects.
                </li>
                <li>
                  <span class="font-semibold">Codebase as Context:</span> Tools like Repomix, ClaudeSync, and GitIngest help process and index your entire codebase so LLMs can search and understand it directly. This lets the LLM answer questions using your actual code—like how to use a dependency, or how a function works—rather than relying only on docs.
                </li>
              </ul>
            </li>
          </ul>
        </td>
        <td class="align-top w-1/3 p-4" style="font-size: 0.595rem;">
          <div class="flex flex-col items-center justify-center">
            <div class="rounded-full bg-[#222] p-2 mb-3 shadow-lg border-4 border-[#e5ec03]">
              <span class="text-2xl" style="color: #e5ec03;">🤯</span>
            </div>
            <div class="text-center font-semibold" style="color: #e5ec03; font-size: 0.7rem;">
              Too much context?<br>
              <span class="italic">LLM brain melts.</span>
            </div>
            <div class="mt-4 text-center text-xs text-gray-400" style="font-size: 0.595rem;">
              Sweeping rewrite or just a padding fix?<br>
              <span class="text-[#e5ec03]">Context, context, context.</span>
            </div>
            <div class="mt-6 p-2 rounded bg-[#222] text-[#e5ec03] text-xs font-mono w-full" style="font-size: 0.595rem;">
              <span>🧑‍🔬 Geek Corner:</span><br>
              <span>Context window = LLM’s memory.<br>
              Too much? <span class="italic">Token soup.</span><br>
              Too little? <span class="italic">Hallucination city.</span></span>
            </div>
            <div class="mt-3 p-2 rounded bg-[#046b79] text-[#e5ec03] font-semibold text-xs w-full" style="font-size: 0.595rem;">
              <span>Pro Tips 💡:</span>
              <ul class="list-disc ml-4">
                <li>No context injection? Paste a <code>tree</code> of your project or describe folders/files.</li>
                <li>Structure helps, iterate to provide files</li>
                <li>keep clearing irrelvant context</li>
              </ul>
            </div>
          </div>
        </td>
      </tr>
    </tbody>
  </table>
</div>

:: HIDE ::
:: NOTES ::
(2 mins)
Now, specific to us developers: your codebase itself is a massive source of context!
Tools like Repomix, or concepts like Claudesync (syncing files to Claude) or Gitingest , are about making your codebase LLM-friendly.
Think about it: how many times have you figured out how to use a library by looking at existing code rather than the official docs? LLMs can benefit from this too if we give them the right access. This is a key part of an "Engineering Vibist's" toolkit.