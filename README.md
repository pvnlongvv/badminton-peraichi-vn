# 🏸 Peraichi Badminton Cup 2026 — Luật chơi & Thể thức cầu lông đôi nam nữ

Trang web một-trang (single page) cho **Peraichi Badminton Cup 2026** — giải cầu lông đôi nam nữ **nội bộ của Peraichi Việt Nam**. Trang giới thiệu **luật chơi cầu lông đôi nam nữ** và **thể thức giải đấu**, viết bằng tiếng Việt, dành cho người mới chơi, kèm nhiều minh hoạ tương tác (demo giao cầu, xoay người, sơ đồ sân...) chạy hoàn toàn trên trình duyệt.

🔗 **Xem trực tiếp:** https://pvnlongvv.github.io/badminton-peraichi-vn/

---

## Nội dung trang

| Mục | Nội dung |
|-----|----------|
| **Hero + Số liệu** | Giới thiệu giải & các con số chính (7 đội, 2 bảng, 21 điểm/ván, Top 2 mỗi bảng). |
| **Thể thức & Lịch thi đấu** | Toàn bộ luật giải: chia bảng, lịch vòng bảng, xếp hạng, play-off, lịch trình ngày thi đấu. |
| **Chuẩn bị cơ bản** | Kích thước sân, đội hình, cách bắt đầu trận đấu. |
| **Tính điểm & Giao cầu** | Cách tính điểm + **demo giao cầu tương tác** và **demo xoay người 4 pha**. |
| **Luật khác** | Đổi sân, các lỗi thường gặp, thời gian nghỉ. |
| **Vùng giao cầu / IN-OUT / LET** | Minh hoạ trực quan cầu trong–ngoài sân, ô giao cầu hợp lệ, tình huống đánh lại. |
| **Tóm tắt nhanh** | 6 điều cốt lõi cần nhớ. |

## Thể thức giải đấu (Peraichi Badminton Cup 2026)

**7 đội**, mỗi đội 1 cặp nam–nữ, thi đấu qua **2 giai đoạn**:

### Giai đoạn 1 — Vòng bảng
- Chia **2 bảng**: **Bảng A** (4 đội) và **Bảng B** (3 đội).
- Mỗi bảng đấu **vòng tròn nội bộ**, 1 ván 21 điểm — thắng +2, thua 0 điểm.
- Tổng **9 trận** (Bảng A 6 trận, Bảng B 3 trận).
- **Top 2 mỗi bảng** (4 đội) giành vé vào play-off.

### Giai đoạn 2 — Play-off (ghép chéo, 3 ván 15 điểm)
- **Bán kết 1:** Nhất bảng A – Nhì bảng B
- **Bán kết 2:** Nhất bảng B – Nhì bảng A
- **Chung kết:** 2 đội thắng bán kết → tranh giải **Nhất – Nhì**
- **Tranh hạng Ba:** 2 đội thua bán kết → tranh giải **Ba – Khuyến khích**

> Tổng cộng 4 trận play-off, xác định đủ 4 giải thưởng.

## Công nghệ

- Một file **`index.html`** duy nhất — HTML + CSS + JavaScript thuần (vanilla), **không phụ thuộc framework**.
- Font: [M PLUS Rounded 1c](https://fonts.google.com/specimen/M+PLUS+Rounded+1c) & [Be Vietnam Pro](https://fonts.google.com/specimen/Be+Vietnam+Pro) (Google Fonts).
- Minh hoạ sân & chuyển động: **SVG** + animation bằng JavaScript.
- Giao diện **responsive**, tối ưu cho cả desktop và điện thoại.

## Chạy / xem trên máy

Vì là trang tĩnh nên chỉ cần mở file là được:

```bash
# Cách 1: mở trực tiếp
open index.html        # macOS
# xdg-open index.html  # Linux

# Cách 2: chạy server tĩnh (khuyến nghị để load font/chuẩn hơn)
python3 -m http.server 8000
# rồi mở http://localhost:8000
```

## Triển khai (Deploy)

Trang được host bằng **GitHub Pages** từ nhánh `main`. Mỗi lần push lên `main`, GitHub Pages tự động cập nhật tại:

```
https://pvnlongvv.github.io/badminton-peraichi-vn/
```

## SEO & chia sẻ mạng xã hội

Trang đã được tối ưu sẵn cho Google và link preview (Facebook / Zalo / LinkedIn / X):

- **Thẻ meta**: `description`, `keywords`, `canonical`, `robots`, `theme-color`.
- **Open Graph + Twitter Card**: tiêu đề, mô tả và ảnh `og-image.png` (1200×630) hiển thị khi dán link.
- **Structured data (JSON-LD)**: `WebSite`, `WebPage`, `FAQPage` — giúp Google hiểu nội dung & có cơ hội hiện rich result cho các câu hỏi luật cầu lông.
- **`robots.txt`** và **`sitemap.xml`** ở thư mục gốc.

### Tạo lại ảnh chia sẻ (`og-image.png`)

Ảnh được render từ `assets/og-card.html` bằng headless Chrome:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --hide-scrollbars \
  --force-device-scale-factor=1 --window-size=1200,630 \
  --virtual-time-budget=5000 \
  --screenshot="$PWD/og-image.png" \
  "file://$PWD/assets/og-card.html"
```

> Sau khi cập nhật ảnh, dùng [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) để "Scrape Again" cho Facebook tải lại ảnh mới.

## Cấu trúc thư mục

```
.
├── index.html          # Toàn bộ trang (HTML + CSS + JS) + thẻ SEO/OG
├── og-image.png        # Ảnh chia sẻ mạng xã hội (1200×630)
├── robots.txt          # Cho phép bot & trỏ tới sitemap
├── sitemap.xml         # Sitemap cho Google Search Console
├── assets/
│   └── og-card.html    # Nguồn để render og-image.png
└── README.md
```

---

*Phiên bản dành cho người mới chơi · 2026 · Chúc giải đấu thành công và fair-play! 🏸*
