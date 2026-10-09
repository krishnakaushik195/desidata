# DesiData MCP Plugin

DesiData helps AI coding assistants find published India-focused datasets and inspect their provenance before using them.

## What users can do

- Search the published DesiData catalogue.
- Read dataset metadata, source, licence, size, and row count.
- Preview a small sample of a CSV dataset.
- Get a notebook link or Python loader example.

Search and previews are available without signing in. The MCP service is hosted and managed by DesiData.

The MCP does not return whole CSV files. Full downloads use the user's own DesiData `DD_TOKEN` through the regular DesiData download flow. Never paste a token into an AI chat or commit it to a project.

## Add to a client

### Cursor

Add this server to Cursor's global `mcp.json` (or install the reviewed marketplace plugin when it is published):

```json
{
  "mcpServers": {
    "desidata": {
      "url": "https://www.desidata.in/api/mcp"
    }
  }
}
```

Reload Cursor, then find DesiData under **Customize → MCP**.

### Codex

```sh
codex mcp add desidata --url https://www.desidata.in/api/mcp
codex mcp list
```

### Gemini CLI

```sh
gemini extensions install https://github.com/krishnakaushik195/desidata
```

Restart Gemini CLI and run `/mcp list` to confirm the connection. You can also connect directly with `gemini mcp add --transport http --scope user desidata https://www.desidata.in/api/mcp`.

Gemini Apps custom-app availability and account-linking requirements are controlled by Google and may differ from Gemini CLI.

## Example prompts

- “Find published datasets about rainfall in Maharashtra.”
- “Show the source, licence, and row count for this dataset.”
- “Preview this dataset and explain the columns.”
- “Give me a Python example to load this dataset.”

## Current limits

- Search matches query text in published dataset titles and descriptions; it is not semantic search and does not search through every CSV row.
- A preview returns at most 10 rows, 12 columns, and 64 KiB of source CSV data.
- Notebook and Python tools return links or example code, not a full dataset download.
- Calls are subject to the DesiData MCP rate limits.

## Privacy

Review the [DesiData Privacy Policy](https://www.desidata.in/privacy). The client sends the MCP server the tool arguments needed for a request, such as a search query or dataset slug.
