# TryPost Connect Docs

Documentation for [TryPost Connect](https://connect.trypost.it) — social publishing infrastructure (REST + MCP). Built with [Mintlify](https://mintlify.com).

This is **not** the old TryPost scheduler docs.

## Development

```bash
npm i -g mint
mint dev
```

Preview at `http://localhost:3000`.

## Publishing

Pushes to `main` deploy via the [Mintlify GitHub app](https://dashboard.mintlify.com/settings/organization/github-app).

## Structure

```
├── getting-started/   # Auth, first publish
├── guides/            # Connect, media, posts, sets, webhooks, MCP, billing
├── platforms/         # Per-network content types and limits
├── api-reference/     # REST endpoints
└── docs.json
```
