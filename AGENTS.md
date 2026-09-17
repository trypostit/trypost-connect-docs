# TryPost Connect Docs

Mintlify documentation for **TryPost Connect** — B2B publishing infrastructure at [connect.trypost.it](https://connect.trypost.it).

## Product

Connect is not the TryPost scheduler. There is no calendar, no asset library, no self-host, no workspaces. Media is pass-through: `POST /medias/presign` → `PUT` → `media[].url` = `public_url`. Connect accounts via `GET /social-accounts/connect/{platform}?redirect_url=` (`{url,state}`; browser redirect to the client). MCP is `https://connect.trypost.it/mcp` (OAuth, no API keys, no connect tool).

Source of truth for the contract is `~/Herd/trypost-connect` (`routes/api.php`, `app/Mcp/Servers/TryPostServer.php`).

## Style

- Active voice, second person
- Sentence case headings
- Do not document the old scheduler (signatures, labels, repurposes, assets, self-hosting)
