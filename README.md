# CBI - SEO Team Workspace

## Cấu trúc thư mục

```
CBI/
├── SOP/                          # Quy trình chuẩn (Standard Operating Procedures)
│   ├── SEO/                      # SOP cho quy trình SEO
│   ├── Content/                  # SOP cho quy trình viết content
│   └── Technical/                # SOP cho kỹ thuật
│
├── 01-Keyword-Research/          # Nghiên cứu từ khóa
│   ├── seed-keywords/            # Danh sách từ khóa gốc
│   ├── keyword-clusters/         # Nhóm từ khóa theo chủ đề
│   ├── competitor-analysis/      # Phân tích từ khóa đối thủ
│   └── search-intent-mapping/    # Phân loại intent (informational, transactional, ...)
│
├── 02-Content/                   # Quản lý nội dung
│   ├── briefs/                   # Content brief cho writer
│   ├── drafts/                   # Bản nháp đang viết
│   ├── published/                # Bài đã xuất bản
│   ├── content-calendar/         # Lịch đăng bài
│   └── templates/                # Mẫu content brief, outline
│
├── 03-On-Page-SEO/               # Tối ưu On-Page
│   ├── title-meta-tags/          # Title tag & meta description
│   ├── heading-structure/        # Cấu trúc H1-H6
│   ├── internal-linking/         # Chiến lược internal link
│   ├── schema-markup/            # Structured data / Schema
│   └── image-optimization/       # Alt text, lazy load, WebP
│
├── 04-Technical-SEO/             # SEO kỹ thuật
│   ├── site-audit/               # Báo cáo audit tổng thể
│   ├── crawl-reports/            # Báo cáo crawl (Screaming Frog, ...)
│   ├── sitemap/                  # File sitemap.xml
│   ├── robots-txt/               # Cấu hình robots.txt
│   ├── page-speed/               # Tối ưu tốc độ trang
│   └── core-web-vitals/          # LCP, FID, CLS metrics
│
├── 05-Link-Building/             # Xây dựng backlink
│   ├── backlink-audit/           # Kiểm tra backlink hiện tại
│   ├── outreach-templates/       # Mẫu email outreach
│   ├── guest-post-tracking/      # Theo dõi guest post
│   └── disavow-list/             # Danh sách link cần disavow
│
├── 06-Analytics-Reporting/       # Phân tích & Báo cáo
│   ├── weekly-reports/           # Báo cáo tuần
│   ├── monthly-reports/          # Báo cáo tháng
│   ├── ranking-tracking/         # Theo dõi thứ hạng từ khóa
│   ├── traffic-analysis/         # Phân tích traffic
│   └── conversion-tracking/      # Theo dõi chuyển đổi
│
├── 07-Local-SEO/                 # SEO địa phương
│   ├── google-business-profile/  # Google Business Profile
│   ├── local-citations/          # NAP citations
│   └── reviews-management/       # Quản lý đánh giá
│
└── 08-Tools-Config/              # Cấu hình công cụ
    ├── google-search-console/    # GSC settings & reports
    ├── google-analytics/         # GA4 config
    ├── ahrefs-semrush/           # Config & exported data
    └── screaming-frog/           # Crawl config profiles
```

## Vai trò trong team

| Vai trò | Thư mục chính | Mô tả |
|---------|--------------|-------|
| SEO Lead | Tất cả | Quản lý chiến lược SEO tổng thể |
| Content Writer | `02-Content/` | Viết bài theo brief, tuân thủ SOP |
| Content Editor | `02-Content/`, `03-On-Page-SEO/` | Review, chỉnh sửa, tối ưu on-page |
| Technical SEO | `04-Technical-SEO/`, `08-Tools-Config/` | Xử lý kỹ thuật, audit, tốc độ |
| Link Builder | `05-Link-Building/` | Outreach, guest post, backlink |
| SEO Analyst | `06-Analytics-Reporting/`, `01-Keyword-Research/` | Phân tích data, báo cáo |

## Quy trình làm việc

1. **Keyword Research** -> Nghiên cứu từ khóa, phân nhóm, xác định intent
2. **Content Brief** -> Tạo brief dựa trên keyword research
3. **Content Creation** -> Writer viết bài theo brief
4. **On-Page Optimization** -> Tối ưu title, meta, heading, schema
5. **Publishing** -> Xuất bản và cập nhật content calendar
6. **Link Building** -> Outreach để xây dựng backlink
7. **Monitoring** -> Theo dõi ranking, traffic, conversion
8. **Reporting** -> Báo cáo tuần/tháng và điều chỉnh chiến lược
