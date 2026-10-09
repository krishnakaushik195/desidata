# Publishing DesiData

The MCP endpoint is deployed and the portable plugin package is prepared. A deployed endpoint does not automatically appear in client directories; each marketplace requires a separate submission and review.

## Before public submission

1. The owner selected the MIT license. The package includes the license text and declares `"license": "MIT"` in `plugin.json`.
2. The package is being added under `plugins/desidata-mcp/` in the existing public `krishnakaushik195/desidata` repository. The private website repository is not part of this release.
3. The listing points to DesiData's public community page for support and the existing privacy policy. DesiData does not currently expose a Terms of Service page; the Codex directory requires one for a public MCP app, so add/approve that URL before submitting there.
4. Confirm the publisher identity and listing text in each marketplace dashboard.

## OpenAI plugin directory (Codex)

1. Upload a ZIP containing `plugin.json`, `mcp.json`, and this package's documentation in the OpenAI Plugins dashboard.
2. Select the verified developer identity that should own the listing.
3. Connect the HTTPS MCP endpoint and complete the domain verification shown in the dashboard.
4. Review the discovered tools and automated findings, fix any issues, and submit for review.

The endpoint is currently public and does not use OAuth. Do not add a client secret or Supabase key to this package.

## Cursor Marketplace

1. Keep the plugin package under `plugins/desidata-mcp/` and its marketplace entry in `.cursor-plugin/marketplace.json` at the public repository root.
2. Confirm the plugin locally in Cursor.
3. Submit `https://github.com/krishnakaushik195/desidata` through [Cursor Marketplace Publish](https://cursor.com/marketplace/publish) and complete Cursor's review process.

Users can install it manually from the MCP URL while the marketplace review is pending.

## Gemini

Gemini CLI can connect directly to the same remote MCP URL; the command is in `README.md`. Gemini Apps custom apps are connected per Google account and are subject to Google's availability and account-linking requirements. They do not become a public marketplace listing just because this package is published.
