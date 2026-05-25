# Glif (glif-app)
Glif is a creative AI platform from Spellcasters, Inc. — originally launched in 2023 as a no-code visual workflow builder for chaining text, image, audio, and video models into shareable "glifs", and re-launched in March 2026 as Glif 2.0, a single chat-based AI agent with access to 100+ native tools (Claude Sonnet 4.5, Claude Opus 4.1, GPT-4o, Nano Banana Pro, Flux 2 Turbo, Seedream V4, Kling 2.5 Turbo Pro, VEO 3.1, Hailuo 2.3, ElevenLabs, MiniMax v2, FFmpeg, web search and more). Glif raised a $17.5M seed round led by a16z and USV in April 2026. The platform is used by creators, e-commerce sellers, performance marketers, and agencies to produce short-form video, product shoots, ad campaigns, character/comic art, memes, logos, and SVG vector graphics. Glif's public REST and Simple APIs were deprecated on 2026-05-20 in favor of the chat agent surface; the open Glif MCP server, ComfyUI custom nodes, Chrome extension, and Python client remain the canonical programmatic entry points to the platform. Profiled in the API Evangelist network as a reference case for the "no-code AI workflow builder → AI agent" platform pivot, alongside peers such as Anthropic, OpenAI, and other foundation-model orchestration providers.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/glif-app/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Artificial Intelligence, No-Code, Workflows, Creative AI, Generative AI, Video Generation, Image Generation, ComfyUI, MCP, LLM Apps

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Glif Simple API
HTTP endpoint for invoking a single published glif (AI workflow) by ID and passing a list of named or positional string inputs. POST a JSON body with `id` and `inputs` to `https://simple-api.glif.app` using a Bearer token; the response includes the run's final `output` (often an image URL or text) plus an `outputFull` block describing the output type. Legacy responses always return HTTP 200 even on error, with the error surfaced in an `error` field. Per Glif's FAQ the API was deprecated on 2026-05-20 as part of the Glif 2.0 chat-agent rebuild; the documentation repository remains public for reference and existing integrations.

**Human URL:** [https://docs.glif.app](https://docs.glif.app)

**Base URL:** `https://simple-api.glif.app`

- [Documentation](https://github.com/glifxyz/api-docs/blob/main/getting-started.md)
- [Authentication](https://glif.app/settings/api-tokens)

### Glif REST API
Read-and-write REST API for the Glif platform — list and fetch glifs (`/glifs`), look up runs (`/runs`), fetch the authenticated user (`/me`), look up users (`/user`), and browse curated collections (`/spheres`). Supports filtering by `id`, `username`, `userId`, `glifId`, `featured`, pagination with `page` and `limit` (default 20, max 100), and inclusion of full glif-graph JSON via `?includes=spells.data`. A private POST `/glifs` endpoint creates draft glifs by supplying a graph of node blocks (TextInputBlock, GPTBlock, ComfyUI blocks, etc.). Deprecated 2026-05-20 alongside the Simple API as Glif retired the workflow-builder surface in favor of the chat-based agent.

**Human URL:** [https://docs.glif.app](https://docs.glif.app)

**Base URL:** `https://glif.app/api`

- [Documentation](https://github.com/glifxyz/api-docs/blob/main/reading-and-writing-data-via-the-api.md)
- [Authentication](https://glif.app/settings/api-tokens)

## Common Properties

- [Glif Homepage (Portal)](https://glif.app)
- [Glif Docs / Guide (Documentation)](https://docs.glif.app)
- [Intro to Glif (Documentation)](https://docs.glif.app/getting-started/intro-to-glif)
- [Glif FAQs (Documentation)](https://docs.glif.app/getting-started/faqs)
- [Glif Changelog (ChangeLog)](https://glif.app/changelog)
- [Glif Pricing (Pricing)](https://glif.app/pricing)
- [Glif Terms of Service (TermsOfService)](https://glif.app/legal)
- [Glif Privacy Policy (PrivacyPolicy)](https://glif.app/privacy)
- [Glif Contact (Support)](https://glif.app/contact)
- [Glif Discord (Forum)](https://discord.gg/nuR9zZ2nsh)
- [Glif on GitHub (GitHub)](https://github.com/glifxyz)
- [Glif on X (Twitter)](https://twitter.com/heyglif)
- [Glif on LinkedIn (LinkedIn)](https://www.linkedin.com/company/heyglif)
- [Glif on YouTube (YouTube)](https://www.youtube.com/@heyglif)
- [Glif MCP Server (Tools)](https://github.com/glifxyz/glif-mcp-server)
- [ComfyUI Glif Nodes (Tools)](https://github.com/glifxyz/ComfyUI-GlifNodes)
- [ComfyUI Glif Vision Nodes (Tools)](https://github.com/glifxyz/ComfyUI-GlifVision)
- [Glif Python Client (SDK)](https://github.com/glifxyz/glif-client-python)
- [Glif API NextJS Demo (SampleApps)](https://github.com/glifxyz/glif-api-demo)
- [Glif API Docs Source (Documentation)](https://github.com/glifxyz/api-docs)
- [Glif Chrome Extension (Application)](https://chromewebstore.google.com/detail/glif-remix-the-web-with-a/abfbooehhdjcgmbmcpkcebcmpfnlingo)
- [Glif on PitchBook (CompanyProfile)](https://pitchbook.com/profiles/company/535615-03)
