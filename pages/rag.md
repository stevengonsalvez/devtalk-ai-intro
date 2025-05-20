<h2 style="color: #046b79; font-weight: bold;">4.5 RAG: Retrieval Augmented Generation</h2>
<div class="my-4"></div>

<table class="w-full text-sm">
  <tr>
    <td class="align-top w-3/5 pr-8" style="font-size: 0.92em;">
      <ul class="list-disc ml-5">
        <li>
          <span class="font-bold">What is RAG?</span>
          <ul class="list-disc ml-5">
            <li>A technique to provide LLMs with external, up-to-date, or proprietary knowledge.</li>
            <li>
              <span class="font-bold">Process:</span>
              <ol class="list-decimal ml-6">
                <li>User asks a question.</li>
                <li>System <em>retrieves</em> relevant documents/data from a knowledge base (often using VectorDBs).</li>
                <li>This retrieved context is added to the original prompt.</li>
                <li>LLM <em>generates</em> an answer based on both the original query and the retrieved context.</li>
              </ol>
            </li>
          </ul>
        </li>
        <li>
          <span class="font-bold">Benefits:</span>
          <ul class="list-disc ml-5">
            <li>Access to current information (beyond training data).</li>
            <li>Reduces hallucinations by grounding responses in facts.</li>
            <li>Enables domain-specific knowledge (e.g., your company's internal docs, your project's codebase).</li>
          </ul>
        </li>
      </ul>
    </td>
    <td class="align-top w-2/5 pl-2">
      <div class="flex flex-col items-center mt-[-1.5rem]">
        <img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*1o5eUMIbInZDd6nIOZvDDw.png" class="rounded-lg shadow-lg mb-2" alt="RAG Diagram" style="max-width: 320px; width: 100%; height: auto;"/>
        <img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*ONHNE0v_MNhrOHWPWh6p5w.png" class="rounded-lg shadow-lg" alt="RAG Diagram" style="max-width: 320px; width: 100%; height: auto;"/>
        <p class="text-xs text-center mt-2">Simplified RAG Architecture</p>
      </div>
    </td>
  </tr>
</table>

<div class="my-4"></div>

:: HIDE ::
:: NOTES ::
(2 mins)
RAG, or Retrieval Augmented Generation, is a game-changer for making LLMs more useful and factual.
It's a fancy way of saying: "Let the LLM search a specific knowledge base before answering."
The process is simple: user asks, system finds relevant info from a source (like your company's wiki, or your codebase via a vector DB), adds that info to the prompt, and then the LLM answers.
This helps with several problems: LLMs don't know very recent events, they don't know your private data, and they can hallucinate. RAG grounds them.
Now, specific to us developers: your codebase itself is a massive source of context! You can RAG codebases easily