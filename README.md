# HCM-KS26-CNTT2_Nhap-mon-CNTT_Session10_Ex05

#  Dự án Smart-Farm

![Sơ đồ Smart Farm](https://via.placeholder.com/800x400.png?text=Smart+Farm "Sơ đồ hệ thống")

## 1. Tính năng
- [x] Thu thập dữ liệu môi trường.
- [x] Tự động tưới tiêu.
- [ ] Gửi tin nhắn cảnh báo.

## 2. Phần cứng (Mô hình IPO)
| Thành phần (IPO) | Thiết bị | Chức năng |
| :--- | :--- | :--- |
| **Input** | Cảm biến DHT22 | Đọc nhiệt độ, độ ẩm |
| **Processing** | SoC Raspberry Pi 4 | Phân tích dữ liệu |
| **Output** | Bơm chìm 12V | Bơm nước |

## 3. Cài đặt
git clone [https://github.com/GreenTech/smart-farm.git](https://github.com/GreenTech/smart-farm.git)
cd smart-farm
python3 main_controller.py


## 4. Nguyên lý hoạt động

> **Chu kỳ lệnh CPU khi bật máy bơm (Fetch–Decode–Execute):**
> Lấy lệnh từ RAM (Fetch) ➔ Dịch thành tín hiệu điện (Decode) ➔ Cấp điện 3.3V ra chân GPIO để chạy bơm (Execute).

**Ứng dụng DIKW:**

* **Data:** 36, 30.
* **Information:** Nhiệt độ 36°C, độ ẩm 30%.
* **Knowledge:** Trời đang quá nóng và khô đối với hoa Lan.
* **Wisdom:** Ra lệnh bật máy bơm ngay lập tức để cứu cây.

## 5. Bảo trì (Lỗi đầy RAM)

Khi hệ thống chạy lâu, file log sẽ làm đầy RAM gây treo máy. **Tuyệt đối không dùng lệnh xóa đệ quy ổ C**. Xử lý an toàn như sau:

Set-Location ".\logs"
Remove-Item -Path "*.log" -Force
