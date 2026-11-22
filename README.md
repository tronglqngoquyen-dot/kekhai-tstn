# Kê khai TSTN

**Phần mềm miễn phí, chạy offline** để lập, tự rà soát và xuất bản kê khai tài sản, thu nhập đúng mẫu **Phụ lục Nghị định số 164/2026/NĐ-CP** ngày 15/5/2026 của Chính phủ.

- 🌐 Dùng ngay / cài đặt: https://tronglqngoquyen-dot.github.io/kekhai-tstn/
- ⬇ Bản 1 file chạy không cần mạng: https://tronglqngoquyen-dot.github.io/kekhai-tstn/KeKhaiTSTN.html
- Phiên bản: 1.0.0

## Tính năng
- Đủ 4 phương thức: lần đầu, hằng năm, bổ sung, phục vụ công tác cán bộ (dùng chung 1 mẫu).
- Nhập theo đúng thứ tự mục I → IV của mẫu; mục trống tự ghi "Không có".
- Nhiều hồ sơ (tự kê khai hoặc hỗ trợ kê khai hộ), nhiều kỳ; **tạo kỳ mới từ kỳ trước**.
- Tự so sánh với kỳ trước để **gợi ý Mục III – biến động**; đối soát dòng tiền (tài sản tăng so với thu nhập).
- Trợ lý tính thu nhập từ hệ số lương theo từng giai đoạn lương cơ sở (2.340.000đ → 2.530.000đ từ 01/7/2026).
- Bộ **tự rà soát** theo Điều 9 NĐ 164 và 42 chú thích của mẫu: ngưỡng 150 triệu, ngoại tệ, địa chỉ sau sáp nhập, con đủ 18 tuổi, đứng tên hộ, giải trình biến động, kê khai bổ sung từ 1 tỷ...
- Xuất **Word (.docx)** đúng mẫu, in trực tiếp; xuất **.json** chuẩn hoá để chuyển sang phần mềm CSDL quốc gia khi có định dạng chính thức.
- **Chế độ Đầu mối đơn vị**: nhận file .tstn hoặc ghi nhận bản giấy; rà soát; góp ý và gửi trả; xuất danh sách theo phụ lục, sổ theo dõi giao nhận, phiếu góp ý.

## Quyền riêng tư
Không có máy chủ. Dữ liệu chỉ nằm trong trình duyệt của máy người dùng và trong các file người dùng tự lưu. File .tstn được mã hoá AES-256-GCM (khoá dẫn xuất PBKDF2-SHA256, 250.000 vòng) bằng mật khẩu do người dùng đặt. Khi có mạng, ứng dụng chỉ đọc `version.json` để báo phiên bản mới.

## Phát hành bản mới (dành cho tác giả)
1. Sửa mã nguồn, tăng `version` trong `src/core.js`.
2. Chạy `python3 build.py tronglqngoquyen-dot kekhai-tstn`.
3. Chép toàn bộ thư mục `dist/site/` lên nhánh `main` của repo `kekhai-tstn` → GitHub Pages tự cập nhật; người dùng PWA nhận bản mới khi mở lại, người dùng bản 1 file thấy thông báo tải bản mới.

## Bản quyền
© 2026 Lê Quang Trọng, đảo Phú Quý · 0909084181 · lequangtrong.c3ngoquyen@moet.edu.vn — xem LICENSE.txt.
