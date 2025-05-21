# DevTalk Presentation Deck

This project contains a modern, visually engaging slide deck focused on LLM tools, the Model Context Protocol (MCP), and agent workflows.

## Overview
- **Topics Covered:**
  - How LLMs use tools and function calling
  - The need for standards like MCP
  - Components of MCP (tools, resources, prompts, connections, OAuth, etc.)
  - Real-world use cases: from code to design, docs, automation, and more
  - Forward-looking questions about AI-friendly documentation and agent ecosystems

## How to Run the Deck

This deck uses [Slidev](https://sli.dev/) for interactive, web-based presentations.

1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the local dev server:
   ```bash
   npm run dev
   ```
3. Open the local URL (usually http://localhost:3000) in your browser to view and present the slides.

## Viewing & Editing Slides
- Slides are written in Markdown (`.md`) files in the `pages/` directory.
- Each slide uses HTML/CSS for custom styling and layout (two-column, color, etc.).
- To view or present:
  - Use a Markdown previewer that supports HTML (e.g., VS Code with Markdown Preview Enhanced, or Obsidian).
  - For web-based slides, consider tools like [Marp](https://marp.app/) or [Deckset](https://www.deckset.com/).

## Tech Stack
- Markdown with embedded HTML/CSS for layout and style
- No build step required; just open in a compatible Markdown viewer

## Contributing & Extending
- Add new slides by creating new `.md` files in `pages/`.
- Follow the existing style: colored titles, two-column layouts, concise and visual content.
- To extend for your own topics, duplicate a slide and update the content.

## License
MIT 