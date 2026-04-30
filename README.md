# ESP32 IoT Environmental Monitoring System

A low-cost IoT system for real-time environmental monitoring and device control using ESP32, Firebase, and a Web interface.

---

## 1. Giới thiệu (Introduction)
Dự án tập trung vào việc phát triển một hệ thống giám sát môi trường tích hợp, sử dụng vi điều khiển ESP32 cùng các cảm biến phổ biến[cite: 1]. Hệ thống được thiết kế hướng tới tiêu chí chi phí thấp, dễ triển khai và có khả năng mở rộng, phù hợp cho các hộ gia đình hoặc trang trại quy mô nhỏ[cite: 1].

## 2. Thành phần hệ thống (System Components)

### Phần cứng (Hardware)[cite: 1]:
* **Vi điều khiển chính**: ESP32 (Tích hợp WiFi/Bluetooth, xung nhịp lên đến 240 MHz)[cite: 1].
* **Cảm biến ánh sáng**: BH1750 (Giao tiếp I2C, đo cường độ ánh sáng Lux)[cite: 1].
* **Cảm biến nhiệt độ & độ ẩm**: SHT31 (Giao tiếp I2C, độ chính xác cao)[cite: 1].
* **Hiển thị**: Màn hình OLED 1.3 inch (Hiển thị thông số thời gian thực)[cite: 1].
* **Cơ cấu chấp hành**: Servo SG90 (Mô phỏng điều khiển cửa thông gió, van nước)[cite: 1].
* **Khối nguồn**: Adapter 5V 3A, Jack DC-005, IC hạ áp AMS1117-3.3V[cite: 1].

### Công nghệ & Phần mềm (Tech Stack)[cite: 1]:
* **Môi trường lập trình**: PlatformIO IDE[cite: 1].
* **Ngôn ngữ**: C/C++ (Firmware), HTML/CSS/JavaScript (Web Dashboard)[cite: 1].
* **Nền tảng Cloud**: Firebase Realtime Database (Đồng bộ dữ liệu thời gian thực)[cite: 1].
* **Giao thức**: I2C (Kết nối đa thiết bị trên 2 dây tín hiệu), PWM (Điều khiển Servo)[cite: 1].

## 3. Sơ đồ hệ thống (System Architecture)
Hệ thống sử dụng ESP32 làm bộ xử lý trung tâm, thu thập dữ liệu từ cảm biến qua bus I2C và điều khiển Servo qua tín hiệu PWM[cite: 1].

![Sơ đồ khối hệ thống](đường_dẫn_ảnh_sơ_đồ_khối_từ_mục_4.1)[cite: 1]
![Sơ đồ nguyên lý mạch](đường_dẫn_ảnh_sơ_đồ_nguyên_lý_từ_mục_4.5)[cite: 1]

## 4. Đặc điểm nổi bật (Key Features)[cite: 1]
* **Giám sát thời gian thực**: Theo dõi nhiệt độ, độ ẩm và ánh sáng trực tiếp tại thiết bị qua OLED và qua giao diện Web từ xa[cite: 1].
* **Phản hồi tự động & thủ công**: Điều khiển Servo thông qua lệnh từ Internet để thực hiện các thao tác cơ khí[cite: 1].
* **Đồng bộ hóa dữ liệu**: Sử dụng Firebase giúp dữ liệu được cập nhật liên tục và ổn định trên nền tảng đám mây[cite: 1].
* **Thiết kế PCB chuyên nghiệp**: Hệ thống được đóng gói gọn gàng trên mạch in tự thiết kế và bảo vệ trong hộp kỹ thuật[cite: 1].

## 5. Hình ảnh thực tế (Project Showcase)

| Mạch in (PCB) đã hoàn thiện | Sản phẩm đóng gói thực tế |
| :---: | :---: |
| ![PCB_Soldered](đường_dẫn_ảnh_mạch_đã_hàn_từ_mục_7.2) | ![Final_Product](đường_dẫn_ảnh_sản_phẩm_từ_mục_7.4) |

## 6. Bài học rút ra (Lessons Learned)[cite: 1]
Thông qua dự án cá nhân này, em đã có cơ hội học hỏi và thực hành các kỹ năng[cite: 1]:
* Tìm hiểu quy trình lựa chọn linh kiện và thiết kế mạch điện tử dựa trên nhu cầu thực tế[cite: 1].
* Rèn luyện kỹ năng lập trình hệ thống nhúng và xử lý lỗi (debug) phần cứng lẫn phần mềm[cite: 1].
* Hiểu rõ cách triển khai một hệ thống IoT hoàn chỉnh từ thiết bị ngoại vi đến Cloud và người dùng cuối[cite: 1].

---
*Để biết thêm chi tiết về thông số kỹ thuật và hướng dẫn lắp đặt, vui lòng xem [Báo cáo đồ án chi tiết (PDF)](đường_dẫn_đến_file_pdf_trong_thư_mục_docs_của_em)[cite: 1].*
