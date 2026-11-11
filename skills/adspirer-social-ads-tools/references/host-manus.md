# Running on Manus

Checked against Manus's custom MCP and Skills documentation on 2026-11-11. Menu labels change;
re-check before relying on them.

## Connection

- The user adds the server under Settings → Integrations → Custom MCP Servers → Add Server (some
  builds show Connectors → Add custom MCP), with the name `Adspirer Social Ads` and the URL
  `https://mcp.adspirer.com/social-ads`. Manus only takes remote HTTPS servers.
- Sign-in is browser OAuth with the user's Adspirer account. Never ask for a token in chat.
- Manus tests the connection and lists the tools. If the tools are missing, tell the user to
  reconnect there; do not invent data.
- Manus times out slow requests. Prefer narrower date ranges and one account per call over one
  very large report; say so when you split a request.

## Autonomy

Manus plans and acts on its own, often with a browser and a sandbox, and can keep working after
the user leaves. This connector can change ad accounts, so stop and ask before every write: show the exact change, the account and the cost, and wait for a yes.
Follow the approvals and purchases rules in the main skill: never use the browser to buy or
upgrade a plan, and never treat a broad goal as permission to spend.

## Scheduled tasks

Manus scheduled tasks run unattended. Schedule read-only reporting only, and state that each run
uses Adspirer tool calls.
