---
name: product-research
description: Nghiên cứu sản phẩm ecommerce/dropship. Phân tích trending products trên marketplace, đánh giá cạnh tranh, tính lợi nhuận, đánh giá niche và gợi ý nhà cung cấp.
argument-hint: [tên sản phẩm, niche, hoặc danh mục]
user-invocable: true
allowed-tools: Read, Write, Glob, Grep, WebSearch, WebFetch
---

# Skill: Product Research

Nghiên cứu sản phẩm ecommerce cho: **$ARGUMENTS**

## Quy trình thực hiện

### Bước 1: Tìm sản phẩm trending
- Search "$ARGUMENTS" trên các marketplace: Shopee, Tiki, Amazon, AliExpress
- Thu thập thông tin cho mỗi sản phẩm:
  - Tên sản phẩm, danh mục
  - Giá bán (min / trung bình / max)
  - Lượt bán ước tính/tháng
  - Số lượng đánh giá và rating trung bình
  - Số lượng shop đang bán sản phẩm tương tự
- Lọc sản phẩm: lượt bán >= 100/tháng, rating >= 4.0, số shop < 50

### Bước 2: Phân tích cạnh tranh
Với top 10-15 sản phẩm lọc được:
- Số lượng shop cạnh tranh trên từng marketplace
- Range giá bán (giá thấp nhất, trung bình, cao nhất)
- Top 3 shop bán chạy nhất: điểm mạnh, chiến lược giá, số lượt bán
- Mức độ bão hòa thị trường (thấp/trung bình/cao)
- Rào cản gia nhập (vốn, kiến thức, logistics)

### Bước 3: Tính lợi nhuận
Với từng sản phẩm tiềm năng:

| Khoản mục | Cách tính |
|-----------|-----------|
| Giá bán (Selling Price) | Giá trung bình top 10 shop |
| Giá nhập (COGS) | Tìm giá trên AliExpress/1688/Alibaba |
| Phí ship về kho | Từ supplier đến kho/nhà bán |
| Phí ship đến KH | Theo đơn vị vận chuyển nội địa |
| Phí sàn (Platform Fee) | Shopee 6.5%, Tiki 5-10%, Amazon 8-15% |
| Phí marketing | Ước tính 5-10% giá bán |
| Phí khác | Đóng gói, nhãn mác, trả hàng: 3-5% |

**Công thức:**
```
Lợi nhuận = Giá bán - COGS - Ship kho - Ship KH - Phí sàn - Marketing - Phí khác
Margin (%) = (Lợi nhuận / Giá bán) x 100
```

**Ngưỡng chấp nhận:** Dropship nội địa >= 20%, Quốc tế >= 30%, Private label >= 40%

### Bước 4: Đánh giá Niche
Đánh giá tổng thể niche "$ARGUMENTS" theo 5 tiêu chí (1-5):
- **Demand (25%):** Search volume + lượt bán trên marketplace
- **Competition (25%):** Số lượng đối thủ, mức độ bão hòa
- **Profit Margin (20%):** Biên lợi nhuận trung bình của niche
- **Trending (15%):** Xu hướng tăng/giảm theo thời gian
- **Logistics (15%):** Độ khó vận chuyển, đóng gói, tỷ lệ hư hỏng

**Niche Score** = (Demand x 0.25) + ((6 - Competition) x 0.25) + (Margin x 0.20) + (Trending x 0.15) + (Logistics x 0.15)

### Bước 5: Gợi ý Supplier
Tìm 3-5 supplier cho các sản phẩm tiềm năng nhất:
- Search trên AliExpress, 1688.com, Alibaba
- Tìm nhà cung cấp nội địa (nếu có)
- Đánh giá: thời gian hoạt động, rating, MOQ, tốc độ phản hồi, chính sách trả hàng
- Sắp xếp theo độ tin cậy và giá cả

## Output format

Tạo file: `09-Ecommerce/product-research/product_[date]_[slug].md`

```markdown
# Product Research: [Tên sản phẩm / Niche]
**Ngày:** [date]
**Niche/Danh mục:** [danh mục]
**Người thực hiện:** Product Research Skill

## 1. Tổng quan thị trường
- Quy mô thị trường ước tính: [mô tả]
- Xu hướng: [tăng/giảm/ổn định]
- Mức độ cạnh tranh: [thấp/trung bình/cao]

## 2. Sản phẩm trending

| # | Sản phẩm | Marketplace | Giá bán (VND) | Lượt bán/tháng | Rating | Số shop | Potential Score |
|---|----------|-------------|---------------|---------------|--------|---------|-----------------|
| 1 | ...      | ...         | ...           | ...           | ...    | ...     | .../5           |
| 2 | ...      | ...         | ...           | ...           | ...    | ...     | .../5           |

## 3. Phân tích cạnh tranh chi tiết

### Sản phẩm 1: [Tên]
- **Số shop cạnh tranh:** [N]
- **Range giá:** [min] - [max] VND
- **Top seller:** [tên shop] - [lượt bán/tháng]
- **Mức độ bão hòa:** [thấp/trung bình/cao]
- **Rào cản gia nhập:** [mô tả]

### Sản phẩm 2: [Tên]
...

## 4. Phân tích lợi nhuận

### Sản phẩm 1: [Tên]
| Khoản mục | Số tiền (VND) | Ghi chú |
|-----------|--------------|---------|
| Giá bán | ... | Giá TB marketplace |
| Giá nhập (COGS) | -... | Supplier: [tên] |
| Phí ship về kho | -... | |
| Phí ship tới KH | -... | |
| Phí sàn (X%) | -... | [Marketplace] |
| Phí marketing (X%) | -... | |
| Phí khác (X%) | -... | |
| **Lợi nhuận** | **...** | |
| **Biên lợi nhuận** | **X%** | [Đạt/Không đạt ngưỡng] |

### Sản phẩm 2: [Tên]
...

## 5. Đánh giá Niche

**Niche Score: [X.X/5.0]** - [Tuyệt vời / Tốt / Trung bình / Không nên tham gia]

| Tiêu chí | Điểm (1-5) | Trọng số | Điểm x Trọng số | Ghi chú |
|----------|-----------|---------|----------------|---------|
| Demand | ... | 25% | ... | ... |
| Competition | ... | 25% | ... | ... |
| Profit Margin | ... | 20% | ... | ... |
| Trending | ... | 15% | ... | ... |
| Logistics | ... | 15% | ... | ... |
| **Tổng** | | | **[X.X]** | |

## 6. Gợi ý Supplier

| # | Supplier | Platform | Rating | MOQ | Giá (VND) | Ship time | Đánh giá |
|---|----------|----------|--------|-----|-----------|-----------|----------|
| 1 | ...      | ...      | ...    | ... | ...       | ...       | ...      |

### Chi tiết supplier tốt nhất
- **Tên:** [tên]
- **Platform:** [AliExpress / 1688 / Nội địa]
- **URL:** [link]
- **Rating:** [X/5]
- **Thời gian hoạt động:** [N năm]
- **MOQ:** [số lượng]
- **Thời gian ship:** [N ngày]
- **Chính sách trả hàng:** [mô tả]

## 7. Kết luận & Khuyến nghị
1. **Top sản phẩm nên bán:** [danh sách]
2. **Supplier ưu tiên:** [tên]
3. **Bước tiếp theo:** [action items]
4. **Rủi ro cần lưu ý:** [danh sách]
```

## Tham khảo SOP
Xem thêm: @../../SOP/Ecommerce/README.md
