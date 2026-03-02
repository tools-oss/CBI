---
name: content-review
description: Review và đánh giá chất lượng content trước khi publish. Kiểm tra SEO, readability, E-E-A-T và cho feedback cải thiện.
argument-hint: [đường dẫn file draft]
user-invocable: true
allowed-tools: Read, Write, Glob, Grep
---

# Skill: Content Review

Review content: **$ARGUMENTS**

## Quy trình review

### 1. Đọc content brief
- Tìm brief tương ứng trong `02-Content/briefs/`
- So sánh draft với requirements trong brief

### 2. Đánh giá Content Quality

#### SEO Score (40 điểm)
| Tiêu chí | Điểm tối đa | Đánh giá |
|----------|-------------|----------|
| Title tag chuẩn SEO | 5 | |
| Meta description | 5 | |
| H1 chứa keyword | 5 | |
| Heading structure logic | 5 | |
| Keyword usage tự nhiên | 5 | |
| Internal links (3-5) | 5 | |
| External links (1-3) | 5 | |
| Image alt text | 5 | |

#### Content Quality Score (40 điểm)
| Tiêu chí | Điểm tối đa | Đánh giá |
|----------|-------------|----------|
| Đúng search intent | 10 | |
| Thông tin chính xác | 10 | |
| E-E-A-T signals | 5 | |
| Readability | 5 | |
| Actionable / useful | 5 | |
| Unique value vs SERP | 5 | |

#### Technical Score (20 điểm)
| Tiêu chí | Điểm tối đa | Đánh giá |
|----------|-------------|----------|
| Word count phù hợp | 5 | |
| Formatting (lists, bold, ...) | 5 | |
| No spelling/grammar errors | 5 | |
| CTA rõ ràng | 5 | |

### 3. Verdict
- **90-100:** Ready to publish
- **70-89:** Minor revisions needed
- **50-69:** Major revisions needed
- **< 50:** Rewrite required

## Output

```markdown
# Content Review: [Title]
**File:** [path]
**Reviewer:** Content Review Skill
**Ngày:** [date]

## Scores
- SEO: [X/40]
- Content Quality: [X/40]
- Technical: [X/20]
- **Total: [X/100]**

## Verdict: [Ready / Minor Revisions / Major Revisions / Rewrite]

## Feedback chi tiết
### Điểm tốt
1. ...

### Cần cải thiện
1. [Vấn đề] -> [Đề xuất fix cụ thể]
2. ...

### Lỗi cần fix ngay
1. ...
```

## Tham khảo
- Checklist: @../../02-Content/templates/content-checklist.md
- SOP: @../../SOP/Content/README.md
