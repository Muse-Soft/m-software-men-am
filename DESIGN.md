# DESIGN.md — Landing page tiệm bánh thủ công Men Ấm

- Sản phẩm: landing page visual-first cho tiệm bánh thủ công Men Ấm (sourdough + bánh ngọt kiểu Pháp).
- Repo: Muse-Soft/m-software-men-am — Project Linear: m-software-men-am — Epic: TEC-176 — Task thiết kế: TEC-177.
- Nguyên tắc: ảnh là nội dung chính; mọi quyết định dưới đây là DỨT KHOÁT, Dev làm đúng thông số, không diễn giải lại thành "đẹp, hiện đại" chung chung.
- Dữ liệu thật chưa có thì để `[CẦN BỔ SUNG]` — không bịa địa chỉ, số điện thoại hay giá thật.

## 1. Bảng màu (mã hex + vai trò từng màu)

| Màu | Mã hex | Vai trò |
| --- | --- | --- |
| Nền kem bơ | `#FAF5EC` | Nền chính toàn trang |
| Chữ nâu sẫm | `#2E211A` | Chữ tiêu đề và chữ nội dung chính |
| Nhấn caramel | `#B07D3C` | Nút chính, link, giá, điểm nhấn, gạch chân tiêu đề mục |
| Nền thẻ | `#FFFDF8` | Nền thẻ sản phẩm, thẻ "Ra lò hôm nay", nền form đặt bánh |
| Chữ phụ | `#7A5C43` | Chữ mô tả phụ, chú thích ảnh, ngày/giờ ra lò |
| Viền | `#E8DCC8` | Viền thẻ, đường phân tách giữa các mục |
| Nền tối chân trang | `#2E211A` | Nền chân trang (footer), chữ trên nền này dùng `#FAF5EC` |
| Nền nhấn nhạt | `#F3E8D3` | Nền khối nổi bật (ví dụ: khối "Ra lò hôm nay", khối giới thiệu lò bánh) |

Quy tắc dùng màu:
- Tỉ lệ dùng màu trên một màn hình: nền kem bơ chiếm đa số, chữ nâu sẫm cho mọi tiêu đề, caramel CHỈ dùng cho nút/link/điểm nhấn — không dùng caramel làm nền diện rộng.
- Nút chính: nền `#B07D3C`, chữ `#FFFDF8`. Nút phụ: viền `#B07D3C`, chữ `#B07D3C`, nền trong suốt.
- Không dùng thêm màu ngoài bảng trên nếu không sửa DESIGN.md này trước.

## 2. Font chữ (cụ thể, kèm subset tiếng Việt)

- Font tiêu đề: **Fraunces** (Google Fonts), weight 600 cho tiêu đề lớn (hero, tên mục), weight 500 cho tiêu đề thẻ; fallback: `Georgia, serif`.
- Font nội dung: **Be Vietnam Pro** (Google Fonts), weight 400 cho nội dung thường, 500 cho chữ đậm vừa, 700 cho nút và nhãn; fallback: `system-ui, sans-serif`.
- Cả hai font đều phải nạp kèm subset tiếng Việt (`vietnamese`) để dấu tiếng Việt hiển thị đúng — Dev kiểm tra tiêu đề "Men Ấm — Bánh thủ công" và các từ có dấu (ổ, ừ, ơ, đ) trước khi coi là đạt.
- Cỡ chữ: hero 56px desktop / 36px mobile; tiêu đề mục 36px desktop / 28px mobile; tiêu đề thẻ 20px; nội dung 16px; chú thích 14px. Dãn dòng nội dung 1.6.

## 3. Phong cách tham chiếu (MỘT phong cách, tên gọi rõ)

**Tiệm bánh châu Âu ấm áp, editorial kiểu tạp chí ẩm thực.**

Giải thích cụ thể phong cách này nghĩa là gì trong trang này:
- Bố cục như một trang tạp chí ẩm thực: ảnh lớn chiếm ưu thế, tiêu đề Fraunces serif cỡ lớn đặt chồng hoặc kề ảnh, khoảng trắng rộng giữa các mục (tối thiểu 80px desktop, 48px mobile).
- Tông ảnh ấm vàng, ánh sáng tự nhiên (xem mục 4) — không dùng ảnh nền trắng studio lạnh, không dùng icon stock trang trí.
- Không dùng template lưới sản phẩm thương mại điện tử dày đặc; mỗi sản phẩm có một ảnh lớn và một dòng mô tả ngắn, không liệt kê thông số kỹ thuật dài.

## 4. Quy tắc hình ảnh

- Ảnh là nội dung chính: mỗi mục phải có ít nhất một ảnh bánh lớn, không dùng khối chữ không ảnh làm mục chính.
- Đồng tông: mọi ảnh đồng tông ấm vàng (ánh vàng kem bơ, nâu caramel), ánh sáng tự nhiên (ánh sáng ban ngày qua cửa sổ, bóng mềm) — ảnh lệch tông lạnh/xanh hoặc tối gắt là lệch DESIGN.md.
- Hero: ảnh bánh toàn màn hình — tỉ lệ khung 16:9 trên desktop, ảnh phủ toàn bộ chiều rộng màn hình, chiều cao tối thiểu 90vh; tiêu đề "Men Ấm" đặt trên ảnh kèm lớp phủ tối nhẹ để chữ đọc được; mobile dùng ảnh dọc 4:5 phủ toàn màn hình.
- Lưới ảnh "Ra lò hôm nay": mỗi ảnh tỉ lệ lớn — 4:3 trên desktop, 3:2 trên mobile; mỗi mẻ bánh một ảnh lớn kèm tên bánh + giờ ra lò (giờ thật là `[CẦN BỔ SUNG]` nếu chưa có).
- Thực đơn 3 nhóm (sourdough, bánh ngọt kiểu Pháp, bánh theo mùa): mỗi nhóm một ảnh đại diện tỉ lệ 4:3, ảnh các món trong nhóm tỉ lệ 1:1.
- Ảnh mẫu ở bản đầu tiên phải là ảnh mẫu chất lượng cao, đồng tông ấm vàng, đúng tỉ lệ khung trên; ghi rõ là ảnh mẫu trong ghi chú bàn giao, không ghi là ảnh thật của tiệm.
- Ảnh chưa có bản quyền rõ thì không dùng; ảnh mẫu dùng nguồn có khai báo (ghi nguồn trong README hoặc chú thích).

## 5. Bố cục các mục (thứ tự cố định)

1. Hero toàn màn hình (ảnh bánh + tên "Men Ấm" + câu giới thiệu ngắn + nút "Xem thực đơn").
2. Giới thiệu lò bánh (1 ảnh lớn + 1 đoạn ngắn, tối đa 3 câu).
3. Thực đơn 3 nhóm: sourdough, bánh ngọt kiểu Pháp, bánh theo mùa (mỗi nhóm ảnh đại diện + tên món + mô tả 1 dòng; giá là `[CẦN BỔ SUNG]`).
4. Khối "Ra lò hôm nay" (lưới ảnh lớn theo mục 4 + giờ ra lò).
5. Form đặt bánh — CHỈ giao diện (4 trường: tên, số điện thoại, loại bánh, ngày nhận); form chưa gửi đi thật, ghi rõ "bản demo — chưa gửi đơn thật" ngay dưới nút gửi.
6. Liên hệ & chân trang: địa chỉ, số điện thoại, giờ mở cửa đều là `[CẦN BỔ SUNG]` cho đến khi có dữ liệu thật.

## 6. Ghi chú bàn giao cho Dev (TEC-178)

- Làm đúng bảng màu mục 1, font mục 2, phong cách mục 3, tỉ lệ ảnh mục 4 — lệch màu/font chủ đạo, vỡ bố cục hoặc ảnh lệch tông là lỗi cần sửa.
- Dữ liệu thật (địa chỉ, điện thoại, giá, giờ ra lò) giữ `[CẦN BỔ SUNG]`, không tự bịa.
