---
layout: default
---

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

# 4.3 Rules: Why Rules?

<div class="flex flex-col items-center justify-center min-h-[20vh]">

  <div class="flex-grow"></div>

  <table class="text-xs w-2/3 mx-auto">
    <caption class="text-xs text-gray-500">Why Rules? (The Basics)</caption>
    <thead>
      <tr>
        <th class="text-left">Purpose</th>
        <th class="text-left">Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Guardrailing</td>
        <td>Keep AI on topic, avoid unwanted output.</td>
      </tr>
      <tr>
        <td>Consistency</td>
        <td>Enforce styles, formats, and tone.</td>
      </tr>
      <tr>
        <td>Reducing Hallucinations</td>
        <td>Ground AI, limit "creative" errors.</td>
      </tr>
      <tr>
        <td>Focus</td>
        <td>Direct AI to the core task at hand.</td>
      </tr>
    </tbody>
  </table>

  <div class="flex-grow"></div>

</div>

---

# 4.3 Managing Rules: The Engineering Vibist's Way

<div class="my-8"></div>


<div class="grid grid-cols-2 gap-6 items-start">

  <div>
    <div class="mb-2 text-lg font-semibold text-primary-700">How to Structure Rules</div>
    <ul class="space-y-2 text-sm">
      <li>
        <span class="font-bold">Be explicit:</span> Make rules clear for both humans and LLMs.
      </li>
      <li>
        <span class="font-bold">Use structure:</span> Go beyond plain text—use fields and partitions.
      </li>
      <li>
        <span class="font-bold">Partition clearly:</span> Mark rule boundaries (e.g., <code>&lt;rule&gt;</code> tags).
      </li>
      <li>
        <span class="font-bold">Define fields:</span> Include name, description, filters, actions.
      </li>
      <li>
        <span class="font-bold">Add metadata:</span> Use frontmatter for globs, <code>alwaysApply</code>, etc.
      </li>
    </ul>
  </div>

  <div>
    <table class="text-xs w-full">
      <caption class="text-xs text-gray-500">Why Structure? & Key Files</caption>
      <thead>
        <tr>
          <th class="text-left w-1/2">Why Structure?</th>
          <th class="text-left w-1/2">Key Files</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>
            <ul class="list-disc ml-4">
              <li>Reliable parsing for LLMs and tools</li>
              <li>Machine-actionable, not just readable</li>
              <li>Reduces ambiguity and creative detours</li>
              <li>Balances clarity for both people and machines</li>
            </ul>
          </td>
          <td>
            <ul class="list-disc ml-4">
              <li><code>@rulestyle-rule.md</code>: How to write rules</li>
              <li><code>@rule-interpreter-rule.md</code>: What the schema means</li>
              <li><code>@rulestore-rule.md</code>: Where rules live for a tool</li>
              <li><code>@rule-registry.json</code>: Index of all rules</li>
            </ul>
          </td>
        </tr>
        <tr>
          <td colspan="2">
            <span class="font-bold">Context is everything:</span> Structured rules go into the LLM's context window. The clearer, the better the results. Experiment to find what works for your workflow.
          </td>
        </tr>
      </tbody>
    </table>
  </div>

</div>