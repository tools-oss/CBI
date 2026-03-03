# SOP - Quy trình Ecommerce & Dropship

## 1. Quy trình nghiên cứu sản phẩm (Product Research)
- Xác định ngành hàng/niche muốn nghiên cứu
- Thu thập dữ liệu sản phẩm trending trên các marketplace: Shopee, Tiki, Amazon, AliExpress
- Phân tích số liệu bán hàng: lượt bán, đánh giá, rating
- Lọc sản phẩm theo tiêu chí: lượt bán > 100/tháng, rating >= 4.0, số lượng shop bán < 50
- Đánh giá mức độ cạnh tranh trên từng marketplace
- Tính lợi nhuận dự kiến cho từng sản phẩm tiềm năng
- Xếp hạng sản phẩm theo điểm tiềm năng (Potential Score)

## 2. Tiêu chí đánh giá Niche
Mỗi niche được đánh giá theo 5 tiêu chí (thang điểm 1-5):

| Tiêu chí | Mô tả | Trọng số |
|----------|-------|---------|
| Demand (Nhu cầu) | Search volume, lượt bán trên marketplace | 25% |
| Competition (Cạnh tranh) | Số lượng shop, mức độ bão hòa | 25% |
| Profit Margin (Biên lợi nhuận) | Chênh lệch giá mua - bán - phí | 20% |
| Trending (Xu hướng) | Tăng trưởng theo thời gian | 15% |
| Logistics (Vận chuyển) | Dễ đóng gói, nhẹ, ít hư hỏng | 15% |

**Công thức Niche Score:**
Niche Score = (Demand x 0.25) + ((6 - Competition) x 0.25) + (Margin x 0.20) + (Trending x 0.15) + (Logistics x 0.15)

**Thang đánh giá:**
- 4.0 - 5.0: Niche tuyệt vời, nên tham gia ngay
- 3.0 - 3.9: Niche tốt, cần nghiên cứu thêm
- 2.0 - 2.9: Niche trung bình, rủi ro cao
- < 2.0: Không nên tham gia

## 3. Quy trình tính lợi nhuận (Profit Margin Calculation)

### Công thức cơ bản
```
Lợi nhuận = Giá bán - Giá nhập - Chi phí vận chuyển - Phí sàn - Phí khác
Biên lợi nhuận (%) = (Lợi nhuận / Giá bán) x 100
```

### Chi tiết chi phí
| Khoản mục | Mô tả | Cách tính |
|-----------|-------|-----------|
| Giá nhập (COGS) | Giá mua từ supplier (AliExpress, 1688, nhà cung cấp VN) | Giá sản phẩm + phí ship về kho |
| Giá bán (Selling Price) | Giá niêm yết trên marketplace | Tham khảo giá trung bình top 10 shop |
| Phí vận chuyển (Shipping) | Ship tới khách hàng | Tương ứng với đơn vị vận chuyển |
| Phí sàn (Platform Fee) | Shopee: 6.5%, Tiki: 5-10%, Amazon: 8-15% | Theo % giá bán |
| Phí marketing | Quảng cáo, khuyến mãi | Ước tính 5-10% giá bán |
| Phí khác | Đóng gói, nhãn mác, trả hàng | Ước tính 3-5% giá bán |

### Ngưỡng chấp nhận
- Dropship nội địa (Shopee, Tiki): Biên lợi nhuận >= 20%
- Dropship quốc tế (AliExpress -> VN): Biên lợi nhuận >= 30%
- Private label: Biên lợi nhuận >= 40%

## 4. Quy trình vet Supplier (Nhà cung cấp)
1. Tìm supplier trên các nguồn: AliExpress, 1688.com, Alibaba, nhà cung cấp nội địa
2. Đánh giá supplier theo tiêu chí:
   - Thời gian hoạt động: >= 2 năm
   - Rating: >= 4.5/5
   - Tốc độ phản hồi: < 24h
   - MOQ (Số lượng đặt tối thiểu): phù hợp với nhu cầu
   - Mẫu sản phẩm: có thể gửi mẫu trước
   - Chính sách trả hàng: rõ ràng
3. Đặt hàng mẫu (sample order) trước khi hợp tác chính thức
4. Đánh giá chất lượng sản phẩm mẫu
5. Thương lượng giá và điều khoản hợp tác
6. Lưu thông tin vào `09-Ecommerce/supplier-list/`

## 5. Workflow Dropship tổng thể
1. **Nghiên cứu niche** -> Ecommerce Analyst đánh giá niche -> `09-Ecommerce/niche-analysis/`
2. **Tìm sản phẩm** -> Research trending products -> `09-Ecommerce/trending-products/`
3. **Phân tích sản phẩm** -> Product research chi tiết -> `09-Ecommerce/product-research/`
4. **Tính lợi nhuận** -> Profit calculator -> `09-Ecommerce/profit-calculator/`
5. **Tìm supplier** -> Vet và chọn supplier -> `09-Ecommerce/supplier-list/`
6. **Tạo listing** -> Content Writer viết mô tả sản phẩm (phối hợp với SEO)
7. **Tối ưu SEO** -> SEO Analyst nghiên cứu keyword sản phẩm -> `01-Keyword-Research/`
8. **Theo dõi** -> Báo cáo hiệu quả bán hàng -> `06-Analytics-Reporting/`

## 6. Tần suất thực hiện
- Scan trending products: Hàng tuần
- Niche evaluation: Hàng tháng hoặc khi có niche mới
- Supplier review: Hàng quý
- Profit margin re-calculation: Khi giá nhập/bán thay đổi
