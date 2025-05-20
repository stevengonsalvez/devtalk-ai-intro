<h2 style="color: #046b79; font-size: 1.6rem; font-weight: bold;">4.6 Tools: Giving AI Superpowers</h2>
<div style="margin-top: 1.5rem; font-size: 0.95rem; gap: 1.5rem; display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); align-items: start;">
  <div>
    <ul style="list-style-type: disc; margin-left: 1rem;">
      <li>
        <strong>How do LLMs use tools - its called function calling</strong>
        <ul style="list-style-type: disc; margin-left: 1rem;">
          <li>Tools declare functions, including their signatures (name, parameters, types).</li>
          <li>These function signatures are passed to the LLM.</li>
          <li>The LLM chooses the right function and fills in the right parameters for the task at hand.</li>
          <li>The LLM sends this invocation data (function name and arguments) to the client.</li>
          <li>The client executes the function and returns the result.</li>
        </ul>
      </li>
      <li>
        <strong>LLMs never run code or access tools directly—they only suggest what to call. The client is responsible for execution and safety.</strong>
      </li>
      </ul>
  </div>
  <div>
    <ul style="list-style-type: disc; margin-left: 1rem;">
      <li>
        <p><strong>Why is this powerful?</strong> LLMs can trigger real actions in your environment, not just generate text.</p>
      </li>
      <li>
        <p><strong>Key challenge:</strong> How do we define and expose our own tools, and keep things safe? (See next slide!)</p>
      </li>
    </ul>
    <div style="margin-top: 1rem;">
      <img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*4fEPg2xuxCMrVP8E5FR2dw.png" alt="LLM Tools Diagram" style="max-width: 100%; border-radius: 0.5rem; box-shadow: 0 2px 8px rgba(0,0,0,0.08);" />
    </div>
  </div>
</div>


:: HIDE ::
:: NOTES ::
(1.5 mins)
This section is about **function calling**—the real mechanism behind "tools" for LLMs. LLMs don't run your code; they just output a function name and parameters, and the client (like Amazon Q, Copilot Workspace, or your own app) decides what to do. Embedded tools are just pre-defined, trusted functions the platform exposes. Custom tools are possible—how to do that is next.
