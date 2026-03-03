---
name: keyword-research
description: Nghiên cứu và phân tích từ khóa cho một chủ đề hoặc ngành. Trả về danh sách từ khóa đã phân nhóm theo topic cluster và search intent.
argument-hint: [chủ-đề hoặc seed keyword]
user-invocable: true
allowed-tools: Read, Write, Glob, Grep, WebSearch, WebFetch
---

# Skill: Keyword Research

Nghiên cứu từ khóa cho chủ đề: **$ARGUMENTS**

## Quy trình thực hiện

### Bước 1: Thu thập Seed Keywords
- Lấy từ khóa gốc từ $ARGUMENTS
- Mở rộng bằng các biến thể: đồng nghĩa, long-tail, câu hỏi (ai, gì, ở đâu, như thế nào, bao nhiêu)
- Tìm related searches và People Also Ask

### Bước 2: Phân tích SERP
- Search từng keyword chính để hiểu SERP landscape
- Ghi nhận: loại content đang rank (blog, product, video, listicle)
- Xác định search features (featured snippet, PAA, local pack, ...)

### Bước 3: Phân nhóm Topic Cluster
Nhóm từ khóa theo cấu trúc:
```
Pillar Topic (keyword chính, volume cao)
├── Cluster 1 (subtopic)
│   ├── supporting keyword 1
│   └── supporting keyword 2
├── Cluster 2 (subtopic)
│   ├── supporting keyword 3
│   └── supporting keyword 4
└── Cluster 3 (subtopic)
```

### Bước 4: Xác định Search Intent
Phân loại mỗi keyword:
- **Informational** (I): "cách ...", "là gì", "hướng dẫn ..."
- **Commercial** (C): "tốt nhất", "so sánh", "review"
- **Transactional** (T): "mua", "giá", "đăng ký"
- **Navigational** (N): tên thương hiệu, trang cụ thể

### Bước 5: Đánh giá & Ưu tiên
Với mỗi keyword, đánh giá:
- Search Volume (ước lượng)
- Difficulty (Low/Medium/High)
- Business Relevance (1-5)
- Priority = Volume × Relevance / Difficulty

## Output format

Tạo file: `01-Keyword-Research/keyword-clusters/cluster_[date]_[topic-slug].md`

```markdown
# Keyword Research: [Topic]
**Ngày:** [date]
**Seed keyword:** [keyword]

## Tổng quan
- Tổng số keywords: [N]
- Clusters: [N]
- Estimated total volume: [N]

## Topic Clusters

### Cluster 1: [Tên cluster]
| Keyword | Volume | KD | Intent | Priority | Ghi chú |
|---------|--------|-----|--------|----------|---------|
| ...     | ...    | ... | ...    | ...      | ...     |

### Cluster 2: [Tên cluster]
...

## Recommendations
1. Quick wins (low KD, decent volume)
2. Long-term targets (high KD, high volume)
3. Content gaps vs competitors
```

## Tham khảo SOP
Xem thêm: @../../SOP/SEO/README.md
