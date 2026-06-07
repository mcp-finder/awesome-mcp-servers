# Awesome MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of the best **Model Context Protocol (MCP) servers** — production-ready, verified, and organized by category. Connect Claude, Cursor, Cline, Zed, and other AI clients to real tools and data.

**Last updated:** 2026-05-11 · **Maintained by** the community · **Verified reliability data:** [MCPfinder.org](https://mcpfinder.org)

The Model Context Protocol (MCP) lets large language models talk to external tools, APIs, files, and databases through a single open standard. This list tracks the MCP server ecosystem so you can find a server that does what you need without sifting through abandoned repos.

> **Need a trust signal before installing?** Every server in this list also has a public reliability score and last-checked timestamp on the [MCPfinder registry](https://mcpfinder.org) — so you can see at a glance whether a server is actively maintained before adding it to your stack.

---

## Contents

- [What is MCP?](#what-is-mcp)
- [Official servers](#official-servers)
- [Databases](#databases)
- [Developer tools](#developer-tools)
- [Files, storage, and search](#files-storage-and-search)
- [Web, scraping, and browsing](#web-scraping-and-browsing)
- [Productivity and notes](#productivity-and-notes)
- [Communication](#communication)
- [Cloud and DevOps](#cloud-and-devops)
- [AI, LLM, and embeddings](#ai-llm-and-embeddings)
- [Finance and crypto](#finance-and-crypto)
- [Design and media](#design-and-media)
- [Security](#security)
- [E-commerce](#e-commerce)
- [Health and fitness](#health-and-fitness)
- [Frameworks and SDKs](#frameworks-and-sdks)
- [Clients that consume MCP](#clients-that-consume-mcp)
- [Learning resources](#learning-resources)
- [Contributing](#contributing)

---

## What is MCP?

The [Model Context Protocol](https://modelcontextprotocol.io) is an open standard, introduced by Anthropic in late 2024, that defines how AI assistants connect to external systems. Instead of every AI client building bespoke integrations for every tool, MCP servers expose tools, resources, and prompts through one protocol that any compatible client (Claude Desktop, Cursor, Cline, Continue, Zed, and many more) can consume.

An MCP server can:

- **Expose tools** — functions the model can call (e.g. `query_database`, `send_email`).
- **Expose resources** — data the model can read (files, API responses, query results).
- **Expose prompts** — reusable prompt templates parameterized by the client.

To pick a server worth installing, look for: an active GitHub repo, a documented tool surface, an explicit transport (stdio or SSE), and ideally a third-party reliability signal — which is the gap [MCPfinder](https://mcpfinder.org) was built to fill.

---

## Official servers

Maintained by Anthropic or the MCP organization.

- [filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) — Secure local file operations with configurable allowed paths.
- [git](https://github.com/modelcontextprotocol/servers/tree/main/src/git) — Read, search, and manipulate Git repositories.
- [github](https://github.com/modelcontextprotocol/servers/tree/main/src/github) — Repository management, issues, PRs, file contents.
- [postgres](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres) — Read-only Postgres access with schema introspection.
- [sqlite](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) — Local SQLite database access with query and schema tools.
- [google-drive](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive) — Search and read Google Drive files.
- [google-maps](https://github.com/modelcontextprotocol/servers/tree/main/src/google-maps) — Directions, places, geocoding.
- [slack](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) — Channels, messages, users, history.
- [memory](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) — Knowledge-graph-based persistent memory.
- [puppeteer](https://github.com/modelcontextprotocol/servers/tree/main/src/puppeteer) — Browser automation and web scraping.
- [fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) — Web content fetching and conversion.
- [brave-search](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) — Web search via Brave's API.
- [sentry](https://github.com/modelcontextprotocol/servers/tree/main/src/sentry) — Issue retrieval and analysis.
- [time](https://github.com/modelcontextprotocol/servers/tree/main/src/time) — Time and timezone conversion.

---

## Databases

- [postgres-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres) — Postgres read access.
- [mysql-mcp-server](https://github.com/benborla/mcp-server-mysql) — MySQL with schema discovery.
- [mongodb-mcp](https://github.com/QuantGeekDev/mongo-mcp) — Collection queries, aggregations.
- [redis-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/redis) — Key-value operations.
- [neo4j-mcp](https://github.com/da-okazaki/mcp-neo4j-server) — Cypher queries against Neo4j.
- [bigquery-mcp](https://github.com/LucasHild/mcp-server-bigquery) — Google BigQuery SQL.
- [snowflake-mcp](https://github.com/datawiza/mcp-snowflake-server) — Snowflake warehouse queries.
- [clickhouse-mcp](https://github.com/ClickHouse/mcp-clickhouse) — ClickHouse OLAP queries.
- [supabase-mcp](https://github.com/supabase-community/supabase-mcp) — Supabase tables, RPC, auth.
- [pinecone-mcp](https://github.com/sirmews/mcp-pinecone) — Vector search.
- [qdrant-mcp](https://github.com/qdrant/mcp-server-qdrant) — Qdrant vector DB.
- [chroma-mcp](https://github.com/privetin/chroma) — Chroma embeddings.

> Picking between vector DBs? The [MCP database comparison on MCPfinder](https://mcpfinder.org) tracks last-release date and open-issue count for each server.

---

## Developer tools

- [gadgethumans-api-hub-mcp](https://github.com/scotia1973-bot/gadgethumans-api-hub-mcp) - 334 free developer tools: QR codes, passwords, UUIDs, hashes, Base64, JSON, color converter, email verification, IP geolocation, timestamps, plus 300+ calculators, text analysis, color tools, readability, domain, code and financial tools. MCP server at `uvx gadgethumans-api-hub-mcp`. Free, no API key required.
- [github-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/github) — Full GitHub API access.
- [gitlab-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/gitlab) — GitLab projects, MRs, issues.
- [linear-mcp](https://github.com/jerhadf/linear-mcp-server) — Linear issues and projects.
- [jira-mcp](https://github.com/sooperset/mcp-atlassian) — Atlassian Jira + Confluence.
- [sentry-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/sentry) — Error monitoring.
- [docker-mcp](https://github.com/QuantGeekDev/docker-mcp) — Container lifecycle.
- [kubernetes-mcp](https://github.com/Flux159/mcp-server-kubernetes) — Cluster inspection and apply.
- [terraform-mcp](https://github.com/severity1/terraform-cloud-mcp) — Terraform Cloud workspaces.
- [npm-mcp](https://github.com/erithwik/mcp-npm) — Package metadata, downloads.
- [code-runner-mcp](https://github.com/formulahendry/mcp-server-code-runner) — Multi-language code execution.
- [vscode-mcp-server](https://github.com/block/vscode-mcp) — VS Code editor integration.

---

## Files, storage, and search

- [filesystem-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) — Local filesystem.
- [s3-mcp](https://github.com/aws-samples/sample-mcp-server-s3) — S3 buckets.
- [gcs-mcp](https://github.com/glandfried/mcp-gcs) — Google Cloud Storage.
- [dropbox-mcp](https://github.com/akoskovacs/mcp-dropbox) — Dropbox file access.
- [box-mcp](https://github.com/box-community/mcp-server-box) — Box enterprise storage.
- [onedrive-mcp](https://github.com/yourusername/onedrive-mcp) — Microsoft OneDrive.

---

## Web, scraping, and browsing

- [puppeteer-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/puppeteer) — Headless Chromium.
- [playwright-mcp](https://github.com/microsoft/playwright-mcp) — Microsoft Playwright automation.
- [browserbase-mcp](https://github.com/browserbase/mcp-server-browserbase) — Hosted browser cloud.
- [firecrawl-mcp](https://github.com/mendableai/firecrawl-mcp-server) — Web crawling and scraping.
- [brave-search-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) — Brave Search API.
- [exa-mcp](https://github.com/exa-labs/exa-mcp-server) — Exa neural search.
- [tavily-mcp](https://github.com/tavily-ai/tavily-mcp) — Tavily search API.
- [perplexity-mcp](https://github.com/jsonallen/perplexity-mcp) — Perplexity-style web answers.
- [fetch-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) — HTTP fetch + HTML→markdown.

---

## Productivity and notes

- [notion-mcp](https://github.com/makenotion/notion-mcp-server) — Notion pages, databases.
- [obsidian-mcp](https://github.com/MarkusPfundstein/mcp-obsidian) — Obsidian vaults.
- [todoist-mcp](https://github.com/abhiz123/todoist-mcp-server) — Tasks and projects.
- [calendar-mcp](https://github.com/Zawad99/Google-Calendar-MCP-Server) — Google Calendar.
- [apple-notes-mcp](https://github.com/sirmews/apple-notes-mcp) — Apple Notes (macOS).
- [readwise-mcp](https://github.com/IAmStoxe/readwise-mcp) — Highlights and reading list.

---

## Communication

- [slack-mcp](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) — Slack workspaces.
- [discord-mcp](https://github.com/v-3/discordmcp) — Discord channels and DMs.
- [telegram-mcp](https://github.com/chigwell/telegram-mcp) — Telegram bots.
- [gmail-mcp](https://github.com/GongRzhe/Gmail-MCP-Server) — Gmail read/send.
- [whatsapp-mcp](https://github.com/lharries/whatsapp-mcp) — WhatsApp via local bridge.

---

## Cloud and DevOps

- [aws-mcp](https://github.com/RafalWilinski/aws-mcp) — AWS CLI passthrough.
- [cloudflare-mcp](https://github.com/cloudflare/mcp-server-cloudflare) — Workers, KV, DNS.
- [vercel-mcp](https://github.com/Quegenx/vercel-mcp-server) — Deployments, env vars.
- [netlify-mcp](https://github.com/MCERQUA/netlify-mcp) — Netlify sites and builds.
- [stripe-mcp](https://github.com/stripe/agent-toolkit) — Payments, customers, subscriptions.

---

## AI, LLM, and embeddings

- [openai-mcp](https://github.com/pierrebrunelle/mcp-server-openai) — OpenAI API passthrough.
- [replicate-mcp](https://github.com/deepfates/mcp-replicate) — Replicate model runs.
- [hugging-face-mcp](https://github.com/shreyaskarnik/huggingface-mcp-server) — Models, datasets, inference.
- [elevenlabs-mcp](https://github.com/elevenlabs/elevenlabs-mcp) — Text-to-speech.
- [openrouter-mcp](https://github.com/heltonteixeira/openrouter-mcp) — Multi-model gateway.

---

## Finance and crypto

- [stripe-mcp](https://github.com/stripe/agent-toolkit) — Stripe operations.
- [quickbooks-mcp](https://github.com/abel9851/mcp-server-quickbooks) — Bookkeeping.
- [plaid-mcp](https://github.com/yourusername/plaid-mcp) — Bank account aggregation.
- [coingecko-mcp](https://github.com/coingecko/mcp-server-coingecko) — Crypto market data.
- [chainstack-mcp](https://github.com/chainstacklabs/mcp-evm-server) — EVM chain RPC.
- [alphavantage-mcp](https://github.com/calvernaz/alphavantage) — Stock market data.

---

## Design and media

- [figma-mcp](https://github.com/GLips/Figma-Context-MCP) — Figma file context.
- [blender-mcp](https://github.com/ahujasid/blender-mcp) — Blender 3D scenes.
- [unity-mcp](https://github.com/justinpbarnett/unity-mcp) — Unity editor automation.
- [spotify-mcp](https://github.com/varunneal/spotify-mcp) — Playback and playlists.

---

## Security

- [shodan-mcp](https://github.com/BurtTheCoder/mcp-shodan) — Shodan host scans.
- [virustotal-mcp](https://github.com/BurtTheCoder/mcp-virustotal) — File/URL reputation.
- [1password-mcp](https://github.com/dkmaker/mcp-1password) — Secret retrieval.

---

## E-commerce

- [shopify-mcp](https://github.com/rezapex/shopify-mcp-server) — Products, orders, inventory.
- [woocommerce-mcp](https://github.com/techspawn/woocommerce-mcp-server) — WordPress shop ops.

---

## Health and fitness

- [strava-mcp](https://github.com/r-huijts/strava-mcp) — Activity history.
- [oura-mcp](https://github.com/tomekkorbak/oura-mcp-server) — Sleep and readiness.

---

## Frameworks and SDKs

Build your own MCP server in your preferred language:

- [@modelcontextprotocol/sdk (TypeScript)](https://github.com/modelcontextprotocol/typescript-sdk) — Official TypeScript SDK.
- [mcp Python SDK](https://github.com/modelcontextprotocol/python-sdk) — Official Python SDK.
- [mcp-go](https://github.com/mark3labs/mcp-go) — Idiomatic Go SDK.
- [mcp-rust-sdk](https://github.com/jeanlucthumm/mcp-rust-sdk) — Rust SDK.
- [mcp-kotlin](https://github.com/modelcontextprotocol/kotlin-sdk) — Kotlin/JVM SDK.
- [mcp-csharp](https://github.com/modelcontextprotocol/csharp-sdk) — .NET SDK.

> Just shipped a server? **List it on [MCPfinder.org](https://mcpfinder.org)** for a verified profile, install snippet, and reliability tracking.

---

## Clients that consume MCP

Apps that can connect to MCP servers:

- **Claude Desktop** — Anthropic's reference client (macOS, Windows).
- **Cursor** — AI code editor with native MCP support.
- **Cline** — VS Code agent (formerly Claude Dev).
- **Continue** — Open-source VS Code / JetBrains assistant.
- **Zed** — Collaborative editor with MCP support.
- **Sourcegraph Cody** — Code intelligence assistant.
- **Windsurf** — Codeium's AI IDE.
- **5ire** — Cross-platform MCP desktop client.

---

## Learning resources

- [Official MCP documentation](https://modelcontextprotocol.io)
- [MCP specification](https://spec.modelcontextprotocol.io)
- [Anthropic's MCP launch announcement](https://www.anthropic.com/news/model-context-protocol)
- [MCPfinder server directory](https://mcpfinder.org) — searchable registry with reliability scores

---

## Contributing

Pull requests welcome. Each entry should:

1. Be a working MCP server (not a placeholder or stub).
2. Have a public source repository or clear installation path.
3. Include a one-sentence description that explains what it does (not what it is).
4. Be placed in the most specific applicable category.

See `CONTRIBUTING.md` for the full checklist.

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, contributors have waived all copyright and related rights to this work.

---

*Maintained alongside [MCPfinder.org](https://mcpfinder.org) — the trust layer for the MCP ecosystem.*
