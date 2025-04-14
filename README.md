# 🗒️ AI Sticky Notes – MCP Server in Python

This project is a minimal **MCP (Message Control Protocol)** server built in Python using the [`mcp` SDK](https://github.com/mcp-ai/mcp). It lets you create and manage sticky notes that can be read, updated, and summarized by an AI agent like Claude, via Claude Desktop.

## 🚀 Features

- ✅ Add and save notes
- 📖 Read all saved notes
- 📌 Fetch the latest note
- 🧠 Prompt Claude to summarize all notes

## 📦 Requirements

- Python 3.8+
- [Claude Desktop](https://www.anthropic.com/index/claude-desktop) installed
- [uv](https://github.com/astral-sh/uv) (recommended over pip for dependency management)
- MCP Python SDK

## 🛠 Setup

1. **Install `uv` (recommended)**

   ```bash
   # Windows
   irm https://astral.sh/uv/install.ps1 | iex

   # macOS/Linux
   curl -LsSf https://astral.sh/uv/install.sh | sh
Initialize a new project

bash
Copy
Edit
uv init .
Install dependencies

bash
Copy
Edit
uv add mcp-cli
Run the MCP server

bash
Copy
Edit
uv run mcp install main.py
Integrate with Claude Desktop

Open Claude Desktop

Go to Settings > Developer > Edit Config

Add your MCP server using the generated uv command

Restart Claude

✨ Usage
Ask Claude things like:

"Add a note saying 'Meeting at 3 PM'"

"Read all my notes"

"What’s the latest note?"

"Summarize my notes"

🧾 File Structure
bash
Copy
Edit
main.py          # MCP server implementation
notes.txt        # Auto-generated file storing notes
📚 Tools and Concepts Used
FastMCP

@mcp.tool – For executable functions

@mcp.resource – For context data (like latest notes)

@mcp.prompt – Reusable prompts for AI agents

Claude Desktop integration

🧠 Ideas for Future Enhancements
