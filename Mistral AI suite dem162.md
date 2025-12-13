Mistral AI suite demo frontend

A multi‑page frontend that showcases how users can explore, integrate, and
interact with specialized AI models across realistic product flows. It
includes a landing page, code assistant, API documentation, social login
demo, geolocation/venue explorers, and a lightweight dataset labeling +
training sandbox. Designed as a teaching/demo app for ethical AI
integrations.
Highlights

   -

   *Landing:* Product overview, model gallery, and quickstarts.
   -

   *Code assistant:* In‑browser coding chat with snippets, autocomplete,
   and explain/fix flows.
   -

   *API docs:* Live, copy‑pastable examples and an interactive console with
   API keys from env.
   -

   *Auth demo:* Email/password and OAuth (Google, GitHub, etc.) with secure
   session handling.
   -

   *Places & routes:* “Boulevard” (urban) and “Milieu naturel”
   (nature/gems) explorers using GPS and addresses.
   -

   *Publication/login modes:* Public browse mode and creator mode for
   posting content with location metadata.
   -

   *Label & train:* Minimal labeling UI and a background job to fine‑tune
   or prompt‑adapt a model on curated data.
   -

   *Safety by design:* No impersonation, spoofing, or deceptive content.
   Clear consent, audit trails, and rate limits.

This project is for education/demo. It intentionally excludes features that
enable impersonation, fake accounts, or disinformation. See “Safety and
ethics.”

Pages

   -

   *Landing:* Model cards, use cases, pricing placeholders, and CTAs.
   -

   *Code assistant:*
   -

      *Prompts:* Explain code, refactor, add tests, fix bugs.
      -

      *Context:* File upload or snippet paste with token budgeting.
      -

      *Outputs:* Diff view and copy actions.
      -

   *API docs:*
   -

      *Guides:* Auth, text, chat, embeddings, image, tools.
      -

      *Reference:* Endpoints, parameters, error codes.
      -

      *Playground:* Interactive requests with masked keys.
      -

   *Auth & profile:*
   -

      *Login/registration:* Password + OAuth via standard providers.
      -

      *Profile:* API key management, session history, data export/delete.
      -

   *Explore places (“Boulevard” and “Milieu naturel”):*
   -

      *Search:* GPS, address (apt, floor, street), and transport hints.
      -

      *Views:* Cards + map preview, sunrise/sunset theming (dawn/dusk).
      -

      *Routes:* Walking/transit driving time estimates (mock or
      provider‑backed).
      -

   *Publication vs login mode:*
   -

      *Publication mode:* Read‑only browsing, shareable links.
      -

      *Login mode:* Create posts with optional location metadata and
      visibility controls.
      -

   *Dataset labeling & training:*
   -

      *Labeler:* Tag text, image captions, or conversation turns.
      -

      *Exporter:* JSONL/Parquet exports with schema validation.
      -

      *Trainer:* Background job to fine‑tune or create prompt‑adapters;
      reports metrics.

Architecture

   -

   *Frontend:* Next.js/React, TypeScript, Tailwind, Zustand/Redux for state.
   -

   *API layer:* Next.js  Route Handlers or Node/Express with zod validation.
   -

   *Auth:* OAuth 2.0/OpenID Connect (e.g., NextAuth), session cookies with
   rotating keys.
   -

   *AI client:* Server‑side SDK wrapper with retry, tracing, and usage
   metering.
   -

   *Storage:* Postgres (Prisma), S3‑compatible object storage for uploads.
   -

   *Jobs:* Queue (BullMQ/Redis) for training and long‑running tasks.
   -

   *Maps:* Provider SDK (Mapbox/Leaflet/Google Maps) with geocoding and
   reverse geocoding.
   -

   *Telemetry:* OpenTelemetry traces; audit logs for sensitive actions.

Getting startedPrerequisites

   -

   *Node:* 18+
   -

   *Package manager:* pnpm or npm
   -

   *Database:* Postgres 14+
   -

   *Redis:* For queues (optional but recommended)
   -

   *Maps provider key:* Mapbox or Google Maps
   -

   *OAuth providers:* Google/GitHub app credentials (optional)
