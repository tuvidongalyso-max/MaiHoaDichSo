# Mai Hoa Dịch Số – Huyền Học Đông A

Ứng dụng web lập quẻ **Mai Hoa Dịch Số** và **Lục Hào**, có luận giải chi tiết theo từng loại việc cần hỏi, xuất kết quả ra PDF.
Chạy hoàn toàn trên trình duyệt, **không cần máy chủ, không cần cài đặt**; toàn bộ ứng dụng nằm trong một file `index.html`.

![Giao diện](docs/screenshot.png)

## Tính năng

- **4 cách lập quẻ:** theo thời gian (tự đổi sang âm lịch), theo số, theo sự vật, và Lục Hào (gieo ba đồng xu hoặc nhập tay sáu số 6/7/8/9).
- **14 loại việc cần hỏi (bắt buộc chọn):** cầu tài, công danh, hôn nhân, sức khỏe, thi cử, kiện tụng, xuất hành, tìm đồ, cầu con, tìm người, phỏng vấn, nhà cửa – đất đai, mộ phần – âm trạch, lo lắng – nghi hoặc.
- **Mai Hoa:** quẻ chính, quẻ hỗ, quẻ biến, hào động, Thể – Dụng, ngũ hành sinh khắc, vượng suy theo mùa, vạn vật loại tượng, ứng kỳ, báo cáo luận giải nhiều mục kèm dự đoán cụ thể.
- **Lục Hào:** nạp giáp, lục thân, lục thú, Thế – Ứng, nguyệt kiến theo tiết khí, tuần không, nguyệt phá, Dụng thần, Nguyên – Kỵ – Cừu thần, hào động biến, ứng kỳ và lời giải.
- **Xuất PDF** khổ A4 (tạo ngay trong trình duyệt).
- Giao diện xanh biển – vàng kim, tối ưu cho điện thoại, tự đổi sáng/tối theo thiết bị, có hiệu ứng nền (rồng, phượng, bát quái).

## Chạy thử trên máy

Cách đơn giản nhất: mở file `index.html` bằng trình duyệt (nhấp đúp).

Hoặc chạy bằng một máy chủ tĩnh bất kỳ, ví dụ:

```bash
python3 -m http.server 8080
# rồi mở http://localhost:8080
```

## Đưa lên GitHub và bật GitHub Pages

1. Tạo repository mới trên GitHub (ví dụ `mai-hoa-dich-so`).
2. Đưa toàn bộ nội dung thư mục này lên (giữ `index.html` ở thư mục gốc):
   ```bash
   git init
   git add .
   git commit -m "Mai Hoa Dich So - ban dau"
   git branch -M main
   git remote add origin https://github.com/<ten-ban>/mai-hoa-dich-so.git
   git push -u origin main
   ```
3. Vào **Settings → Pages**, mục *Build and deployment* chọn **Deploy from a branch**, nhánh `main`, thư mục `/ (root)`, bấm **Save**.
4. Sau khoảng 1–2 phút, trang chạy tại `https://<ten-ban>.github.io/mai-hoa-dich-so/`.

## Cấu trúc

```
index.html        Toàn bộ ứng dụng (HTML, CSS, JavaScript, hình nền nhúng sẵn)
docs/screenshot.png   Ảnh minh họa cho README
.nojekyll         Báo GitHub Pages phục vụ file nguyên trạng
```

## Lưu ý kỹ thuật

- Cần Internet để tải phông chữ *Noto Serif* từ Google Fonts; nếu offline, trang tự dùng phông dự phòng.
- Hình rồng và hình phượng được nhúng dưới dạng dữ liệu trong `index.html`. Hãy bảo đảm bạn có quyền sử dụng các hình này trước khi công khai.
- Nút **Lưu PDF** tạo file PDF dạng ảnh (chưa chọn/sao chép chữ được). Trên Safari, mình đã thêm bước tự hiệu chỉnh tỉ lệ nhưng chưa thử được trên thiết bị thật; nếu PDF lỗi, hãy dùng nút **In trực tiếp**.
- Chuyển đổi âm lịch theo thuật toán Hồ Ngọc Đức (múi giờ +7). Nguyệt kiến của Lục Hào tính theo tiết khí; sát giờ chuyển tiết (trong khoảng một giờ) kết quả có thể lệch.

## Lưu ý về nội dung

Mai Hoa Dịch Số và Lục Hào là phương pháp diễn giải truyền thống. Nội dung luận giải trong ứng dụng mang tính **tham khảo**, không xác định chắc chắn tương lai và **không thay thế** ý kiến chuyên môn (y tế, pháp lý, tài chính, bất động sản...). Con số phần trăm chỉ là cách diễn đạt mức cát – hung, không phải xác suất khoa học.

## Liên hệ

Huyền Học Đông A – Master Trần Đức Trường – 079 43 53 630

## Bản quyền

© Huyền Học Đông A. Mọi quyền được bảo lưu. (Hãy chỉnh mục này nếu bạn muốn chọn giấy phép mã nguồn mở, ví dụ MIT.)
