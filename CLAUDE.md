# TryPost Connect Docs

Docs for [TryPost Connect](https://connect.trypost.it). Mintlify site. Work on `main`.

## Product (do not mix with the old app)

| | Connect |
|---|---|
| What | Infra so customers build their own scheduler |
| App | `https://connect.trypost.it` |
| REST | `https://connect.trypost.it/api` |
| MCP | `https://connect.trypost.it/mcp` (OAuth `mcp:use`, not API keys) |
| Tenant | One account |
| Media | Presign → PUT → `public_url` on the post. No library. No public-URL ingest. |
| Connect | `GET /social-accounts/connect/{platform}?redirect_url=` → `{url,state}`. Browser comes back to the client. |

Do **not** document: asset library, attach-from-url, `/content-types` REST, `/workspace`, signatures, labels, repurposes, self-hosting, `app.trypost.it`.

## Contract to follow

Read `~/Herd/trypost-connect/routes/api.php` and `app/Mcp/Servers/TryPostServer.php` before changing API or MCP pages.

- Path params are `{id}` (nested child `{log_id}`).
- `JsonResource::withoutWrapping()` — single objects and non-paginated lists are bare; only posts, logs, and webhook logs paginate.
- Social account JSON: `id`, `set_id`, `platform`, `display_name`, `username`, `avatar_url`, `status`.
- Webhook events include `account.connected` / `account.disconnected`.
- MCP `request-media-upload-tool` = REST presign. Then `media[].url` on create/update.

## Writing

- Cloud only. No self-host accordions.
- Link to official platform docs when changing OAuth or publish limits.
- `mint broken-links` after large IA changes.
