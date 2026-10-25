---
layout: doc
title: "OSS Roadmap"
description: "Lộ trình 12 tuần đóng góp mã nguồn mở — EVerest, HuggingFace, Qdrant, Carbon Design System"
author: "@Dennis-nham"
version: "1.0.0"
okr: "O1 · O2 · O3"
breadcrumb:
  - title: "Tài liệu"
    url: "/"
  - title: "OSS Roadmap"
tags:
  - name: "OSS"
    color: "green"
  - name: "12 tuần"
    color: "orange"
prev:
  title: "Kiến trúc hệ thống"
  url: "/docs/architecture/"
next:
  title: "Tài trợ & Gọi vốn"
  url: "/docs/sponsorship/"
---

# 🌐 OSS Contribution Roadmap

Lộ trình **12 tuần** đóng góp vào các dự án OSS lớn để xây dựng uy tín kỹ thuật, unlock cloud credits $450k và đạt GitHub Accelerator.

<div class="callout note">
  <span class="callout-icon">📊</span>
  <div class="callout-content">
    <strong>Tiến độ Sprint Tuần 1</strong>
    48/49 issues đã mở · 34 repos tiếp cận · 100% nhóm D1–D7 hoàn thành.
    Xem <a href="https://github.com/Dennis-nham/Dennis-nham/blob/main/.profile/OSS-FUNDING-SPRINT-WEEK1.md">tracking file đầy đủ</a>.
  </div>
</div>

---

## Ba lý do chiến lược {#ly-do}

1. **Unlock cloud credits** — Google/Azure/AWS Activate ưu tiên dự án có OSS contribution thực tế
2. **Tech branding** cho Pitch Deck $50M — "active contributor" profile + LF Energy member status
3. **Tuyển maintainer tier 1** — kỹ sư giỏi gia nhập org có OSS activity thực sự

---

## Phase 1 — Establish Presence (Tuần 1–4) {#phase1}

| # | Task | Owner | Tag | Unlock |
|---|---|---|---|---|
| 1.1 | Enable GitHub Sponsors org | @Dennis-nham | `github` | MRR |
| 1.2 | PR: Vietnamese docs EVerest | @Dennis-nham | `everest` | LF Energy |
| 1.3 | Join EVerest Slack + mailing list | @Dennis-nham | `everest` | Community |
| 1.4 | Upload vi-tokenizer → HuggingFace | @nhamlapquoc | `ai` | ZeroGPU |
| 1.5 | Nộp Google for Startups ($200k) | @Dennis-nham | `cloud` | GCP credits |
| 1.6 | Đăng ký NVIDIA Inception | @Dennis-nham | `cloud` | GPU credits |

## Phase 2 — Active Contribution (Tuần 5–8)

| # | Task | Owner | Tag | Unlock |
|---|---|---|---|---|
| 2.1 | PR kỹ thuật EVerest: OCPP timezone | @Dennis-nham | `everest` | LF TSC invite |
| 2.2 | PR Qdrant: Vietnamese text example | @nhamlapquoc | `ai` | Qdrant credits |
| 2.3 | PR Carbon DS: dark-mode token fix | @thekingbao | `ios` | IBM recognition |
| 2.4 | Nộp Microsoft Founders Hub ($150k) | @Dennis-nham | `cloud` | Azure credits |
| 2.5 | Tìm referral → AWS Activate ($100k) | @Dennis-nham | `cloud` | AWS credits |

## Phase 3 — Strategic Partnership (Tuần 9–12)

| # | Task | Owner | Tag | Unlock |
|---|---|---|---|---|
| 3.1 | Đề xuất LF Energy Associate Member | @Dennis-nham | `everest` | Logo tại lfenergy.org |
| 3.2 | Nộp GitHub Accelerator (≥3 merged PR) | @Dennis-nham | `github` | $120k |
| 3.3 | Submit ViFinNLU benchmark HuggingFace | @nhamlapquoc | `ai` | Academic grant |
| 3.4 | Tiếp cận GIZ Vietnam + UNDP | @Dennis-nham | `fund` | NGO grant |

---

## Sprint Tuần 1 — Kết quả thực tế {#sprint}

| Nhóm | Repos | Issues | Trạng thái |
|---|---|---|---|
| D1 — LF Energy / EVerest | 2 | 3 | ✅ DONE |
| D2 — AI/ML Frameworks | 5 | 5 | ✅ DONE |
| D3 — Cloud Provider OSS | 5 | 5 | ✅ DONE |
| D4 — Vector DB / RAG | 7 | 11 | ✅ DONE |
| D5 — iOS / UI | 5 | 10 | ✅ DONE |
| D6 — Vietnamese NLP | 4 | 8 | ✅ DONE |
| D7 — Grant Orgs | 6+1 SKIP | 6 | ⚠️ PARTIAL |
| **TỔNG** | **34 repos** | **48 issues** | **✅** |

---

## Ma trận ưu tiên

```
         │ Impact Cao                │ Impact Thấp
─────────┼───────────────────────────┼──────────────────────
Effort   │ 🟢 BẮT ĐẦU NGAY         │ 🟡 SONG SONG
Thấp     │ • Vietnamese README EVerest│ • Star/Watch repos
         │ • Upload vi-tokenizer HF  │ • Join EVerest Slack
─────────┼───────────────────────────┼──────────────────────
Effort   │ 🔵 LÊN KẾ HOẠCH         │ 🔴 TRÌ HOÃN
Cao      │ • OCPP locale PR EVerest  │ • Fork full EVerest
         │ • vi-financial-news dataset│ • Custom OCPP stack
```
