---
name: competitor-analysis
description: Phân tích chiến lược SEO của đối thủ cạnh tranh. Bao gồm keyword gaps, content strategy, backlink profile và opportunities.
argument-hint: [URL đối thủ hoặc tên đối thủ]
user-invocable: true
allowed-tools: Read, Write, Glob, Grep, WebSearch, WebFetch
---

# Skill: Competitor Analysis

Phân tích đối thủ: **$ARGUMENTS**

## Quy trình phân tích

### 1. Overview
- Domain authority / Domain rating
- Estimated organic traffic
- Total keywords ranking
- Top pages by traffic

### 2. Keyword Analysis
- Top keywords đối thủ đang rank
- Keywords đối thủ rank top 3
- Keywords đối thủ có mà mình chưa có (content gaps)
- Keyword overlap giữa mình và đối thủ

### 3. Content Strategy
- Tần suất đăng bài
- Content types (blog, guide, tool, ...)
- Average word count
- Topics chính
- Content quality assessment

### 4. Backlink Profile
- Tổng số referring domains
- Top referring domains
- Link types (editorial, guest post, directory, ...)
- Anchor text distribution

### 5. Technical
- Site speed
- Mobile experience
- Structured data usage
- Site architecture

## Output

Tạo file: `01-Keyword-Research/competitor-analysis/competitor_[date]_[name].md`

```markdown
# Competitor Analysis: [Tên đối thủ]
**URL:** [domain]
**Ngày phân tích:** [date]

## Overview
| Metric | Đối thủ | Mình | Gap |
|--------|---------|------|-----|
| DA/DR  | ...     | ...  | ... |
| Traffic| ...     | ...  | ... |
| Keywords| ...    | ...  | ... |

## Keyword Gaps (Opportunities)
| Keyword | Đối thủ Rank | Volume | KD | Priority |
|---------|-------------|--------|-----|----------|
| ...     | ...         | ...    | ... | ...      |

## Content Insights
[Phân tích chiến lược content]

## Actionable Takeaways
1. [Action cụ thể mình có thể làm]
2. ...
```
