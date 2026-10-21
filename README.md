# HCM-KS26-CNTT2_Nhap-mon-CNTT_Session10_Ex05

# Dự án Smart-Farm
Hệ thống tự động chăm sóc hoa Lan.

## 1. Tính năng chính
- Đo nhiệt độ/độ ẩm.
- Tự động tưới nước.
- Gửi tin nhắn cảnh báo.

## 2. Cấu trúc thiết bị (Mô hình IPO)
- **Đầu vào (Input):** Cảm biến đo dữ liệu môi trường.
- **Xử lý (Processing):** Mạch Raspberry Pi tính toán dữ liệu.
- **Đầu ra (Output):** Máy bơm phun nước.

## 3. Cách chạy
Tải mã nguồn về máy và gõ lệnh chạy file python.

## 4. Nguyên lý hoạt động
- **Hoạt động của chip (CPU):** Lấy lệnh -> Dịch hiểu lệnh -> Cấp điện cho máy bơm chạy.
- **Logic ra quyết định (DIKW):** Đọc được số liệu -> Hiểu là 36 độ C và đất rất khô -> Nhận định cây đang thiếu nước -> Quyết định bật máy bơm ngay lập tức.

## 5. Lưu ý bảo trì
Máy chạy lâu sẽ lưu nhiều file nhật ký (log) gây đầy RAM và treo máy. Chỉ cần vào đúng thư mục chứa log để xóa các file cũ là được, tuyệt đối không gõ lệnh xóa sạch toàn bộ ổ đĩa.
