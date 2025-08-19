# RAG Slide Notes

(2 mins)
RAG, or Retrieval Augmented Generation, is a game-changer for making LLMs more useful and factual.
It's a fancy way of saying: "Let the LLM search a specific knowledge base before answering."
The process is simple: user asks, system finds relevant info from a source (like your company's wiki, or your codebase via a vector DB), adds that info to the prompt, and then the LLM answers.
This helps with several problems: LLMs don't know very recent events, they don't know your private data, and they can hallucinate. RAG grounds them.
Now, specific to us developers: your codebase itself is a massive source of context! You can RAG codebases easily 