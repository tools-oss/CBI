---
name: on-page-audit
description: Kiểm tra và đánh giá on-page SEO cho một URL hoặc nội dung. Trả về checklist đánh giá và recommendations cải thiện.
argument-hint: [URL hoặc tên file content]
user-invocable: true
allowed-tools: Read, Write, Glob, Grep, WebFetch
---

# Skill: On-Page SEO Audit

Kiểm tra on-page SEO cho: **$ARGUMENTS**

## Checklist đánh giá

### 1. Title Tag
- [ ] Có chứa primary keyword?
- [ ] Độ dài 50-60 ký tự?
- [ ] Unique (không trùng trang khác)?
- [ ] Compelling (thu hút click)?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

### 2. Meta Description
- [ ] Có chứa primary keyword?
- [ ] Độ dài 150-160 ký tự?
- [ ] Có CTA rõ ràng?
- [ ] Unique?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

### 3. URL Structure
- [ ] Ngắn gọn, có keyword?
- [ ] Không có parameter thừa?
- [ ] Lowercase, dùng hyphens?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

### 4. Heading Structure
- [ ] Có đúng 1 H1?
- [ ] H1 chứa primary keyword?
- [ ] H2-H3 logic, hierarchical?
- [ ] H2s cover main subtopics?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

### 5. Content Quality
- [ ] Word count phù hợp với SERP?
- [ ] Keyword density tự nhiên (1-2%)?
- [ ] Có data/statistics dẫn nguồn?
- [ ] E-E-A-T signals?
- [ ] Readability tốt?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

### 6. Internal Links
- [ ] Có 3-5 internal links?
- [ ] Anchor text descriptive?
- [ ] Link tới related content?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

### 7. Images
- [ ] Có alt text mô tả?
- [ ] File size optimized?
- [ ] Format tối ưu (WebP)?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

### 8. Schema Markup
- [ ] Có schema phù hợp?
- [ ] Valid (không có errors)?
- **Đánh giá:** ⬜ Pass / ⬜ Cần cải thiện / ⬜ Fail

## Output

Tạo file: `03-On-Page-SEO/audit_[date]_[slug].md`

```markdown
# On-Page Audit: [Page/URL]
**Ngày:** [date]
**Overall Score:** [X/8 pass]

## Summary
[Tóm tắt nhanh]

## Issues Found
1. [Issue] - [Severity] - [Fix suggestion]
2. ...

## Recommendations
1. [Action item cụ thể]
2. ...
```
