# Awesome Laravel [Awesome](https://awesome.re/badge.svg)

> A curated list of Laravel 13.x features, official packages, community packages, observability tooling, self-hosted infra patterns, YouTube channels, and websites. Inspired by awesome-php and other awesome lists.

**Maintained under sudo-su-coffee.** Contributions welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

[![Laravel 13](https://img.shields.io/badge/Laravel-13.x-red?style=for-the-badge&logo=laravel)](https://laravel.com)
[![PHP 8.3+](https://img.shields.io/badge/PHP-8.3%2B-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net)
[![Packages](https://img.shields.io/badge/Packages-320%2B-blue?style=for-the-badge)](#-table-of-contents)
[![Last Updated](https://img.shields.io/badge/Updated-2026--10--04-orange?style=for-the-badge)](#)

---

## Table of Contents

1. [Laravel Version History (8 → 13)](#1-laravel-version-history-8--13)
2. [Laravel 13 Highlights](#2-laravel-13-highlights)
3. [YouTube Channels](#3-youtube-channels)
4. [Websites](#4-websites)
5. [First-Party Packages](#5-first-party-packages)
6. [Package Reference — By Domain](#6-package-reference--by-domain)
   - [Core & Skeleton](#61-core--skeleton)
   - [Admin Panels & CRUD](#62-admin-panels--crud)
   - [Auth, Permissions, Multi-Tenancy](#63-auth-permissions-multi-tenancy)
   - [Data, DTOs, State](#64-data-dtos-state)
   - [Query Building & API Resources](#65-query-building--api-resources)
   - [Media, Files, Uploads](#66-media-files-uploads)
   - [Excel, PDF, Documents](#67-excel-pdf-documents)
   - [API Development & Docs](#68-api-development--docs)
   - [Search](#69-search)
   - [Testing](#610-testing)
   - [Settings & Feature Flags](#611-settings--feature-flags)
   - [Auditing & Activity](#612-auditing--activity)
   - [Backups, Health, Monitoring](#613-backups-health-monitoring)
   - [Localization](#614-localization)
   - [Queues, Jobs, Scheduling](#615-queues-jobs-scheduling)
   - [Payments & Billing](#616-payments--billing)
   - [E-Commerce](#617-e-commerce)
   - [Kafka & Event Streaming](#618-kafka--event-streaming)
   - [Code Quality & Static Analysis](#619-code-quality--static-analysis)
   - [Dev Environment & Tooling](#620-dev-environment--tooling)
   - [Debugging](#621-debugging)
   - [Performance & Octane](#622-performance--octane)
   - [HTTP, Utilities, Misc](#623-http-utilities-misc)
   - [Livewire / Frontend](#624-livewire--frontend)
   - [AI, Vector, Embeddings](#625-ai-vector-embeddings)
   - [Observability](#626-observability)
   - [Database & Infra](#627-database--infra)
   - [Log Aggregation](#628-log-aggregation)
7. [Observability — Deep Dive](#7-observability--deep-dive)
8. [Queue Monitoring — Horizon vs Telescope vs Pulse](#8-queue-monitoring--horizon-vs-telescope-vs-pulse)
9. [University Multi-Module Platform Stack](#9-university-multi-module-platform-stack)
10. [Docker at Scale](#10-docker-at-scale)
11. [License](#-license)

---

## 1. Laravel Version History (8 → 13)

| Version | Released | PHP Req. | Key New Features |
|---|---|---|---|
| **8** | Sep 8, 2020 | 7.3+ | Laravel Jetstream, app/Models directory, class-based model factories, migration squashing (`schema:dump`), improved rate limiting, time testing helpers, dynamic Blade components, job batching (`Bus::batch()`), maintenance mode with pre-rendered view |
| **9** | Feb 8, 2022 | 8.0+ | Symfony 6.0 components, Symfony Mailer (replaced SwiftMailer), Flysystem 3.0, Scout database driver, new accessor/mutator syntax (`Attribute::make()`), implicit route bindings via Enums, controller route grouping, forced scoped bindings, annual release cycle starts |
| **10** | Feb 14, 2023 | 8.1+ | Process facade (`Process::run()`, concurrent pools, faking), invokable validation rules by default, native PHP type declarations across skeleton code, Laravel Pennant (feature flags), `Str::password()`, test profiling (`--profile`), Horizon/Telescope UI refresh |
| **11** | Mar 12, 2024 | 8.2+ | Slimmed-down default app skeleton, per-second rate limiting, health check routing (`/up`), Laravel Reverb (WebSocket server), Prompts for CLI, graceful encryption key rotation, `once()` helper, Dumpable trait, resendable email verification |
| **12** | Feb 24, 2025 | 8.2–8.5 | New official starter kits (React/Svelte/Vue/Livewire on Inertia 2 + TypeScript + shadcn/ui / Flux+Volt), WorkOS AuthKit variant per kit, Breeze/Jetstream deprecated, Carbon 3-only, JSON cast Unicode preservation, minimal-breaking "maintenance release" |
| **13** | Mar 17, 2026 | 8.3–8.5 | **Laravel AI SDK** (text/tools/embeddings/audio/images), native **JSON:API resources**, **PreventRequestForgery** CSRF middleware, queue routing by class (`Queue::route()`), expanded **PHP attributes** (`#[Middleware]`, `#[Authorize]`, `#[Tries]`, `#[Backoff]`, `#[Timeout]`, `#[FailOnTimeout]`), **`Cache::touch()`**, native **vector/semantic search** (`whereVectorSimilarTo()` + pgvector) |

**Official release notes:** [8.x](https://laravel.com/docs/8.x/releases) · [9.x](https://laravel.com/docs/9.x/releases) · [10.x](https://laravel.com/docs/10.x/releases) · [11.x](https://laravel.com/docs/11.x/releases) · [12.x](https://laravel.com/docs/12.x/releases) · [13.x](https://laravel.com/docs/13.x/releases)

---

## 2. Laravel 13 Highlights

**Laravel 13.0 — March 17, 2026.** Requires PHP 8.3+. [Official release notes](https://laravel.com/docs/13.x/releases).

- ⭐ **Laravel AI SDK** — First-party, unified API for text generation, tool-calling agents, embeddings, audio, images, vector-store integration. One SDK for OpenAI, Anthropic, Gemini, Groq, xAI, and more. Includes classification (Jev), Vercel Chat protocol support, AG-UI protocol, conversation storage, streaming chat, tool approvals. [reference:0][reference:1]
- **JSON:API Resources** — Native JSON:API-compliant resource serialization. No external packages needed.
- **PreventRequestForgery** — Formalized, origin-aware CSRF middleware.
- **Queue routing by class** — `Queue::route(Job::class, connection: 'redis', queue: 'name')`.
- **Expanded PHP attributes** — `#[Middleware]`, `#[Authorize]`, `#[Tries]`, `#[Backoff]`, `#[Timeout]`, `#[FailOnTimeout]` across ~15 locations.
- **`Cache::touch()`** — Extend TTL without re-storing the value.
- **Native semantic/vector search** — `whereVectorSimilarTo()` against PostgreSQL + pgvector.
- **Tagged Memoized Cache** — v13.33.0 adds tag support for the memoized cache and a `Refreshes` model attribute for reloading generated columns after a write. [reference:2]
- **Typed Translation Accessors** — v13.15.0 adds typed translation accessors, JSON Schema deserialization, a dedicated Cloud queue driver. [reference:3]
- **Laravel Cloud Facade for Managed Queues** — August 2026 changelog. Read-through filesystems, AI tool-call recovery. [reference:4]

**Carried over from Laravel 12:** React/Svelte/Vue/Livewire starter kits (Inertia 2, TypeScript, shadcn/ui / Flux UI + Volt), WorkOS AuthKit variant per kit, Carbon 3-only.

---

## 3. YouTube Channels

| Channel | Focus |
|---|---|
| [Laravel](https://www.youtube.com/@Laravel) | Official channel — conference talks, feature announcements |
| [Laravel Daily](https://www.youtube.com/@LaravelDaily) | Tutorials, package roundups, real-world patterns |
| [Grant Harting](https://www.youtube.com/@grantharting) | In-depth Laravel/PHP tutorials |
| [CodeHead](https://www.youtube.com/@CodeHead) | Laravel tutorials and project walkthroughs |
| [Laracasts](https://laracasts.com) | Video courses (Jeffrey Way) — official-adjacent |
| [PHP Architect](https://www.phparch.com) | Deep-dive PHP/Laravel performance and architecture |

---

## 4. Websites

| Site | What It Is |
|---|---|
| [Laravel News](https://laravel-news.com) | News, package releases, tutorials |
| [Laravel Daily (site)](https://laraveldaily.com) | Tutorials + [packages directory](https://laraveldaily.com/packages) [reference:5] |
| [Laracasts](https://laracasts.com) | Official-adjacent video courses |
| [Spatie Open Source](https://spatie.be/open-source) | Full catalog from Laravel's most prolific package maintainer |
| [Packagist](https://packagist.org) | Official PHP package registry |
| [Packalyst](https://packalyst.com) | Laravel-specific package directory |
| [LaraPlugins](https://laraplugins.io) | Plugin discovery with compatibility filters |
| [Laravel.com](https://laravel.com) | Official site & docs |
| [awesome-laravel (chiraggude)](https://github.com/chiraggude/awesome-laravel) | Curated list: essentials, hosting, deployment, learning resources |
| [Best-Laravel-Packages (LaravelDaily)](https://github.com/LaravelDaily/Best-Laravel-Packages) | Curated package list on GitHub |

---

## 5. First-Party Packages

| Package | Purpose |
|---|---|
| **laravel/framework** | Core framework — service container, routing, middleware, events, queues |
| **laravel/laravel** | Application skeleton / starter template |
| **laravel/octane** | High-performance app server (FrankenPHP / Swoole / RoadRunner) |
| **laravel/horizon** | Redis queue dashboard + monitoring |
| **laravel/sanctum** | Lightweight SPA/mobile token auth |
| **laravel/passport** | Full OAuth2 server |
| **laravel/socialite** | OAuth login (Google, GitHub, etc.) |
| **laravel/fortify** | Headless auth backend — 2FA, email verify, lockout |
| **laravel/reverb** | First-party WebSocket server |
| **laravel/echo** | JS client for broadcasting / WebSockets |
| **laravel/scout** | Full-text search driver abstraction |
| **laravel/pennant** | Feature flags |
| **laravel/pulse** | Real-time app performance monitoring dashboard |
| **laravel/nightwatch** | APM/observability product (paid) |
| **laravel/telescope** | Local debugging / request inspector |
| **laravel/dusk** | Browser testing (Selenium-based) |
| **laravel/cashier** | Stripe billing / subscriptions |
| **laravel/cashier-paddle** | Paddle billing variant |
| **laravel/pint** | Opinionated PHP code style fixer |
| **laravel/sail** | Docker dev environment |
| **laravel/valet** | macOS local dev environment |
| **laravel/envoy** | SSH task runner — deploy scripts in Blade syntax |
| **laravel/prompts** | Beautiful CLI prompts |
| **laravel/passkeys** | WebAuthn / FIDO2 passkey client (TS) |
| **laravel/stream** | SSE streaming hooks for React/Vue — LLM response streaming |
| **laravel/wayfinder** | Type-safe route / action references for TS frontends |
| **laravel/folio** | File-system page routing (Next.js style) for Blade |
| **laravel/ai** | First-party AI SDK (13.x) — text, tools, embeddings, images, audio [reference:6] |
| **laravel/surveyor** | Static analysis — extracts PHP/Laravel meta from codebase |
| **laravel/ranger** | Runtime introspection — query, model, service container inspection |
| **Forge / Vapor / Cloud** | Hosting / deployment (paid) |
| **Nova** | Admin panel (paid) |

---

## 6. Package Reference — By Domain

### Legend

| Symbol | Meaning |
|---|---|
| 🟢 | **Active** — recent commits, healthy issue response |
| 🟡 | **Maintained** — works, slower cadence |
| 🟠 | **Stale** — no commits in 12+ months, still functional |
| 🔴 | **Deprecated / Archived** — do not start new projects here |
| ⭐ | **First-party** — maintained by the Laravel team |
| 🧩 | **Framework-agnostic** — usable outside Laravel |

**Compatibility:** `13` = Laravel 13, `12` = Laravel 12, `11` = Laravel 11.

---

### 6.1 Core & Skeleton

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/framework** | Core framework | 🟢 | 13/12/11 | ~34.7k ★ |
| ⭐ **laravel/laravel** | App skeleton | 🟢 | 13/12/11 | ~84.3k ★ |
| ⭐ **laravel/installer** | CLI installer | 🟢 | 13/12/11 | `composer global require laravel/installer` |
| ⭐ **laravel/prompts** | Beautiful CLI prompts | 🟢 | 13/12/11 | Used by Artisan generators |

---

### 6.2 Admin Panels & CRUD

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **filament/filament** | TALL-stack admin builder | 🟢 | 13/12/11 | Dominant choice. ~19k ★. v4 adds refreshed design, improved performance [reference:7] |
| **laravel/nova** | Official paid admin panel | 🟢 | 13/12/11 | Paid license |
| **orchid/platform** | Admin panel framework | 🟢 | 13/12 | Alternative to Nova |
| **backpack/crud** | CRUD generator + admin | 🟢 | 13/12/11 | Long-standing |
| **voyager/voyager** | BREAD-based admin | 🟡 | 11 | Lightly maintained |
| **craftable** (brackets) | CRUD generator | 🟡 | 12 | Backpack-based |
| **bezhansalleh/filament-shield** | Filament permissions | 🟢 | 13/12 | Pairs with spatie/laravel-permission |
| **muazzam/filament-pro-starter** | Filament starter kit | 🟢 | 13 | Shield, 2FA, Passkeys pre-configured [reference:8] |

---

### 6.3 Auth, Permissions, Multi-Tenancy

#### Authentication

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/sanctum** | SPA/mobile token auth | 🟢 | 13/12/11 | First-party default for APIs |
| ⭐ **laravel/passport** | Full OAuth2 server | 🟢 | 13/12/11 | Use when you need a full OAuth server |
| ⭐ **laravel/socialite** | OAuth login abstraction | 🟢 | 13/12/11 | ~5.7k ★ |
| ⭐ **laravel/fortify** | Headless auth backend | 🟢 | 13/12/11 | 2FA, email verify, lockout |
| ⭐ **laravel/jetstream** | Full-stack auth starter | 🔴 | 11/12 | Deprecated in favor of starter kits |
| ⭐ **laravel/ui** | Legacy UI presets | 🔴 | 11 | Deprecated |
| **tymon/jwt-auth** | JWT authentication | 🟢 | 13/12/11 | Still widely used despite Sanctum |
| ⭐ **laravel/passkeys** | WebAuthn / FIDO2 (TS client) | 🟢 | 13/12 | First-party |
| **workos/workos-php** | WorkOS AuthKit (SSO, passkeys) | 🟢 | 13/12/11 | Bundled in starter kits |
| **laragear/two-factor** | 2FA (TOTP, SMS, email) | 🟢 | 13/12/11 | Cleaner than Fortify's built-in |
| **pragmarx/google2fa-laravel** | Google 2FA | 🟢 | 13/12/11 | Older but stable |
| **spatie/laravel-one-time-passwords** | OTP for passwordless | 🟢 | 13/12/11 | Magic-link + OTP |
| **spatie/laravel-login-link** | Passwordless login links | 🟢 | 13/12/11 | Dev-friendly |

#### Permissions

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-permission** | RBAC — roles & permissions | 🟢 | 13/12/11 | ~12k ★. Near-universal |
| **spatie/laravel-permission-teams** | Team-scoped permissions | 🟢 | 13/12/11 | Extension for multi-tenant RBAC |
| **santigarcor/laratrust** | RBAC + teams | 🟡 | 12/11 | Multi-guard roles |
| **jeremykenedy/laravel-roles** | Role management | 🟡 | 12/11 | Includes UI |

#### Multi-Tenancy

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **stancl/tenancy** | Multi-tenancy (DB-per-tenant) | 🟢 | 13/12/11 | Most mature. No code changes needed [reference:9] |
| **spatie/laravel-multitenancy** | Alternative multi-tenancy | 🟢 | 13/12/11 | Simpler, less feature-rich |
| **tenancy/tenancy** | Base library (Stancl uses it) | 🟢 | 13/12/11 | Framework-agnostic core |
| **mahdisphp/laravel-realm** | Multi-tenancy with single trait | 🟢 | 13/12 | Safety-first approach [reference:10] |
| **kicklabel/tenancy** | Automatic multi-tenancy | 🟢 | 13/12 | v1.0.0 released [reference:11] |
| **nunomazer/laravel-samehouse** | Single-database multi-tenancy | 🟢 | 13/12/11 | Simple, easy to use [reference:12] |
| **mohamedhekal/tenantforge** | Shared-database multi-tenancy | 🟢 | 13/12 | SaaS foundation: tenants, domains, API keys [reference:13] |

#### Impersonation

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **lab404/laravel-impersonate** | User impersonation | 🟢 | 13/12/11 | Standard |

---

### 6.4 Data, DTOs, State

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-data** | Typed DTOs with validation + TS gen | 🟢 | 13/12/11 | ~3.9k ★. Standard |
| **spatie/laravel-model-states** | State machine on models | 🟢 | 13/12/11 | Order/trip states |
| **spatie/laravel-model-status** | Status history on models | 🟢 | 13/12/11 | Audit of state changes |
| **spatie/enum** | Enum helper | 🟢 | 13/12/11 | Framework-agnostic |
| **bensampo/laravel-enum** | Enum implementation | 🟡 | 11/12 | Less popular now with native enums |
| **spatie/laravel-typescript-transformer** | PHP → TypeScript types | 🟢 | 13/12/11 | Shares types with frontend |
| **wendelladriel/laravel-validated-dto** | DTO with validation | 🟢 | 13/12/11 | Lighter than spatie/laravel-data |
| **spatie/laravel-schemaless-attributes** | JSON column attributes | 🟢 | 13/12/11 | — |
| **spatie/laravel-options** | Option objects | 🟢 | 13/12/11 | — |

---

### 6.5 Query Building & API Resources

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-query-builder** | Filter/sort/include from query string | 🟢 | 13/12/11 | ~4k ★ |
| **spatie/laravel-fractal** | API transformation via Fractal | 🟢 | 13/12/11 | Legacy-style transformers |
| 🧩 **league/fractal** | Underlying transformer library | 🟢 | 13/12/11 | Framework-agnostic |
| **spatie/laravel-json-api-paginate** | JSON:API pagination | 🟢 | 13/12/11 | Compatible with JSON:API spec |
| **timacdonald/json-api** | Full JSON:API resources | 🟢 | 13/12 | Modern JSON:API implementation |
| **spatie/laravel-eloquent-query-cache** | Query result caching | 🟢 | 13/12/11 | Automatic invalidation |
| **protonemedia/laravel-eloquent-scope-as-select** | Subquery scopes | 🟢 | 13/12/11 | N+1 optimization |
| **protonemedia/laravel-cross-eloquent-search** | Cross-model search | 🟢 | 13/12/11 | Search across multiple models [reference:14] |
| **spatie/laravel-query-builder** | Filter/sort/include | 🟢 | 13/12/11 | — |

---

### 6.6 Media, Files, Uploads

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-medialibrary** | Media/file attachment | 🟢 | 13/12/11 | ~5.8k ★. Standard |
| **spatie/laravel-image-optimizer** | Auto-optimize images | 🟢 | 13/12/11 | JPEG/PNG/WebP |
| 🧩 **intervention/image** | Image manipulation | 🟢 | 13/12/11 | Framework-agnostic |
| 🧩 **intervention/image-laravel** | Laravel integration | 🟢 | 13/12/11 | Official wrapper |
| **spatie/laravel-glide** | On-the-fly image manipulation | 🟢 | 13/12/11 | URL-based transforms |
| 🧩 **league/flysystem-aws-s3-v3** | S3 filesystem driver | 🟢 | 13/12/11 | Works with MinIO, R2, B2 |
| **spatie/laravel-responsive-images** | Responsive image variants | 🟡 | 12/11 | For medialibrary |

---

### 6.7 Excel, PDF, Documents

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **maatwebsite/excel** | Excel/CSV import/export | 🟢 | 13/12/11 | ~12k ★. Standard |
| 🧩 **phpoffice/phpspreadsheet** | Underlying spreadsheet library | 🟢 | 13/12/11 | Framework-agnostic |
| **barryvdh/laravel-dompdf** | HTML → PDF | 🟢 | 13/12/11 | Simple, widely used |
| **barryvdh/laravel-snappy** | HTML → PDF via wkhtmltopdf | 🟡 | 12/11 | Requires wkhtmltopdf binary |
| **spatie/laravel-pdf** | PDF via headless Chrome | 🟢 | 13/12/11 | Modern. Pairs with Browsershot |
| **spatie/browsershot** | Screenshot/PDF via Puppeteer | 🟢 | 13/12/11 | Requires Node + Chromium |
| **spatie/laravel-browsershot** | Laravel wrapper for Browsershot | 🟢 | 13/12/11 | Simplifies config |

---

### 6.8 API Development & Docs

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **dedoc/scramble** | Auto-generate OpenAPI from code | 🟢 | 13/12/11 | No annotations. Modern |
| **darkaonline/l5-swagger** | Swagger/OpenAPI via annotations | 🟢 | 13/12/11 | Annotation-driven |
| **knuckleswtf/scribe** | API documentation from code | 🟢 | 13/12/11 | Postman export |
| **nuwave/lighthouse** | GraphQL server | 🟢 | 13/12/11 | Standard GraphQL |
| **rebing/graphql-laravel** | Alternative GraphQL | 🟢 | 13/12/11 | Query-based |
| **spatie/laravel-route-attributes** | Routes from attributes | 🟢 | 13/12/11 | Controller-based routing |

---

### 6.9 Search

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/scout** | Search driver abstraction | 🟢 | 13/12/11 | First-party |
| **meilisearch/meilisearch-php** | Meilisearch driver | 🟢 | 13/12/11 | Self-hostable, <1ms |
| **typesense/typesense-php** | Typesense driver | 🟢 | 13/12/11 | Typo-tolerant |
| **algolia/scout-extended** | Algolia Scout extensions | 🟢 | 13/12/11 | SaaS |
| **teamtnt/tntsearch** | Pure-PHP full-text search | 🟢 | 13/12/11 | No external service needed |
| **spatie/laravel-searchable** | Simple trait-based search | 🟢 | 13/12/11 | For small datasets |
| **lorisleiva/laravel-search-string** | Query-string search DSL | 🟢 | 13/12/11 | Human-friendly syntax |

---

### 6.10 Testing

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **pestphp/pest** | Testing framework | 🟢 | 13/12/11 | ~9.3k ★. Preferred over PHPUnit |
| **pestphp/pest-plugin-laravel** | Pest Laravel helpers | 🟢 | 13/12/11 | `actingAs`, `get`, `post` |
| **pestphp/pest-plugin-livewire** | Pest Livewire helpers | 🟢 | 13/12/11 | — |
| **pestphp/pest-plugin-arch** | Architectural testing | 🟢 | 13/12/11 | Enforce boundaries |
| **pestphp/pest-plugin-type-coverage** | Type coverage testing | 🟢 | 13/12/11 | — |
| ⭐ **laravel/dusk** | Browser E2E testing | 🟢 | 13/12/11 | Selenium-based |
| 🧩 **mockery/mockery** | Mocking library | 🟢 | 13/12/11 | Framework-agnostic |
| 🧩 **fakerphp/faker** | Fake data generation | 🟢 | 13/12/11 | — |
| **spatie/pest-plugin-snapshots** | Snapshot testing for Pest | 🟢 | 13/12/11 | — |
| **spatie/phpunit-snapshot-assertions** | Snapshot testing for PHPUnit | 🟢 | 13/12/11 | — |
| **nunomaduro/collision** | Better CLI error output | 🟢 | 13/12/11 | Ships with Laravel |
| **nunomaduro/phpinsights** | Code quality scoring | 🟢 | 13/12/11 | — |

---

### 6.11 Settings & Feature Flags

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-settings** | Typed DB-backed settings | 🟢 | 13/12/11 | — |
| ⭐ **laravel/pennant** | Feature flags | 🟢 | 13/12/11 | First-party. Per-user/per-tenant toggling [reference:15] |
| **spatie/laravel-feature-flags** | Alternative feature flags | 🟠 | 11 | — |
| **henzeb/laravel-pennant-cache** | Cache driver for Pennant | 🟢 | 13/12 | Redis, Memcached, DynamoDB [reference:16] |
| **creativitykills/filament-pennant** | Filament UI for Pennant | 🟢 | 13/12 | Manage flags from admin panel [reference:17] |

---

### 6.12 Auditing & Activity

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-activitylog** | Model change tracking | 🟢 | 13/12/11 | ~5.6k ★. Standard |
| **owen-it/laravel-auditing** | Alternative audit trail | 🟢 | 13/12/11 | More detailed |
| **spatie/laravel-model-status** | Status history | 🟢 | 13/12/11 | — |
| **laravel-auditing/laravel-auditing** | Current maintained version | 🟢 | 13/12/11 | Fork of owen-it |
| **Chronicle** (verifiable audit logging) | Hash-chained append-only ledger | 🟢 | 13 | Tamper-verifiable audit history [reference:18] |

---

### 6.13 Backups, Health, Monitoring

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-backup** | DB + file backups | 🟢 | 13/12/11 | ~5.7k ★ |
| **spatie/laravel-health** | Health check dashboard | 🟢 | 13/12/11 | ~2.7k ★ |
| ⭐ **laravel/pulse** | Real-time APM | 🟢 | 13/12/11 | First-party. See [Observability Deep Dive](#7-observability--deep-dive) |
| ⭐ **laravel/telescope** | Dev debugging | 🟢 | 13/12/11 | Dev only — never in prod at scale |
| ⭐ **laravel/nightwatch** | Production APM (paid) | 🟢 | 13/12 | Replaces Datadog for Laravel |
| **sentry/sentry-laravel** | Error tracking | 🟢 | 13/12/11 | Official first-party SDK |
| **bugsnag/bugsnag-laravel** | Error tracking | 🟢 | 13/12/11 | Alternative to Sentry |
| **spatie/laravel-schedule-monitor** | Cron task monitoring | 🟢 | 13/12/11 | Alert if scheduled task fails |

---

### 6.14 Localization

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-translatable** | Translatable model attributes | 🟢 | 13/12/11 | ~2.5k ★ [reference:19] |
| **mcamara/laravel-localization** | URL/route localization | 🟢 | 13/12/11 | ~3.5k ★. Language selection in URL and from headers [reference:20] |
| **spatie/laravel-translation-loader** | DB-backed translations | 🟢 | 13/12/11 | — |
| **astrotomic/laravel-translatable** | Alternative translatable | 🟢 | 13/12/11 | Different storage model. ~1.4k ★ [reference:21] |
| **dimsav/laravel-translatable** | Historical predecessor | 🔴 | 8 | Superseded by astrotomic |
| **laravel-lang/lang** | Language files for all locales | 🟢 | 13/12/11 | 126 languages. ~7.8k ★ [reference:22] |
| **MohmmedAshraf/laravel-translations** | Translation management UI | 🟢 | 13/12/11 | ~819 ★ [reference:23] |
| **niels-numbers/laravel-localizer** | Locale-aware routing | 🟢 | 13/12 | Modern alternative [reference:24] |

---

### 6.15 Queues, Jobs, Scheduling

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/horizon** | Redis queue dashboard | 🟢 | 13/12/11 | ~4.1k ★. Standard for Redis. See [Queue Monitoring](#8-queue-monitoring--horizon-vs-telescope-vs-pulse) |
| ⭐ **laravel/reverb** | WebSocket server | 🟢 | 13/12/11 | Replaces Pusher. Managed clusters on Laravel Cloud [reference:25] |
| **spatie/laravel-queueable-action** | Action classes as jobs | 🟢 | 13/12/11 | — |
| **spatie/laravel-schedule-monitor** | Scheduled task monitoring | 🟢 | 13/12/11 | — |
| **vyuldashev/laravel-queue-rabbitmq** | RabbitMQ queue driver | 🟢 | 13/12/11 | — |
| **php-amqplib/php-amqplib** | RabbitMQ AMQP library | 🟢 | 13/12/11 | Underlying |
| **dusterio/laravel-aws-worker** | SQS worker for AWS | 🟡 | 12/11 | — |
| **hardimpactdev/horizon-new-dawn** | React 19 + Inertia 3 Horizon UI | 🟢 | 13 | Replaces Horizon's bundled interface [reference:26] |
| **pocketarc/horizon-database** | Run Horizon on a database | 🟢 | 13 | Instead of Redis [reference:27] |

---

### 6.16 Payments & Billing

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/cashier** | Stripe billing | 🟢 | 13/12/11 | ~5.9k ★ |
| ⭐ **laravel/cashier-paddle** | Paddle billing | 🟢 | 13/12/11 | Tax-inclusive |
| **srmklive/paypal** | PayPal integration | 🟢 | 13/12/11 | — |
| **anandsiddharth/laravel-razorpay** | Razorpay | 🟡 | 12/11 | Thin wrapper |
| 🧩 **razorpay/razorpay** | Official Razorpay SDK | 🟢 | 13/12/11 | Framework-agnostic |
| **rushabhmishrarmz/indipay** | Indian gateway aggregator | 🟠 | 10/11 | Multi-gateway (CCAvenue, PayU, etc.) |
| **laravel/paddle** | First-party Paddle SDK | 🟢 | 13/12 | — |

---

### 6.17 E-Commerce

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **aimeos/aimeos-laravel** | Full e-commerce package | 🟢 | 13/12/11 | API-first, cloud-native |
| **bagisto/bagisto** | Standalone e-commerce app | 🟢 | 12/11 | Full store out of the box |
| **lunarphp/lunar** | Headless e-commerce | 🟢 | 13/12/11 | API-first |
| **vanilophp/framework** | Modular e-commerce | 🟢 | 13/12/11 | Compose your own |
| **getcandy/getcandy** | Headless e-commerce (pre-Lunar) | 🔴 | 10/11 | Renamed to Lunar |

---

### 6.18 Kafka & Event Streaming

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **mateusjunges/laravel-kafka** | Kafka producer/consumer | 🟢 | 13/12/11 | ~728 ★. Standard |
| **chocofamilyme/laravel-kafka** | Batch produce/consume fork | 🟢 | 12/11 | High-throughput |
| 🧩 **ext-rdkafka** (PECL) | Required PHP extension | 🟢 | — | `pecl install rdkafka` |
| 🧩 **librdkafka** (system) | Required system library | 🟢 | — | Install before PECL |
| **spatie/laravel-event-sourcing** | Event sourcing | 🟢 | 13/12/11 | Different paradigm |
| **spatie/laravel-event-sourcing-projections** | Event projections | 🟢 | 13/12/11 | Companion |

**Install order (order matters):**
```
librdkafka (system) → pecl install rdkafka → composer require mateusjunges/laravel-kafka
```

---

### 6.19 Code Quality & Static Analysis

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/pint** | Code style fixer | 🟢 | 13/12/11 | ~3.1k ★. First-party |
| 🧩 **friendsofphp/php-cs-fixer** | Underlying CS fixer | 🟢 | 13/12/11 | Pint uses this |
| 🧩 **phpstan/phpstan** | Static analysis | 🟢 | 13/12/11 | Framework-agnostic |
| **larastan/larastan** | PHPStan rules for Laravel | 🟢 | 13/12/11 | ~3.3k ★. Renamed from nunomaduro/larastan |
| **rector/rector** | Automated refactoring | 🟢 | 13/12/11 | Upgrade automation |
| **driftingly/rector-laravel** | Laravel Rector rules | 🟢 | 13/12/11 | Framework-specific refactors |
| **nunomaduro/phpinsights** | Code quality scoring | 🟢 | 13/12/11 | — |
| **symplify/easy-coding-standard** | Alternative CS tool | 🟢 | 13/12/11 | Simpler than php-cs-fixer |

---

### 6.20 Dev Environment & Tooling

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/sail** | Docker dev environment | 🟢 | 13/12/11 | Local dev only |
| ⭐ **laravel/valet** | macOS local dev | 🟢 | 13/12/11 | Nginx + dnsmasq |
| ⭐ **laravel/tinker** | REPL | 🟢 | 13/12/11 | ~7.4k ★ |
| ⭐ **laravel/envoy** | SSH task runner | 🟢 | 13/12/11 | Deploy scripts |
| **beyondcode/laravel-dump-server** | Standalone dump server | 🟢 | 13/12/11 | — |
| **spatie/laravel-ignition** | Enhanced error page | 🟢 | 13/12/11 | Ships with Laravel |
| **spatie/laravel-tail** | `artisan tail` command | 🟢 | 13/12/11 | — |
| **spatie/laravel-db-snapshots** | DB snapshot/load | 🟢 | 13/12/11 | Fast test DB reset |
| **spatie/laravel-artisan-dispatchable** | Dispatch artisan from code | 🟢 | 13/12/11 | — |
| **laravel/homestead** | Vagrant dev box | 🟠 | 10/11 | Legacy, replaced by Sail |

---

### 6.21 Debugging

| Package | Approach | Status | Compat | Notes |
|---|---|---|---|---|
| **barryvdh/laravel-debugbar** | In-page toolbar | 🟢 | 13/12/11 | ~16k ★. Dev only. v4 released Jan 2026 |
| **itsgoingd/clockwork** | Browser extension panel | 🟢 | 13/12/11 | Lighter than Debugbar |
| **spatie/ray** | Desktop app debugging | 🟢 | 13/12/11 | Paid desktop app |
| ⭐ **laravel/telescope** | Full dashboard | 🟢 | 13/12/11 | Dev only |
| **spatie/laravel-ray** | Laravel integration for Ray | 🟢 | 13/12/11 | — |

---

### 6.22 Performance & Octane

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/octane** | Persistent worker via Swoole/RoadRunner/FrankenPHP | 🟢 | 13/12/11 | ~4k ★. 2.5–3.1x throughput gains [reference:28] |
| 🧩 **spiral/roadrunner-http** | RoadRunner HTTP worker | 🟢 | 13/12/11 | Required for RR |
| 🧩 **spiral/roadrunner-cli** | RoadRunner CLI | 🟢 | 13/12/11 | Required for RR |
| **protonemedia/laravel-pipeline-benchmark** | Middleware bottleneck detection | 🟡 | 12/11 | Dev tool |
| **spatie/laravel-responsecache** | Full response caching | 🟢 | 13/12/11 | — |
| **watson/rememberable** | Query result caching | 🟢 | 13/12/11 | — |
| **rennokki/laravel-eloquent-query-cache** | Query cache | 🟢 | 13/12/11 | — |

**Octane server comparison (2026):**

| Server | When to Use | Notes |
|---|---|---|
| **FrankenPHP** | Default recommendation. Easiest path into Octane. HTTP/3 native, single binary, bundles Caddy + TLS. [reference:29] | FrankenPHP significantly outperformed PHP-FPM + Nginx [reference:30] |
| **RoadRunner** | Mature, process-isolated monolith deployments. No PHP extensions required. [reference:31] | Battle-tested Go binary |
| **Swoole / Open Swoole** | Only if you need coroutines, concurrent tasks, ticks, or Octane's in-memory cache/tables. [reference:32] | Maximum throughput, low latency |

---

### 6.23 HTTP, Utilities, Misc

#### Spatie utility packages

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **spatie/laravel-sluggable** | Auto-generate slugs | 🟢 | 13/12/11 | — |
| **spatie/laravel-sitemap** | XML sitemap generation | 🟢 | 13/12/11 | — |
| **spatie/laravel-tags** | Taggable models | 🟢 | 13/12/11 | — |
| **spatie/laravel-comments** | Commenting system | 🟢 | 13/12/11 | — |
| **spatie/laravel-webhook-client** | Receive/verify webhooks | 🟢 | 13/12/11 | — |
| **spatie/laravel-webhook-server** | Send webhooks with retries | 🟢 | 13/12/11 | — |
| **spatie/laravel-csp** | Content Security Policy | 🟢 | 13/12/11 | — |
| **spatie/laravel-cookie-consent** | GDPR cookie banner | 🟢 | 13/12/11 | — |
| **spatie/laravel-honeypot** | Spam form protection | 🟢 | 13/12/11 | — |
| **spatie/laravel-url-signer** | Signed URLs | 🟢 | 13/12/11 | — |
| **spatie/laravel-collection-macros** | Extra Collection methods | 🟢 | 13/12/11 | 100+ macros |
| **spatie/laravel-html** | HTML builder | 🟢 | 13/12/11 | — |
| **spatie/laravel-menu** | Menu builder | 🟢 | 13/12/11 | — |
| **spatie/laravel-navigation** | Navigation builder | 🟢 | 13/12/11 | — |
| **spatie/laravel-blade-comments** | Blade comments | 🟢 | 13/12/11 | — |
| **spatie/laravel-package-tools** | Package development helpers | 🟢 | 13/12/11 | — |
| **spatie/laravel-personal-data-export** | GDPR data export | 🟢 | 13/12/11 | — |
| **spatie/laravel-referer** | Referer tracking | 🟢 | 13/12/11 | — |
| **spatie/laravel-discord-alerts** | Discord notifications | 🟢 | 13/12/11 | — |
| **spatie/laravel-slack-alerts** | Slack notifications | 🟢 | 13/12/11 | — |
| **spatie/laravel-google-calendar** | Google Calendar sync | 🟢 | 13/12/11 | — |
| **spatie/laravel-google-fonts** | Self-hosted Google Fonts | 🟢 | 13/12/11 | GDPR-friendly |
| **spatie/laravel-feed** | RSS/Atom feed generation | 🟢 | 13/12/11 | — |
| **spatie/laravel-view-models** | View models for Blade | 🟢 | 13/12/11 | — |
| **spatie/laravel-ciphersweet** | Searchable encryption | 🟢 | 13/12/11 | — |
| **spatie/laravel-crypto** | Cryptography helpers | 🟢 | 13/12/11 | — |
| **spatie/laravel-rate-limited-job-middleware** | Rate-limited jobs | 🟢 | 13/12/11 | — |
| **spatie/laravel-route-discovery** | Route discovery | 🟢 | 13/12/11 | — |
| **spatie/laravel-directory-cleanup** | Clean temp directories | 🟢 | 13/12/11 | — |
| **spatie/laravel-missing-page-redirector** | Redirect missing pages | 🟢 | 13/12/11 | — |
| **spatie/laravel-failed-job-monitor** | Failed job alerts | 🟢 | 13/12/11 | — |

#### Other utility packages

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **laravel-notification-channels** (org) | Extra notification channels | 🟢 | 13/12/11 | Telegram, Slack, Discord, etc. |
| 🧩 **guzzlehttp/guzzle** | HTTP client | 🟢 | 13/12/11 | ~23k ★. Underlies Http facade |
| 🧩 **doctrine/dbal** | DB abstraction | 🟢 | 13/12/11 | Required for some migrations |
| 🧩 **predis/predis** | Pure-PHP Redis client | 🟢 | 13/12/11 | No ext-redis needed |
| **dyrynda/laravel-cascade-soft-deletes** | Cascade soft deletes | 🟢 | 13/12/11 | Recommended by LaravelDaily [reference:33] |
| **spatie/laravel-google-fonts** | Self-hosted Google Fonts | 🟢 | 13/12/11 | — |

---

### 6.24 Livewire / Frontend

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **livewire/livewire** | Full-stack reactive UI | 🟢 | 13/12/11 | ~23.5k ★ |
| **livewire/volt** | Single-file component syntax | 🟢 | 13/12 | — |
| **livewire/flux** | Official UI component library | 🟢 | 13/12 | Used in starter kits |
| **wire-elements/modal** | Modal component | 🟢 | 13/12/11 | ~2.1k ★ |
| **spatie/laravel-livewire-wizard** | Multi-step wizard | 🟢 | 13/12/11 | — |
| **spatie/laravel-livewire-flash** | Flash messages | 🟢 | 13/12/11 | — |
| **inertiajs/inertia-laravel** | Inertia adapter | 🟢 | 13/12/11 | ~2.1k ★ |
| **inertiajs/inertia** (JS) | Inertia JS client | 🟢 | — | SPA without API |
| ⭐ **laravel/echo** | WebSocket JS client | 🟢 | 13/12/11 | Pairs with Reverb |
| ⭐ **laravel/stream** | SSE streaming for LLMs | 🟢 | 13/12 | New |
| ⭐ **laravel/wayfinder** | Type-safe routes for TS | 🟢 | 13/12 | — |
| **tightenco/ziggy** | Named routes in JS | 🟢 | 13/12/11 | ~4.6k ★ |
| ⭐ **laravel/folio** | File-system routing | 🟢 | 13/12 | Next.js-style |

---

### 6.25 AI, Vector, Embeddings

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/ai** | First-party AI SDK | 🟢 | 13 | Text, tools, embeddings, images, audio. Unified API for OpenAI, Anthropic, Gemini, Groq, xAI. Classification (Jev), Vercel Chat, AG-UI. [reference:34] |
| **laraigent/larai-kit** | RAG & AI agent toolkit | 🟢 | 13/12 | Document ingestion, vector search, streaming chat, multi-tenant scoping. Works with OpenAI, Anthropic, Gemini, Pinecone, pgvector. [reference:35] |
| **solution-forest/ai-kit-core** | RAG toolkit engine | 🟢 | 13/12 | Ingestion, chunking, extraction, vector retrieval (sqlite-vec + pgvector), RAG agents on Laravel AI SDK. [reference:36] |
| **jati/rafurivel** | Zero-config VectorRAG | 🟢 | 13/12 | Bridges Eloquent models with Pinecone. Enterprise-grade. [reference:37] |
| 🧩 **pgvector/pgvector-php** | PostgreSQL pgvector client | 🟢 | 13/12/11 | Native vector search. Pairs with Laravel's `whereVectorSimilarTo()`. |
| **Laravel Related Content** (Vladislav Stoitsov) | Semantic relationships | 🟢 | 13 | Uses vector embeddings + pgvector for content discovery. [reference:38] |
| **openai-php/laravel** | OpenAI API wrapper | 🟢 | 13/12/11 | Community |
| **openai-php/client** | OpenAI PHP client | 🟢 | 13/12/11 | Framework-agnostic |
| **probots-io/ai** | Multi-provider AI | 🟢 | 13/12 | OpenAI, Anthropic, etc. |
| **echolabsdev/prism** | LLM integration package | 🟢 | 13/12 | Integrating LLMs into AI applications [reference:39] |

---

### 6.26 Observability

#### Metrics & Monitoring

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| ⭐ **laravel/pulse** | APM dashboard | 🟢 | 13/12/11 | First-party. See [Observability Deep Dive](#7-observability--deep-dive) |
| **lkaemmerling/laravel-horizon-prometheus-exporter** | Horizon → Prometheus | 🟢 | 13/12/11 | Actively maintained |
| **saschahemleb/laravel-prometheus-exporter** | General Prometheus exporter | 🟢 | 13/12/11 | Wraps promphp client |
| **aduzenko/laravel-configurable-prometheus** | Config-driven metrics | 🟢 | 13/12 | — |
| 🧩 **promphp/prometheus_client_php** | Prometheus PHP client | 🟢 | 13/12/11 | Framework-agnostic |

#### Tracing

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **keepsuit/laravel-opentelemetry** | OTel auto-instrumentation | 🟢 | 13/12/11 | Best choice. 500k+ installs. Auto-instruments HTTP, DB, queues, Redis, cache, events, Livewire, Scout. Explicit Octane support. |
| **open-telemetry/opentelemetry-auto-laravel** | Official OTel auto-instr | 🟢 | 13/12/11 | More manual |

#### Error Tracking

| Package | Purpose | Status | Compat | Notes |
|---|---|---|---|---|
| **sentry/sentry-laravel** | Sentry integration | 🟢 | 13/12/11 | Official. Exceptions, performance traces, breadcrumbs. |
| **bugsnag/bugsnag-laravel** | Bugsnag integration | 🟢 | 13/12/11 | Alternative |

---

### 6.27 Database & Infra

| Tool | Type | Notes |
|---|---|---|
| 🧩 **PgBouncer** | External | Postgres connection pooler. Use **session mode** for prepared statements/advisory locks |
| 🧩 **pgvector** | Postgres extension | Vector similarity search. Native support in Laravel 13. |
| 🧩 **PostGIS** | Postgres extension | Geospatial indexing — the scalable path beyond haversine-in-PHP |
| 🧩 **Redis Sentinel / Cluster** | External | HA Redis for queues + cache + sessions |
| 🧩 **librdkafka** | System lib | Required for ext-rdkafka |

---

### 6.28 Log Aggregation

| Tool | Type | Notes |
|---|---|---|
| 🧩 **monolog/monolog** | Library | Underlying logger Laravel ships with |
| 🧩 **Loki + Promtail** | External | Self-hosted log aggregation |
| **arcanedev/log-viewer** | Package | In-app log viewer |
| **spatie/laravel-tail** | Package | `artisan tail` |
| **opcodesio/log-viewer** | Package | Modern in-app log viewer |

---

## 7. Observability — Deep Dive

### Prometheus

| Package | Notes |
|---|---|
| **lkaemmerling/laravel-horizon-prometheus-exporter** | Horizon queue metrics for Prometheus — actively maintained |
| **saschahemleb/laravel-prometheus-exporter** | General-purpose wrapper around promphp/prometheus_client_php |
| **aduzenko/laravel-configurable-prometheus** | Config-driven metric definitions, targets Laravel 12/13 |
| **promphp/prometheus_client_php** | Underlying PHP Prometheus client |

**Storage adapter note:** Use Redis as the storage adapter for multi-worker/k8s deploys — in-memory and APCu don't share state across workers.

### OpenTelemetry

| Package | Notes |
|---|---|
| **keepsuit/laravel-opentelemetry** | Current best choice — 500k+ installs, active, Laravel 11/12/13. Auto-instruments HTTP, DB, queues, Redis, cache, events, Livewire, Scout. Explicit Octane worker-mode support. |
| **open-telemetry/opentelemetry-auto-laravel** | Official OTel PHP auto-instrumentation (more manual setup) |

**For Octane:** set `OTEL_*` env vars at process/container level, not just `.env`.

### Error Tracking

| Package | Notes |
|---|---|
| **sentry/sentry-laravel** | Official first-party integration — exceptions, performance traces, breadcrumbs |
| **bugsnag/bugsnag-laravel** | Alternative error tracking |

---

## 8. Queue Monitoring — Horizon vs Telescope vs Pulse

**Direct answer to "can I see queue/job reduction in Telescope?":** partially, not really for production monitoring.

| Tool | What It Shows | Fit for Job/Queue Visibility |
|---|---|---|
| ⭐ **laravel/horizon** | Purpose-built for Redis queues — live dashboard of jobs (pending/processing/completed/failed), throughput graphs, wait-time metrics, per-queue breakdown, failed job retry UI, tags for filtering by job type. | **This is the right tool for queue monitoring at scale.** Use this, not Telescope, for production job visibility. [reference:40] |
| ⭐ **laravel/telescope** | Records individual job dispatches/executions as part of general request/event debugging — good for "did this one job run and what did it do" | **Not built for live throughput/backlog monitoring** — it's a debug log, not an operations dashboard. Fine for dev, wrong tool for watching queue depth in prod. |
| ⭐ **laravel/pulse** | App-wide performance dashboard — slow jobs, slow queries, exceptions, usage by user, queue sizes as one panel among several. Cards for server health (CPU, memory, storage via `pulse:check`), top application usage, slow requests, slow jobs, slow queries, slow outgoing requests, cache hit/miss rates. [reference:41] | Good complementary high-level view; pairs with Horizon rather than replacing it. |
| **spatie/laravel-schedule-monitor** | Monitors scheduled tasks (cron), not queued jobs — alerts if a scheduled command didn't run | Different problem: use alongside Horizon, not instead of it |
| **Prometheus + Grafana** (via lkaemmerling/laravel-horizon-prometheus-exporter) | Exports Horizon's own metrics for long-term retention/alerting (Horizon's UI itself doesn't retain history well) | Add this once Horizon's built-in UI isn't enough for historical trend/alerting needs |

**For your setup:** Horizon as the primary queue dashboard (real-time, per-queue), Pulse for overall app health at a glance, Prometheus+Grafana exporter once you need alerting/history beyond what Horizon's UI retains. Telescope stays for local dev debugging only — don't rely on it in production at this scale.

---

## 9. University Multi-Module Platform Stack

Given the actual shape of the project — five Laravel projects: a combined booking system (hostel + transport + hall booking) and a separate full SIS (admissions → course catalog → marks → attendance) — here's what maps to each module.

### Booking System (Hostel / Transport / Hall)

| Package | Purpose |
|---|---|
| **spatie/laravel-model-states** | Booking state machine (requested → confirmed → checked-in → completed → cancelled) |
| **netsells/laravel-geoscope** | Distance/geofence queries for transport routing (nearest stop, route matching) |
| **spatie/laravel-google-calendar** | If hall/room bookings need calendar sync for staff |
| **Custom double-booking prevention:** DB-level unique constraints + pessimistic locking (`lockForUpdate()`) | Not a package — at this scale, race conditions on hostel room/hall slot booking need row-level locks, not application-level checks. This is the actual hard problem in a booking system, not a package gap. |
| **spatie/laravel-sluggable** | Clean URLs for hall/room listings |
| ⭐ **laravel/reverb** | Live seat/room availability updates without polling |
| **spatie/laravel-webhook-client / webhook-server** | If transport booking integrates with an external fleet/GPS provider |

### Student Information System (Admissions → Catalog → Courses → Marks → Attendance)

| Package | Purpose |
|---|---|
| **spatie/laravel-permission** | Role separation: student / faculty / admin / registrar — non-negotiable for a system this size |
| **spatie/laravel-model-states** | Admission pipeline state machine (applied → verified → admitted → enrolled → graduated) |
| **maatwebsite/excel** | Bulk marks upload/download, attendance import from biometric/RFID exports |
| **barryvdh/laravel-dompdf** or **spatie/laravel-pdf** | Marksheets, admit cards, transcripts, ID cards |
| **spatie/laravel-activitylog** | Audit trail — mandatory for marks/attendance edits (academic integrity, dispute resolution) |
| **spatie/laravel-medialibrary** | Admission documents, photos, certificates |
| **Attendance at scale:** Kafka (`mateusjunges/laravel-kafka`) or Redis Streams, not direct DB writes | If attendance is captured via biometric/RFID at thousands of scan events per minute across campus, direct synchronous DB writes will choke — queue the events, batch-write |
| **dedoc/scramble** | If SIS exposes an API to the booking system / mobile app — keep the OpenAPI spec accurate across 5 projects |

### Cross-Cutting (shared across all 5 projects)

| Need | Package/Approach |
|---|---|
| Single sign-on across all 5 Laravel apps | **laravel/passport** as a central OAuth2 server, or **workos/workos-php** for SSO — one auth service, not 5 separate login systems |
| Shared UI kit across projects | **filamentphp/filament** for all admin panels — consistent look/UX across hostel/transport/hall/SIS admin screens with one shared design system |
| Inter-service communication | **Kafka** (`mateusjunges/laravel-kafka`) — SIS enrolls a student → event → hostel/transport systems react (auto-allocate room, activate transport pass) without tight coupling |
| Shared config/secrets across 5 deployments | Not a package — a shared `.env` management strategy (Vault, or even a private Composer package holding shared config helpers) matters more at 5-project scale than any single package |

---

## 10. Docker at Scale

| Piece | Notes |
|---|---|
| **laravel/sail** | Fine for local dev, not what you run in production at 500k req/sec — don't confuse the two |
| **Multi-stage Dockerfile with FrankenPHP base image** | Production image should build once, run everywhere — Octane+FrankenPHP in the container, not PHP-FPM [reference:42] |
| **Docker Compose for local multi-service dev** (5 apps + Redis + Postgres + Kafka) | Practical for local dev across 5 interconnected Laravel projects; not what you'd run in prod at this scale — prod needs orchestration |
| **Kubernetes / Nomad, or your own Porter (Firecracker microVM)** | At 500k req/sec across 5 services, plain `docker run` on a few boxes isn't enough — you need real orchestration for autoscaling, rolling deploys, health-checked restarts. This is exactly the problem your own Porter project is aimed at — worth using your own tooling here rather than reaching for vanilla Coolify/Dokploy, which are built for much smaller scale. |
| **PgBouncer** | Mandatory in front of Postgres at this write volume — see [Database & Infra](#627-database--infra) |
| **Redis Sentinel or Redis Cluster** | A single Redis instance backing Horizon queues + cache + sessions will itself become the bottleneck at this scale — needs HA/clustering |

**Bottom line on Docker + 500k req/sec + 5 Laravel projects:** the container runtime (Docker) is the easy part. The hard part is orchestration and traffic shaping across 5 services with shared identity/auth and an event bus tying them together — that's an infra design problem your existing Porter/dispatchd-go work is already positioned to solve better than any Composer package list can.

---

## 🤝 Contributing

Add a package by opening a PR with:

- Package name and repository URL
- One-line description
- Status (Active / Maintained / Stale / Deprecated)
- Laravel compatibility (13 / 12 / 11)
- Why it belongs (one sentence, no marketing)

See [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.
