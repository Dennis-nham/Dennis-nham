---
layout: doc
title: "Bắt đầu"
description: "Tổng quan về NLP Labs Vietnam, cách thiết lập môi trường và bước đầu tiên tham gia cộng đồng"
author: "@Dennis-nham"
version: "1.0.0"
okr: "O1 · O2"
breadcrumb:
  - title: "Tài liệu"
    url: "/"
  - title: "Bắt đầu"
tags:
  - name: "Quick Start"
    color: "green"
  - name: "Community"
    color: "blue"
prev: null
next:
  title: "Kiến trúc hệ thống"
  url: "/docs/architecture/"
---

# 🚀 Bắt đầu với NLP Labs Vietnam

NLP Labs Vietnam là tổ chức nghiên cứu và phát triển phần mềm **mã nguồn mở (MIT)**, xây dựng hạ tầng AI cốt lõi cho chuyển đổi năng lượng xanh và trí tuệ tài chính tại Việt Nam và Đông Nam Á.

<div class="callout note">
  <span class="callout-icon">ℹ️</span>
  <div class="callout-content">
    <strong>Chào mừng contributor mới!</strong>
    Bắt đầu bằng cách đọc tài liệu này, sau đó xem <a href="/docs/contributing/">hướng dẫn đóng góp</a> để gửi PR đầu tiên.
  </div>
</div>

---

## Tổ chức là gì? {#gioi-thieu}

**@nlp-labs-vietnam** hoạt động trên 4 repository cốt lõi:

| Repository | Owner | Mục đích |
|---|---|---|
| `ios-design-system` | [@thekingbao](https://github.com/thekingbao) | Apple HIG design tokens · `@alisababivip/*` |
| `investment-platform` | [@nhamlapquoc](https://github.com/nhamlapquoc) | Kafka · RabbitMQ · FinBERT · RAG |
| `core-nlp` | [@nhamlapquoc](https://github.com/nhamlapquoc) | PhoBERT · vi-tokenizer · solar RAG |
| `wikialisa-labs` | [@wikialisalabs](https://github.com/wikialisalabs) | tree-sitter-vi · open standards |

---

## Thiết lập môi trường {#cai-dat}

### Yêu cầu hệ thống

- **Node.js** ≥ 20 LTS
- **pnpm** ≥ 8
- **Python** ≥ 3.11 (cho core-nlp)
- **Git** ≥ 2.40
- **GitHub CLI** (`gh`) — khuyên dùng

### Clone và cài đặt

```bash
# Clone repo bạn muốn contribute
git clone https://github.com/nlp-labs-vietnam/ios-design-system.git
cd ios-design-system

# Cài dependencies (dùng pnpm)
pnpm install

# Build tất cả packages
pnpm turbo build

# Chạy docs local
pnpm --filter docs dev
```

### Cấu hình Git

```bash
git config user.name  "Tên của bạn"
git config user.email "email@example.com"

# Thiết lập commit signing (khuyến nghị)
git config commit.gpgsign true
```

---

## Tài khoản cần thiết {#tai-khoan}

<div class="callout tip">
  <span class="callout-icon">✅</span>
  <div class="callout-content">
    <strong>Checklist trước khi bắt đầu</strong>
    Hoàn thành danh sách dưới đây để đóng góp hiệu quả nhất.
  </div>
</div>

- [ ] **GitHub account** — tham gia [@nlp-labs-vietnam](https://github.com/nlp-labs-vietnam)
- [ ] **HuggingFace account** — upload datasets và models
- [ ] **EVerest Slack** — join tại [lfenergy.slack.com](https://lfenergy.slack.com) (kênh `#everest`)
- [ ] **LF Energy mailing list** — subscribe tại [lists.lfenergy.org](https://lists.lfenergy.org)
- [ ] **Discord NLP Labs** — liên hệ [@Dennis-nham](https://github.com/Dennis-nham)

---

## Bước tiếp theo {#buoc-tiep-theo}

Sau khi thiết lập xong môi trường, hãy khám phá:

1. **[Kiến trúc hệ thống](../architecture/)** — Hiểu toàn bộ monorepo trước khi code
2. **[OSS Roadmap](../oss-roadmap/)** — Xem sprint hiện tại và cách tham gia
3. **[Hướng dẫn đóng góp](../contributing/)** — Quy trình PR chuẩn, commit convention
4. **[Tài trợ](../sponsorship/)** — Tìm hiểu cách hỗ trợ dự án

---

## Nhận hỗ trợ

| Kênh | Mục đích |
|---|---|
| [GitHub Issues](https://github.com/nlp-labs-vietnam/.github/issues) | Báo lỗi, yêu cầu tính năng |
| [GitHub Discussions](https://github.com/orgs/nlp-labs-vietnam/discussions) | Thảo luận kỹ thuật, câu hỏi |
| [enterprise@nlpgroup.vn](mailto:enterprise@nlpgroup.vn) | Hợp tác doanh nghiệp, tài trợ |
| [@Dennis-nham](https://github.com/Dennis-nham) | Project Lead trực tiếp |
