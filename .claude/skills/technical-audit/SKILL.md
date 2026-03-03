---
name: technical-audit
description: Audit kỹ thuật SEO cho website. Kiểm tra crawlability, indexing, page speed, Core Web Vitals, structured data và các vấn đề kỹ thuật khác.
argument-hint: [URL website hoặc phạm vi audit]
user-invocable: true
allowed-tools: Read, Write, Bash, Glob, Grep, WebFetch
---

# Skill: Technical SEO Audit

Thực hiện technical audit cho: **$ARGUMENTS**

## Checklist Audit

### 1. Crawlability
- Robots.txt configuration
- Sitemap.xml status
- Crawl errors / blocked resources
- Redirect chains (max 1 redirect)
- Orphan pages

### 2. Indexing
- Index coverage
- Canonical tags
- Noindex/nofollow usage
- Duplicate content issues

### 3. Page Speed & Core Web Vitals
- LCP (target < 2.5s)
- INP (target < 200ms)
- CLS (target < 0.1)
- TTFB (target < 800ms)
- Total page size
- Number of requests

### 4. Mobile
- Mobile-friendly
- Viewport configuration
- Touch elements spacing
- Font sizes readable

### 5. Security
- HTTPS configuration
- Mixed content
- Security headers

### 6. Structured Data
- Schema types implemented
- Validation errors
- Rich results eligibility

## Output

Tạo file: `04-Technical-SEO/site-audit/audit_[date]_[domain].md`

```markdown
# Technical SEO Audit: [Domain]
**Ngày:** [date]
**Phạm vi:** [scope]

## Executive Summary
[2-3 câu tóm tắt tình trạng]

## Critical Issues (fix ngay)
1. ...

## High Priority
1. ...

## Medium Priority
1. ...

## Low Priority
1. ...

## Action Plan
| # | Issue | Fix | Priority | Effort | Owner |
|---|-------|-----|----------|--------|-------|
| 1 | ...   | ... | ...      | ...    | ...   |
```

## Tham khảo SOP
Xem thêm: @../../SOP/Technical/README.md
