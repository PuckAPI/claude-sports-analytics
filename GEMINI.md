# PuckAPI for Gemini CLI

This extension connects Gemini CLI to the PuckAPI MCP server at https://mcp.puckapi.com/mcp.
PuckAPI is a sports data API for NHL hockey. The server exposes tools for
schedules, results, team and player stats, and betting odds.

## Setup

1. Get a free key at https://puckapi.com/signup. The free tier includes 500 credits per month.
2. Set the key as an environment variable before you start Gemini CLI:

   export PUCKAPI_API_KEY=your_key

3. Restart Gemini CLI. The extension sends the key in the x-api-key header.

Connecting and listing tools works without a key. Calling a tool needs one.

## How to use it

- Ask for NHL hockey data in plain language. Gemini picks the matching MCP tool.
- Each tool call uses credits from your monthly allowance.
- If a call fails with an auth error, check that PUCKAPI_API_KEY is set in the shell that launched Gemini CLI.
- Docs: https://puckapi.com/docs
