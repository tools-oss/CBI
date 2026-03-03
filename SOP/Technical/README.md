# SOP - Quy trình Technical SEO

## 1. Site Audit
- Chạy crawl toàn site bằng Screaming Frog (hàng tháng)
- Export và lưu report vào `04-Technical-SEO/site-audit/`
- Phân loại lỗi theo mức độ ưu tiên: Critical > High > Medium > Low
- Tạo action plan fix lỗi

## 2. Core Web Vitals
- Kiểm tra CWV hàng tuần qua PageSpeed Insights / CrUX
- Lưu metrics vào `04-Technical-SEO/core-web-vitals/`
- Target: LCP < 2.5s, FID < 100ms, CLS < 0.1

## 3. Sitemap & Robots.txt
- Tự động generate sitemap khi có bài mới
- Review robots.txt mỗi quý
- Đảm bảo không block resource quan trọng

## 4. Page Speed Optimization
- Compress images (WebP, AVIF)
- Minify CSS/JS
- Implement lazy loading
- Sử dụng CDN
- Cache policy hợp lý

## 5. Structured Data
- Implement schema phù hợp cho từng content type
- Validate bằng Google Rich Results Test
- Theo dõi rich snippets trong GSC
