# 02 - Content

Thư mục quản lý toàn bộ vòng đời nội dung: từ brief -> draft -> publish.

## Cấu trúc

| Thư mục | Mô tả | Người phụ trách |
|---------|-------|----------------|
| `briefs/` | Content brief cho writer | Content Editor / SEO Lead |
| `drafts/` | Bản nháp đang viết/review | Content Writer |
| `published/` | Bài đã xuất bản (lưu trữ) | Content Editor |
| `content-calendar/` | Lịch đăng bài hàng tháng | Content Editor / SEO Lead |
| `templates/` | Mẫu brief, outline, checklist | SEO Lead |

## Workflow

```
Brief tạo bởi Editor  -->  Writer nhận brief & viết draft
       |                            |
       v                            v
  briefs/                    drafts/ (v1, v2, ...)
                                     |
                                     v
                            Editor review & approve
                                     |
                                     v
                              published/
                                     |
                                     v
                        Cập nhật content-calendar/
```

## Quy ước đặt tên file
- Brief: `brief_YYYY-MM-DD_[keyword-slug].md`
- Draft: `draft_v[N]_YYYY-MM-DD_[keyword-slug].md`
- Published: `pub_YYYY-MM-DD_[keyword-slug].md`
- Calendar: `calendar_YYYY-MM.csv`
