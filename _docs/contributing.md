---
layout: doc
title: "Đóng góp"
description: "Quy trình PR chuẩn, commit convention Conventional Commits, CODEOWNERS và hướng dẫn tham gia cộng đồng"
author: "@Dennis-nham"
version: "1.0.0"
okr: "O1"
breadcrumb:
  - title: "Tài liệu"
    url: "/"
  - title: "Đóng góp"
tags:
  - name: "Contributing"
    color: "green"
  - name: "Community"
    color: "blue"
prev:
  title: "White Paper"
  url: "/docs/white-paper/"
next: null
---

# 🤝 Hướng dẫn Đóng góp

Chào mừng bạn muốn đóng góp cho **@nlp-labs-vietnam**! Tài liệu này giải thích toàn bộ quy trình từ fork đến PR merged.

---

## Quy trình PR {#quy-trinh-pr}

```
1. Fork repo → 2. Tạo branch → 3. Code → 4. Commit → 5. Push → 6. Mở PR → 7. Review → 8. Merge
```

### Bước chi tiết

```bash
# 1. Fork trên GitHub, sau đó clone
git clone https://github.com/YOUR_USERNAME/ios-design-system.git
cd ios-design-system

# 2. Thêm upstream
git remote add upstream https://github.com/nlp-labs-vietnam/ios-design-system.git

# 3. Tạo branch (theo pattern bên dưới)
git checkout -b feat/ios-button-haptic

# 4. Làm việc, sau đó commit
git add .
git commit -m "feat(button): add haptic feedback support for iOS"

# 5. Push
git push origin feat/ios-button-haptic

# 6. Mở PR trên GitHub
gh pr create --title "feat(button): add haptic feedback" --body "..."
```

---

## Branch Pattern {#branch-pattern}

| Loại | Pattern | Ví dụ |
|---|---|---|
| Tính năng mới | `feat/<mô-tả>` | `feat/solar-rag-pipeline` |
| Sửa lỗi | `fix/<mô-tả>` | `fix/phobert-tokenizer-vi` |
| Tài liệu | `docs/<mô-tả>` | `docs/everest-vi-translation` |
| Refactor | `refactor/<mô-tả>` | `refactor/kafka-consumer` |
| Chore | `chore/<mô-tả>` | `chore/update-deps` |

---

## Commit Convention {#commit-convention}

Dự án tuân theo **[Conventional Commits](https://www.conventionalcommits.org/)**:

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### Các type hợp lệ

| Type | Khi nào dùng |
|---|---|
| `feat` | Thêm tính năng mới |
| `fix` | Sửa lỗi |
| `docs` | Thay đổi tài liệu |
| `style` | Format code (không thay đổi logic) |
| `refactor` | Refactor không thêm tính năng/sửa lỗi |
| `test` | Thêm hoặc sửa tests |
| `chore` | Build, CI/CD, dependencies |

### Ví dụ commit messages tốt

```bash
feat(solar-rag): add Vietnamese word segmentation before chunking
fix(ocpp): correct UTC+7 timezone offset in timestamp parser
docs(i18n): add Vietnamese translation for EVerest Getting Started
chore(deps): update phobert-base-v2 to latest checkpoint
```

---

## CODEOWNERS & Review {#review}

```
PR mở
 └─→ Module owner review (≤ 48 giờ)
       └─→ @Dennis-nham final approval (PRs ảnh hưởng kiến trúc)
             └─→ Merge vào main
```

| Loại PR | Yêu cầu approval |
|---|---|
| Hotfix | 1 approval từ bất kỳ Core Contributor |
| Feature | Module Owner + Project Lead |
| Architecture (`/infrastructure/`, `turbo.json`) | **Bắt buộc @Dennis-nham** |

---

## Code of Conduct

Dự án tuân theo [Contributor Covenant v2.1](https://github.com/Dennis-nham/Dennis-nham/blob/main/.profile/CODE_OF_CONDUCT.md). Mọi participant đều được đối xử tôn trọng.

Báo cáo vi phạm: [enterprise@nlpgroup.vn](mailto:enterprise@nlpgroup.vn)
