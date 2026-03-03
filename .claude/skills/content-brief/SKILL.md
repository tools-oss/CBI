---
name: content-brief
description: Tạo content brief chi tiết cho writer dựa trên keyword. Bao gồm outline, SERP analysis, word count, và SEO guidelines.
argument-hint: [primary keyword]
user-invocable: true
allowed-tools: Read, Write, Glob, Grep, WebSearch, WebFetch
---

# Skill: Content Brief

Tạo content brief cho keyword: **$ARGUMENTS**

## Quy trình thực hiện

### Bước 1: SERP Analysis
- Search "$ARGUMENTS" và phân tích top 5-10 kết quả
- Ghi nhận: word count, heading structure, content format
- Xác định content type phù hợp nhất

### Bước 2: Search Intent
- Xác định intent chính (Informational/Commercial/Transactional)
- Hiểu user cần gì khi search keyword này
- Xác định stage trong customer journey

### Bước 3: Outline
Tạo heading structure dựa trên SERP analysis:
- H1: chứa primary keyword
- H2s: cover main subtopics từ SERP
- H3s: chi tiết cho mỗi subtopic
- FAQ section nếu có PAA data

### Bước 4: SEO Guidelines
- Title tag suggestion (50-60 ký tự)
- Meta description suggestion (150-160 ký tự)
- Target word count (dựa trên competitor average)
- Internal link opportunities
- Schema markup recommendation

## Output

Tạo file: `02-Content/briefs/brief_[date]_[keyword-slug].md`

Sử dụng template từ: @../../02-Content/templates/content-brief-template.md

## Sau khi hoàn thành
- Thông báo brief đã sẵn sàng cho Content Writer
- Cập nhật content calendar nếu có deadline

## Tham khảo SOP
Xem thêm: @../../SOP/Content/README.md
