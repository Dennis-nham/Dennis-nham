---
layout: doc
title: "Kiến trúc hệ thống"
description: "Sơ đồ monorepo 4 repository, tech stack đầy đủ và luồng dữ liệu giữa các service"
author: "@Dennis-nham"
version: "1.0.0"
okr: "O1"
breadcrumb:
  - title: "Tài liệu"
    url: "/"
  - title: "Kiến trúc"
tags:
  - name: "Architecture"
    color: "purple"
  - name: "Monorepo"
    color: "blue"
prev:
  title: "Bắt đầu"
  url: "/docs/get-started/"
next:
  title: "OSS Roadmap"
  url: "/docs/oss-roadmap/"
---

# 🗺 Kiến trúc hệ thống

Tổ chức **@nlp-labs-vietnam** vận hành theo mô hình **monorepo phân tán** — 4 repository độc lập, mỗi repo có Turborepo riêng, kết nối với nhau qua shared packages.

---

## Tổng quan tổ chức {#tong-quan}

```
╔══════════════════════════════════════════════════════════╗
║        @nlp-labs-vietnam  ·  GitHub Organization        ║
║   AI for Clean Energy · Vietnamese NLP · FinIntelligence ║
╚══════════════════════════════════════════════════════════╝
         │
         ├── 🎨  ios-design-system      (@thekingbao)
         ├── 📈  investment-platform    (@nhamlapquoc)
         ├── 🧠  core-nlp               (@nhamlapquoc)
         ├── 📦  wikialisa-labs         (@wikialisalabs)
         └── ⚙️  .github  [org root]   (@Dennis-nham)
```

---

## ios-design-system {#ios-design-system}

> **Owner:** [@thekingbao](https://github.com/thekingbao) · Turborepo · `@alisababivip/*` · Apple HIG

Design language chuẩn iOS HIG, framework-agnostic, token-driven:

| Package | Mô tả |
|---|---|
| `@alisababivip/tokens` | CSS Variables + JSON Design Tokens (màu sắc, typography, spacing) |
| `@alisababivip/icons` | SVG Icons + SF Symbols |
| `@alisababivip/core` | Web Components thuần CSS |
| `@alisababivip/react` | React 18 wrapper components |
| `@alisababivip/vue` | Vue 3 wrapper (Composition API) |
| `@alisababivip/blade` | Laravel Blade bridge |

---

## investment-platform {#investment-platform}

> **Owner:** [@nhamlapquoc](https://github.com/nhamlapquoc) · Kafka · RabbitMQ · FinBERT · Milvus

Nền tảng phân tích cảm xúc thị trường tài chính thời gian thực:

```
🌍 External Data (Reuters · Bloomberg · HNX/HOSE · Social)
         │
 🌊 ingestion/     ← Apache Kafka (millions events/sec)
         │
 🐇 orchestrator/  ← RabbitMQ routes to workers
    ┌────┴────┐
 🧠 nlp-    🔍 nlp-
  sentiment/  ner/
 (FinBERT+RAG) (Entity)
    └────┬────┘
 🌐 api-gateway/   ← gRPC · REST · WebSocket
         │
 📊 dashboard/     ← Real-time trading signals UI
```

---

## core-nlp {#core-nlp}

> **Owner:** [@nhamlapquoc](https://github.com/nhamlapquoc) · PhoBERT · HuggingFace · Solar RAG

| Module | Công nghệ |
|---|---|
| `models/vi-bert-base` | Vietnamese BERT (PhoBERT-based) |
| `models/vi-finbert` | Financial Vietnamese BERT |
| `pipeline/tokenizer` | Vietnamese word segmentation |
| `research/solar-rag` | RAG pipeline cho solar PV advisory |
| `packages/vi-tokenizer` | npm: `@nlp-labs-vietnam/vi-tokenizer` |

---

## Tech Stack tổng thể {#tech-stack}

| Layer | Technology |
|---|---|
| **Monorepo** | Turborepo · pnpm workspaces · Node ≥ 20 |
| **Frontend** | React 18 · Vue 3 · Vite · VitePress |
| **Design** | Apple HIG · CSS Custom Properties · Web Components |
| **Backend** | Node.js (Fastify) · gRPC · WebSocket |
| **Streaming** | Apache Kafka · RabbitMQ |
| **AI/NLP** | HuggingFace Transformers · PyTorch · FinBERT · PhoBERT |
| **RAG** | Milvus · Qdrant · LangChain |
| **Database** | PostgreSQL · Redis · Milvus (vector) |
| **Infra** | Docker · Nginx · PM2 · GitHub Actions |
| **Package registry** | npm (`@alisababivip/*`, `@nlp-labs-vietnam/*`) |
