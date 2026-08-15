# Nexledge Web 🚀

> **Architecting the Next Ledge of Intelligence.**

![Angular](https://img.shields.io/badge/Angular-21-DD0031?logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-AI--Native-6E56CF)
![Status](https://img.shields.io/badge/Status-Active%20Development-orange)
![License](https://img.shields.io/badge/License-TBD-lightgrey)

## AI-Native Intelligence Workspace

**Nexledge Web** is the frontend application for the **Nexledge AI Platform**.

It is being built as a high-performance, AI-native workspace that goes beyond a traditional chatbot. Nexledge brings together conversational AI, software engineering assistance, interview preparation, reusable prompt workflows, knowledge retrieval, persistent memory, and AI-generated artifacts into a unified professional workspace.

The application is designed to evolve from a real-time AI chat experience into a multi-purpose intelligence platform without requiring architectural rewrites as new capabilities are introduced.

```text
                           NEXLEDGE
                                │
                                ▼
               AI-NATIVE INTELLIGENCE WORKSPACE
                                │
            ┌───────────────────┼───────────────────┐
            │                   │                   │
            ▼                   ▼                   ▼
         EXPLORE               BUILD                GROW
            │                   │                   │
       Understand          Create & Solve      Learn & Improve
```

---

## ✨ Product Vision

Nexledge is designed around a simple idea:

> **AI should be an intelligent workspace, not just a chat window.**

A user should be able to start with a question and progressively transform the result into something useful.

```text
User Intent
     │
     ▼
AI Interaction
     │
     ├── Conversation
     ├── Code
     ├── Architecture
     ├── Document
     ├── Research
     ├── Presentation
     ├── Image
     └── Other AI Artifacts
```

The platform supports multiple professional workflows while sharing a common intelligence layer, context model, memory system, and workspace architecture.

---

## 🧭 Product Domains

### 🔍 Explore
Understand, research, discover, and interact with information.
- AI Conversations
- Research
- Knowledge Exploration
- Document Intelligence
- Persistent Context
- AI Memory
- Prompt Library

### 🛠️ Build
Create, analyze, and engineer.
- Code Studio
- Code Review
- Refactoring
- Test Generation
- Architecture Analysis
- Software Design
- Document / PDF / Presentation / Image / Media Generation

### 📈 Grow
Improve professional and technical capabilities.
- Interview Lab
- Mock Interviews
- Technical Question Banks
- AI Feedback
- Skill Tracking
- Learning Progress
- Personalized Improvement Areas

### 🧠 Knowledge
Manage reusable intelligence and context.
- Prompt OS
- Personal Knowledge
- Documents
- Memory
- Context Sources
- AI Artifacts
- Reusable Workflows

---

## 🏛️ Nexledge Ecosystem

Nexledge Web is the presentation and interaction layer of the larger Nexledge platform.

```text
┌─────────────────────────────────────────────────────────────────────┐
│                              USER                                   │
└─────────────────────────────────┬───────────────────────────────────┘
                                  │
                                  ▼
┌─────────────────────────────────────────────────────────────────────┐
│                          NEXLEDGE WEB                               │
│                                                                     │
│ Angular 21 • Zoneless • Signals • Streaming • Responsive UI        │
│                                                                     │
│  ┌──────────────┬──────────────┬──────────────┬──────────────────┐ │
│  │   EXPLORE    │    BUILD     │     GROW     │    KNOWLEDGE     │ │
│  │ Intelligence │ Code Studio  │ Interview    │ Prompt Library   │ │
│  │ Conversations│ Architecture │ Skill Map    │ Memory           │ │
│  │ Research     │ Media Studio │ Progress     │ Documents        │ │
│  └──────────────┴──────────────┴──────────────┴──────────────────┘ │
└─────────────────────────────────┬───────────────────────────────────┘
                                  │
                              /api/*
                                  │
                                  ▼
                       (see Nexledge Platform README)
```

Nexledge Web talks exclusively to the **API Gateway**; it has no direct dependency on backend service hostnames or AI providers. See the companion **Nexledge Platform README** for everything behind `/api/*`.

---

## 🖥️ Frontend Architecture

Feature-oriented, target structure:

```text
src/
├── app/
│   ├── core/
│   │   ├── api/
│   │   ├── auth/
│   │   ├── config/
│   │   ├── errors/
│   │   ├── streaming/
│   │   └── telemetry/
│   │
│   ├── design-system/
│   │   ├── tokens/
│   │   ├── primitives/
│   │   └── patterns/
│   │
│   ├── shell/
│   │   ├── app-shell/
│   │   ├── navigation/
│   │   ├── sidebar/
│   │   ├── topbar/
│   │   └── command-bar/
│   │
│   ├── features/
│   │   ├── intelligence/
│   │   │   ├── chat/
│   │   │   ├── conversations/
│   │   │   ├── artifacts/
│   │   │   └── context/
│   │   │
│   │   ├── knowledge/
│   │   │   ├── memory/
│   │   │   ├── documents/
│   │   │   └── prompt-library/
│   │   │
│   │   ├── build/
│   │   │   ├── code-studio/
│   │   │   ├── architecture/
│   │   │   └── media-studio/
│   │   │
│   │   └── growth/
│   │       ├── interview-lab/
│   │       ├── skills/
│   │       └── progress/
│   │
│   ├── app.routes.ts
│   ├── app.config.ts
│   └── app.component.ts
│
├── assets/
│
└── styles/
    ├── global.css
    ├── theme.css
    └── utilities.css
```

New modules are added only when their implementation phase begins — no upfront scaffolding of unbuilt features.

---

## ⚡ Technology Stack (Frontend)

| Layer                  | Technology                       |
| ----------------------- | --------------------------------- |
| Framework                | Angular 21                        |
| Language                 | TypeScript                        |
| Component Architecture   | Standalone Components             |
| Change Detection         | Zoneless                          |
| State Management         | Angular Signals                   |
| Streaming                | Fetch API / ReadableStream / SSE  |
| Styling                  | CSS Design Tokens                 |
| Testing                  | Vitest                            |
| API Layer                | HTTP APIs (via API Gateway)       |

---

## 🔄 AI Streaming Architecture

```text
Chat Input → Chat Store (Signals) → Chat API Service → Streaming Client (SSE)
   → API Gateway → AI Platform → AI Provider
```

The component layer stays independent of HTTP and stream-parsing logic. Planned stream event types:

```text
TOKEN
STATUS
TOOL_CALL
TOOL_RESULT
ARTIFACT
COMPLETE
ERROR
```

---

## 🧩 State Management

```text
SERVER STATE      → Conversations, Artifacts, User, Prompts, Knowledge
FEATURE STATE      → Chat, Code Studio, Interview Lab, Media Studio
UI STATE           → Sidebar, Panels, Dialogs, Selected Views
```

Flow: `Angular Signals → Feature Stores → Services → API / Streaming`

A global state framework is introduced only if application complexity creates a clear requirement.

---

## 🎨 Design System

Independent visual identity, built around: **Precision, Intelligence, Engineering, Depth, Speed, Clarity**.

```text
design-system/
└── tokens/
    ├── colors.css
    ├── typography.css
    ├── spacing.css
    ├── radius.css
    ├── elevation.css
    ├── motion.css
    ├── breakpoints.css
    └── z-index.css
```

Component layers: **Primitives** (Button, Input, Icon, Badge, Dialog) → **Patterns** (Empty State, Loading State, Error State, Artifact Card, Command Palette, AI Status).

---

## ✍️ Universal Intelligence Composer

The long-term central interaction model:

```text
User Request → Context Assembly (Conversation, Workspace, Memory,
Documents, Files, Tool Results) → Intelligence Router → AI / Tool / Job
```

Starts as a focused chat input and evolves as backend capabilities become available.

---

## 📦 AI Response & Artifact System

```text
AI Response → Structured Output (Text, Markdown, Code, Table, Diagram, Artifact)
   → Artifact Viewer → PDF / PPT / Image
```

Artifact lifecycle: `QUEUED → PROCESSING → STREAMING → COMPLETED / FAILED / CANCELLED`

---

## 🧠 Memory & Context Inspector

The frontend will expose a **Context Inspector** giving visibility into retrieved context and sources — without exposing private model reasoning. Backing pipeline (chunking, embedding, retrieval) lives in the Nexledge Platform.

---

## 💻 Code Studio, 🎯 Interview Lab, 🎨 Media Studio

- **Code Studio** — Explain, Review, Refactor, Test Generation, Optimize, Diff Comparison, Architecture Analysis (Monaco Editor, lazy loaded).
- **Interview Lab** — Structured mock interviews with AI evaluation across Accuracy, Depth, Clarity, Communication, and Improvement Areas; longitudinal skill tracking.
- **Media & Artifact Studio** — Job-based generation of Documents, PDFs, Presentations, Images, Diagrams, and (future) short-form video, with live job status.

---

## ⚡ Performance Strategy

```text
Zoneless + Signals + Lazy Loaded Features + @defer
   + Virtual Scrolling + Web Workers + Code Splitting
```

Heavy modules (Monaco Editor, PDF Viewer, Presentation Editor, Media Preview, large viz libraries) are excluded from the initial bundle and loaded on demand.

---

## 🧪 Testing Strategy

```text
                    E2E Tests
                       ▲
                Integration Tests
                       ▲
                    Unit Tests
```

- **Unit** — Feature Stores, Services, Utilities, Domain Logic, Streaming Parsing
- **Integration** — Component + Store interaction, API clients, streaming flows, error recovery
- **E2E** — Login → Open Workspace → Send Prompt → Receive Streaming Response → Save Conversation → Retrieve Context → Generate Artifact

---

## 🔐 Authentication

OAuth2/OIDC via the platform Auth Service (Google, GitHub). Frontend responsibilities: token refresh, route guards, protected API calls, user profile, workspace identity, session management.

---

## 🌐 API Integration

```text
Angular Application → /api/* → API Gateway → Backend Services
```

Target API domains:
```text
/api/auth  /api/chat  /api/conversations  /api/workspaces
/api/memory  /api/knowledge  /api/prompts  /api/interview
/api/artifacts  /api/jobs
```

The frontend never depends directly on individual backend service hostnames.

---

## 🗺️ Frontend Roadmap

| Status | Meaning              |
| ------ | --------------------- |
| 🟢     | Foundation Available  |
| 🟡     | In Progress            |
| 🔵     | Planned                |
| ⚪     | Future / Research      |

- 🟡 **Phase 1 — Angular AI Experience**: Zoneless app shell, design tokens, streaming chat, markdown/code rendering, loading/error states.
  *Exit criteria: a user can open Nexledge, send a prompt, and watch the AI response stream in real time.*
- 🔵 **Phase 2 — Identity & Platform**: OAuth2/OIDC login, route guards, token refresh, protected APIs, workspace identity.
- 🔵 **Phase 3 — Core AI Workspace**: Conversation persistence/history, structured AI responses, artifact foundation, retry & recovery.
- 🔵 **Phase 4 — Memory & RAG**: Context Inspector surfaced in-app.
- 🔵 **Phase 5 — Prompt OS**: Prompt CRUD, categories, tags, variables, versioning, forking, search UI.
- 🔵 **Phase 6 — Professional Workspaces**: Code Studio, Interview Lab, Media & Artifact Studio.
- ⚪ **Phase 7 — Intelligence Extensions**: Tool activity surfacing, agent workflow UI, conversation branching, context visibility, model routing UI.
- ⚪ **Phase 8 — Scale & Hardening**: Frontend telemetry, SSR/prerendering for public pages, production monitoring.

---

## 🧱 Architecture Principles

1. Feature-oriented architecture
2. Streaming-first AI interaction
3. Signal-first frontend state
4. Clear separation between UI, state, API, and infrastructure
5. Stable API contracts
6. No direct frontend dependency on AI providers
7. Context is a first-class concept
8. AI outputs can become reusable artifacts
9. Heavy capabilities are lazy loaded
10. Async work is modeled explicitly as jobs
11. MCP and agents are introduced only when the platform foundation supports them
12. Future capabilities extend the architecture instead of requiring rewrites
13. A phase is not complete until its exit criteria work end-to-end

---

## 📁 Development

### Prerequisites
- Node.js LTS
- npm
- Angular CLI 21
- Running Nexledge backend services (see Nexledge Platform README)

### Install Dependencies
```bash
npm install
```

### Start Development Server
```bash
ng serve
```
Available at `http://localhost:4200`

### Production Build
```bash
ng build
```

### Run Unit Tests
```bash
ng test
```

---

> **Nexledge**
>
> **Architecting the Next Ledge of Intelligence.**
