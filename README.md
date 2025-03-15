🌱 Vườn Thông Minh Ứng Dụng AI và IoT
📌 Giới Thiệu
Hệ thống vườn thông minh là một giải pháp kết hợp IoT và trí tuệ nhân tạo (AI) để giám sát và điều khiển tự động môi trường vườn. Hệ thống giúp:
✅ Theo dõi tình trạng đất, ánh sáng, độ ẩm.
✅ Tưới nước tự động.
✅ Nhận diện hình ảnh để phát hiện người lạ xâm nhập hoặc xác định thời điểm thu hoạch cây trồng.

🎯 Mục Tiêu
✔ Xây dựng hệ thống IoT thu thập dữ liệu môi trường.
✔ Triển khai AI phân tích hình ảnh và tối ưu hóa việc chăm sóc cây trồng.
✔ Phát triển giao diện app Blynk để giám sát & điều khiển từ xa.
✔ Nhận diện người lạ, gửi cảnh báo Telegram.

🏢 Kiến Trúc Hệ Thống
🔧 Phần Cứng
Thành phần	Chức năng
Cảm biến độ ẩm đất	Đo độ ẩm đất
Cảm biến ánh sáng	Đo cường độ ánh sáng
Cảm biến mưa	Phát hiện mưa
Arduino Uno	Vi điều khiển chính
ESP32/ESP8266	Kết nối Internet
ESP32-CAM	Nhận diện hình ảnh
Máy bơm nước	Tưới nước tự động
Relay	Điều khiển bật/tắt thiết bị
💻 Phần Mềm
✔ Giám sát môi trường: Hiển thị dữ liệu cảm biến theo thời gian thực.
✔ Tưới cây tự động:

Độ ẩm đất < 50% → Bật máy bơm.
Độ ẩm đất > 50% → Tắt máy bơm.
✔ Điều khiển từ xa: Bật/tắt thiết bị qua app Blynk.
✔ Nhận diện hình ảnh:
Người lạ → Gửi cảnh báo Telegram.
Cây trồng → Xác định thời điểm thu hoạch.
🚀 Hướng Dẫn Cài Đặt
🛠 1. Yêu Cầu Hệ Thống
Loại	Công Nghệ
Phần mềm	Python 3.13.2, Arduino IDE
Thư viện	ESP32, ESP8266, OpenCV, Flask, ultralytics, torch
📥 2. Cài Đặt
bash
Sao chép
Chỉnh sửa
# Clone repository
git clone https://github.com/Nghia2624/VuonThongMinh
cd VuonThongMinh

# Cài đặt thư viện Python
pip install ultralytics opencv-python torch torchvision numpy

# Chạy server
python app.py
🔌 3. Kết Nối Phần Cứng
✅ Nạp code vào Arduino/ESP32.
✅ Kiểm tra cảm biến hoạt động chính xác.
✅ Kết nối ESP32-CAM để lấy luồng hình ảnh.

📊 Giao Diện Web
✔ Hiển thị hình ảnh trực tiếp từ ESP32-CAM.
✔ Phân tích hình ảnh, phát hiện người lạ.
✔ Gửi cảnh báo Telegram khi phát hiện người.

🤖 AI và Nhận Diện Hình Ảnh
✔ Mô hình: YOLOv8 để nhận diện người lạ và phân tích cây trồng.
✔ Xử lý ảnh: OpenCV trích xuất thông tin.
✔ Lưu trữ log: Ghi lại thời gian và hình ảnh khi phát hiện người lạ.

📝 Nhóm Thực Hiện
👨‍💻 Thành viên:

Đỗ Ngọc Nghĩa
Bùi Văn Trường
Nguyễn Thành Hưng
Nguyễn Chí Nhật
📚 Lớp: CNTT 16-03
