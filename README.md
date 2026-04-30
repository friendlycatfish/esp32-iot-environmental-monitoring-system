# ESP32 IoT Environmental Monitoring System

A low-cost IoT system for real-time environmental monitoring and device control using ESP32, Firebase, and a Web interface.

---

## 1. Giới thiệu (Introduction)
Dự án tập trung vào việc phát triển một hệ thống giám sát môi trường tích hợp, sử dụng vi điều khiển ESP32 cùng các cảm biến phổ biến. Hệ thống được thiết kế hướng tới tiêu chí chi phí thấp, dễ triển khai và có khả năng mở rộng, phù hợp cho các hộ gia đình hoặc trang trại quy mô nhỏ.

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
* **Giao thức**: I2C (Kết nối đa thiết bị), PWM (Điều khiển Servo)[cite: 1].

## 3. Sơ đồ hệ thống (System Architecture)

![System Block Diagram](images/system-block-diagram.jpg)
*Hình 1: Sơ đồ khối thể hiện luồng dữ liệu giữa MCU ESP32, các cảm biến qua I2C và kết nối Cloud qua WiFi[cite: 1].*

![Circuit Schematic](images/circuit-schematic.jpg)
*Hình 2: Sơ đồ nguyên lý chi tiết bao gồm khối nguồn hạ áp, mạch nạp UART CH340C và mạch auto-reset[cite: 1].*

## 4. Đặc điểm nổi bật (Key Features)[cite: 1]
* **Giám sát thời gian thực**: Theo dõi nhiệt độ, độ ẩm và ánh sáng trực tiếp tại thiết bị qua OLED và qua giao diện Web từ xa[cite: 1].
* **Phản hồi từ xa**: Điều khiển Servo thông qua lệnh từ Internet để thực hiện các thao tác cơ khí mô phỏng[cite: 1].
* **Đồng bộ hóa dữ liệu**: Sử dụng Firebase giúp dữ liệu được cập nhật liên tục và ổn định trên nền tảng đám mây[cite: 1].
* **Thiết kế PCB**: Hệ thống được đóng gói gọn gàng trên mạch in tự thiết kế và bảo vệ trong hộp kỹ thuật[cite: 1].

## 5. Hình ảnh thực tế (Project Showcase)[cite: 1]

| Mạch in chưa hàn | Mạch đã hàn linh kiện | Sản phẩm hoàn thiện |
| :---: | :---: | :---: |
| ![Bare_PCB](images/mach-chua-han.jpg) | ![Soldered_PCB](images/mach-da-han.jpg) | ![Final_Product](images/san-pham-hoan-thien.jpg) |
| *Hình 3: Mạch in (PCB) lớp Top chưa lắp linh kiện[cite: 1].* | *Hình 4: Mạch thực tế sau khi hàn lắp linh kiện dán (SMD)[cite: 1].* | *Hình 5: Hệ thống hoàn chỉnh được đóng gói trong hộp nhựa kỹ thuật[cite: 1].* |

## 6. Bài học rút ra (Lessons Learned)[cite: 1]
Thông qua dự án cá nhân này, em đã có cơ hội học hỏi và thực hành các kỹ năng:
* Tìm hiểu quy trình lựa chọn linh kiện và thiết kế mạch điện tử dựa trên nhu cầu thực tế[cite: 1].
* Rèn luyện kỹ năng lập trình hệ thống nhúng và xử lý lỗi (debug) phần cứng lẫn phần mềm[cite: 1].
* Hiểu rõ cách triển khai một hệ thống IoT hoàn chỉnh từ thiết bị ngoại vi đến Cloud và người dùng cuối[cite: 1].

---
*Để biết thêm chi tiết về thông số kỹ thuật và hướng dẫn lắp đặt, vui lòng xem [Báo cáo đồ án chi tiết (PDF)](docs/BAO-CAO-DO-AN-CHUAN.pdf)[cite: 1].*
