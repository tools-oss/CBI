---
name: reporting
description: Tạo báo cáo SEO (tuần hoặc tháng). Tổng hợp ranking, traffic, content performance và recommendations.
argument-hint: [weekly hoặc monthly] [YYYY-MM-DD]
user-invocable: true
allowed-tools: Read, Write, Glob, Grep
---

# Skill: SEO Reporting

Tạo báo cáo: **$ARGUMENTS**

## Xác định loại báo cáo

Dựa trên $ARGUMENTS, chọn template phù hợp:
- **weekly** -> Báo cáo tuần
- **monthly** -> Báo cáo tháng

---

## Template: Báo cáo tuần

Tạo file: `06-Analytics-Reporting/weekly-reports/weekly_[YYYY]-W[NN].md`

```markdown
# Báo cáo SEO Tuần [W##] - [Date Range]

## Highlights
- [1-3 điểm nổi bật trong tuần]

## Ranking Changes
### Top Movers (Up)
| Keyword | Vị trí trước | Vị trí hiện tại | Thay đổi |
|---------|-------------|-----------------|----------|

### Top Movers (Down)
| Keyword | Vị trí trước | Vị trí hiện tại | Thay đổi |
|---------|-------------|-----------------|----------|

## Traffic Overview
- Organic sessions: [N] ([+/-]% vs tuần trước)
- New users: [N]
- Top pages by traffic: ...

## Content Published
| Bài viết | Ngày publish | Target keyword | Status |
|----------|-------------|---------------|--------|

## Tasks Completed
- [x] ...

## Tasks Next Week
- [ ] ...

## Notes
[Ghi chú quan trọng]
```

---

## Template: Báo cáo tháng

Tạo file: `06-Analytics-Reporting/monthly-reports/monthly_[YYYY]-[MM].md`

```markdown
# Báo cáo SEO Tháng [MM/YYYY]

## Executive Summary
[Tóm tắt 3-5 câu cho leadership]

## KPIs
| Metric | Target | Actual | vs Tháng trước | Status |
|--------|--------|--------|----------------|--------|
| Organic Traffic | ... | ... | ... | ... |
| Keywords Top 10 | ... | ... | ... | ... |
| Keywords Top 3 | ... | ... | ... | ... |
| Backlinks mới | ... | ... | ... | ... |
| Content published | ... | ... | ... | ... |

## Ranking Distribution
- Top 3: [N] keywords
- Top 10: [N] keywords
- Top 20: [N] keywords
- Top 100: [N] keywords

## Traffic Analysis
### By Channel
### By Landing Page (Top 10)
### By Device

## Content Performance
| Bài viết | Traffic | Avg Position | CTR | Conversions |
|----------|---------|-------------|-----|-------------|

## Link Building
- New backlinks: [N]
- New referring domains: [N]
- Top links acquired: ...

## Technical Health
- Crawl errors: [N]
- Core Web Vitals: [status]
- Index coverage: [N] pages

## Competitor Movements
[Thay đổi đáng chú ý từ đối thủ]

## Recommendations for Next Month
1. [Priority 1]
2. [Priority 2]
3. [Priority 3]

## Risks & Blockers
- [Nếu có]
```

## Thu thập data từ
- `06-Analytics-Reporting/ranking-tracking/` - Ranking data
- `06-Analytics-Reporting/traffic-analysis/` - Traffic data
- `02-Content/content-calendar/` - Content published
- `05-Link-Building/` - Link building data
