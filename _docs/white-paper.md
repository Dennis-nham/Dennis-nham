---
layout: doc
title: "White Paper"
description: "Sách trắng NLP Labs Vietnam — AI cho chuyển đổi năng lượng xanh và trí tuệ tài chính"
author: "NHAM QUOC HUAN"
version: "1.0.0"
okr: "O3 · O4"
breadcrumb:
  - title: "Tài liệu"
    url: "/"
  - title: "White Paper"
tags:
  - name: "White Paper"
    color: "purple"
  - name: "v1.0.0"
    color: "blue"
prev:
  title: "Tài trợ & Gọi vốn"
  url: "/docs/sponsorship/"
next:
  title: "Đóng góp"
  url: "/docs/contributing/"
---

# 📄 White Paper · NLP Labs Vietnam

> **Phiên bản:** 1.0.0 · **Tác giả:** NHAM QUOC HUAN · **Authorized Signatory:** [@Dennis-nham](https://github.com/Dennis-nham)

---

## Tóm tắt điều hành

**NLP Labs Vietnam** xây dựng hạ tầng AI cốt lõi để giải quyết hai bài toán lớn:

1. **Chuyển đổi năng lượng xanh** — RAG/LLM tư vấn thiết kế điện mặt trời áp mái, tích hợp EVerest/OCPP cho EV Charging
2. **Trí tuệ tài chính** — Phân tích cảm xúc thị trường thời gian thực bằng FinBERT + PhoBERT

**Vòng gọi vốn:** $50,000,000 USD Series A  
**Cloud credits mục tiêu:** ≥ $450,000 trong 90 ngày

---

## Bài toán & Cơ hội {#problem}

### Thị trường điện mặt trời Việt Nam

| Vấn đề | Hiện trạng | Cơ hội AI |
|---|---|---|
| Tư vấn sizing hệ thống | 4–8h/dự án thủ công | Tự động hóa 94% → 15 phút |
| Chi phí tư vấn | $40–80 USD/tư vấn | $0.5 (API call cost) |
| Sai số thiết kế | ±15–30% công suất | ≥ 92% chính xác |
| Rào cản ngôn ngữ | Tài liệu chỉ tiếng Anh | Vietnamese NLP pipeline |

---

## Giải pháp {#solution}

### Solar PV Advisory (RAG/LLM)

```
Người dùng nhập yêu cầu (tiếng Việt)
    → Vi-NLP Preprocessing (vi-tokenizer)
    → RAG Retrieval (Milvus/Qdrant)
    → LLM Generation (PhoBERT + solar domain)
    → Báo cáo tư vấn tự động (PDF/API)
```

### Investment Intelligence Platform

```
Reuters · Bloomberg · HNX/HOSE
    → Kafka ingestion
    → RabbitMQ orchestration
    → FinBERT sentiment + NER
    → gRPC/WebSocket API
    → Real-time dashboard
```

---

## Impact Metrics {#impact}

| Chỉ số | Năm 1 | Năm 3 |
|---|---|---|
| Tư vấn solar/tháng | 5,000 | 50,000 |
| Thời gian tư vấn | −94% (4h→15min) | −97% |
| Solar hỗ trợ lắp đặt | 10 MWp | 200 MWp |
| CO₂ tiết kiệm | ~11,000 tCO₂/năm | ~220,000 tCO₂/năm |
| EPC tích hợp API | 15 công ty | 150 công ty |

> CO₂ đóng góp vào mục tiêu NDC Việt Nam: giảm 43.5% phát thải đến 2030.

---

## Liên kết tài liệu đầy đủ

- [WHITE-PAPER.md đầy đủ trên GitHub](https://github.com/Dennis-nham/Dennis-nham/blob/main/.profile/WHITE-PAPER.md)
- [OSS-CONTRIBUTION-ROADMAP.md](https://github.com/Dennis-nham/Dennis-nham/blob/main/.profile/OSS-CONTRIBUTION-ROADMAP.md)
- [SPONSORSHIP.md](https://github.com/Dennis-nham/Dennis-nham/blob/main/.profile/SPONSORSHIP.md)
