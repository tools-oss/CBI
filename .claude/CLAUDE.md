# CBI - SEO Team Workspace

## Tổng quan dự án
Đây là workspace quản lý SEO và ecommerce cho team CBI, bao gồm keyword research, content management, technical SEO, link building, analytics reporting và ecommerce product research.

## Cấu trúc team (Agents)

| Agent | File | Vai trò | Khi nào dùng |
|-------|------|---------|-------------|
| `seo-leader` | `.claude/agents/seo-leader.md` | Quản lý chiến lược, điều phối team | Lập kế hoạch, review, ra quyết định |
| `technical-seo` | `.claude/agents/technical-seo.md` | SEO kỹ thuật | Audit, page speed, crawling, schema |
| `content-writer` | `.claude/agents/content-writer.md` | Viết & edit content | Viết bài, tạo brief, tối ưu nội dung |
| `seo-analyst` | `.claude/agents/seo-analyst.md` | Phân tích data | Keyword research, competitor analysis, báo cáo |
| `ecommerce-analyst` | `.claude/agents/ecommerce-analyst.md` | Nghiên cứu sản phẩm | Product research, niche analysis, profit calculation, supplier sourcing |

## Shared Skills (dùng chung)

| Skill | Lệnh | Mô tả |
|-------|-------|-------|
| Keyword Research | `/keyword-research [topic]` | Nghiên cứu và phân nhóm từ khóa |
| Content Brief | `/content-brief [keyword]` | Tạo brief cho writer |
| On-Page Audit | `/on-page-audit [URL/file]` | Kiểm tra on-page SEO |
| Technical Audit | `/technical-audit [URL]` | Audit kỹ thuật website |
| Competitor Analysis | `/competitor-analysis [domain]` | Phân tích đối thủ |
| Reporting | `/reporting [weekly/monthly] [date]` | Tạo báo cáo SEO |
| Content Review | `/content-review [file]` | Review chất lượng content |
| Product Research | `/product-research [sản phẩm/niche]` | Nghiên cứu sản phẩm ecommerce, phân tích niche, tính lợi nhuận, gợi ý supplier |

## Quy ước chung

### Đặt tên file
- Luôn dùng format: `type_YYYY-MM-DD_slug.md`
- Slug viết thường, dùng hyphens, không dấu

### Ngôn ngữ
- Tài liệu nội bộ: Tiếng Việt
- Tên file, thư mục: Tiếng Anh
- Code/technical terms: Giữ nguyên tiếng Anh

### Workflow chuẩn
1. SEO Analyst nghiên cứu từ khóa -> `01-Keyword-Research/`
2. Content Writer tạo brief -> `02-Content/briefs/`
3. Content Writer viết bài -> `02-Content/drafts/`
4. Review qua `/content-review` -> feedback
5. Tối ưu on-page qua `/on-page-audit`
6. Publish -> `02-Content/published/`
7. Technical SEO kiểm tra kỹ thuật
8. SEO Analyst theo dõi & báo cáo -> `06-Analytics-Reporting/`
9. Ecommerce Analyst nghiên cứu sản phẩm & niche -> `09-Ecommerce/`

### Tham khảo SOP
- SEO: @../SOP/SEO/README.md
- Content: @../SOP/Content/README.md
- Technical: @../SOP/Technical/README.md
- Ecommerce: @../SOP/Ecommerce/README.md
