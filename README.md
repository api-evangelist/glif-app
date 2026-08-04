# Glif (glif-app)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
