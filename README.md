# Nexledge Web 🖥️
> **The reactive face of Nexledge — AI-native, signal-driven, zoneless.**

Nexledge Web is the Angular frontend for [Nexledge](https://github.com/pravudatta10/nexledge), a high-performance AI-native platform. This repo is a hands-on learning project exploring the latest Angular 21 patterns — signals, zoneless change detection, and real-time AI streaming — while integrating with the Nexledge backend's Auth, Gateway, and Intelligence Router services.

---

## 🎯 Purpose

This project exists to explore modern Angular concepts in a real, non-trivial context rather than isolated tutorials:

- Signal-first state management (no NgRx/Zone.js crutches)
- Zoneless change detection in a production-shaped app
- Streaming UI patterns (SSE) against a real LLM-backed API
- Standalone-only architecture with strict enforcement

---

## 🛠️ Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Framework** | Angular 21 (standalone, zoneless) |
| **Reactivity** | Signals, `computed()`, `effect()`, `resource()` / `httpResource()` |
| **Styling** | Tailwind CSS |
| **HTTP** | `HttpClient` with Fetch backend (SSE-friendly) |
| **Auth** | OAuth 2.0 / OIDC against the Nexledge Auth Service |
| **Testing** | Vitest |
| **Build** | Angular CLI / esbuild |

---

## 🏛️ Architecture

Feature-based, signal-driven structure:

```
src/app/
  core/            # interceptors, guards, singleton services
  shared/          # presentational components, pipes, directives
  features/
    chat/          # AI streaming dashboard
    workspace/     # workspace management
    auth/          # login / OIDC callback handling
  data-access/     # signal-based services per domain (API + state)
```

- **Smart vs. presentational split** — feature components own signals via `data-access/` services; `shared/` components stay stateless.
- **Streaming** — the chat feature consumes Server-Sent Events from the Intelligence Router for token-by-token AI responses.
- **No gRPC in-browser** — the browser talks REST/SSE to the API Gateway; gRPC stays internal to the Java services.

---

## 🚀 Getting Started

### Prerequisites
- Node.js (LTS)
- Angular CLI 21 (`npm install -g @angular/cli@21`)
- A running instance of the [Nexledge backend](https://github.com/pravudatta10/nexledge) (Gateway + Auth + Intelligence Router)

### Setup

```bash
git clone https://github.com/<your-username>/nexledge-web.git
cd nexledge-web
npm install
ng serve
```

The app expects the Nexledge API Gateway to be reachable at the URL configured in `src/environments/environment.ts`.

---

## 🗺️ Roadmap

- [ ] **Phase 1:** Project scaffold, zoneless bootstrap, strict standalone config
- [ ] **Phase 2:** OIDC login flow against Nexledge Auth Service
- [ ] **Phase 3:** SSE-based AI streaming chat UI
- [ ] **Phase 4:** Workspace management & persisted sessions
- [ ] **Phase 5:** Scholar module UI (document upload & analysis)

---
