# 🏸 Luật chơi cầu lông đôi nam nữ — Hướng dẫn cho người mới

Trang web một-trang (single page) giới thiệu **luật chơi cầu lông đôi nam nữ** và **thể thức giải đấu**, viết bằng tiếng Việt, dành cho người mới chơi. Trang có nhiều minh hoạ tương tác (demo giao cầu, xoay người, sơ đồ sân...) chạy hoàn toàn trên trình duyệt.

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

## Thể thức giải đấu

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

## Cấu trúc thư mục

```
.
├── index.html   # Toàn bộ trang (HTML + CSS + JS)
└── README.md
```

---

*Phiên bản dành cho người mới chơi · 2026 · Chúc giải đấu thành công và fair-play! 🏸*
