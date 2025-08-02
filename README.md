# AI Assistant with MCP Servers, LangChain & Groq

A multi-tool, agentic AI assistant powered by [Model Context Protocol (MCP)](https://github.com/anthropics/model-context-protocol), [LangChain](https://www.langchain.com/), and [Groq](https://groq.com/). This assistant dynamically connects to external tools and services like web search (DuckDuckGo), browser automation (Playwright), and travel APIs (Airbnb) — all without writing separate integration code for each tool.

> Built from scratch using `mcp-use`, LangChain, and Cursor IDE. Ideal for AI agents, autonomous task execution, and context-aware assistants.

---

##  Features

- **Connect to Multiple MCP Servers** (e.g., DuckDuckGo, Airbnb, Playwright)
- **LLM Agent Powered by Groq (or OpenAI/Anthropic)**
- **LangChain Integration** for memory, tool routing, and async flows
- **Tool-based Configuration using JSON**
- **Command-Line Interface (CLI)** for real-time interaction
-  Built with **Cursor IDE** and `uv` (Rust-based Python environment manager)
-  Lets you interact with the assistant via terminal, asking questions like:
  - _"Show me hotels in Goa"_
  - _"What are the top AI news today?"_
  - _"Open MakeMyTrip website"_

---

## Prerequisites

Make sure you have the following installed:
- [Node.js](https://nodejs.org/)
- [Python 3.9+](https://www.python.org/)
- [Cursor IDE](https://www.cursor.so/)
- [uv](https://github.com/astral-sh/uv) (Rust-powered Python package manager)
- Groq / OpenAI API Key

---

## 🛠️ Installation

```bash
# Step 1: Clone this repo
git clone https://github.com/manasiadhav/AI-Assistant-With-MCP-Servers-using-LangChain-And-Groq.git
cd AI-Assistant-With-MCP-Servers-using-LangChain-And-Groq

# Step 2: Initialize a Python project using uv
uv init mcp-demo
cd mcp-demo

# Step 3: Install required packages
uv pip install langchain langchain-groq openai mcp-use python-dotenv

# Step 4: Create your environment file
touch .env
# Add your keys
GROQ_API_KEY=your-groq-api-key

# Step 5:
uv run app.py
