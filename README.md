# Chatbot using MCP

A simple command-line chatbot that connects a Groq LLM to MCP (Model Context Protocol) tools, with conversation memory.

## Setup

```bash
git clone https://github.com/soumita20/chatbot-using-mcp.git
cd chatbot-using-mcp
pip install mcp-use langchain-groq python-dotenv
```

Create a `.env` file with your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Define your MCP servers in `browser_mcp.json`, for example:

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    }
  }
}
```

## Run

```bash
python app.py
```

## Commands

- `exit` or `quit`: end the chat
- `clear`: clear conversation history

## Notes

- Uses the `openai/gpt-oss-120b` model via Groq
- Requires Python 3.11+ and Node.js (for `npx`-based MCP servers)