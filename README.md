# Mạch MKE-M21 SIM7680C 4G SMS/CALL Module

*****Lưu ý quan trọng:**
- SIM phải được đăng ký 4G và dịch vụ VoLTE (HD Voice) trước khi sử dụng!!!
- Sản phẩm này là mạch phát triển được thiết kế phục vụ cho mục đích nghiên cứu, thử nghiệm và học tập, không phải là một thiết bị hoàn chỉnh và không thể hoạt động độc lập như một sản phẩm thương mại. Trong trường hợp người dùng kết hợp mạch này với các linh kiện, thiết bị hoặc phần mềm khác để tạo thành một hệ thống hoặc sản phẩm hoàn chỉnh, mọi chức năng, độ an toàn và tính phù hợp của sản phẩm sau cùng đều thuộc trách nhiệm của người sử dụng.

## Giới thiệu
MKE-M21 SIM7680C 4G SMS/CALL Module là mạch phát triển sử dụng IC SIM7680C, cho phép thực hiện các chức năng gọi điện thoại (Voice Call) và gửi/nhận tin nhắn SMS trên nền tảng mạng 4G LTE CAT1, thay thế hoàn toàn cho các module 2G như SIM800C hiện đã không còn hoạt động tại nhiều khu vực.

Module được thiết kế nhỏ gọn với khối SIM và khối cấp nguồn tách rời, giúp người dùng dễ dàng lựa chọn phiên bản có hoặc không kèm khối nguồn. Phiên bản không kèm khối cấp nguồn vẫn giữ nguyên kích thước và chuẩn chân tương thích với các module SIM800C cũ, giúp nâng cấp hệ thống hiện có một cách thuận tiện mà không cần thay đổi nhiều về cơ khí và kết nối.

Mạch được ứng dụng rộng rãi trong nhiều hệ thống thực tế như: thiết bị cảnh báo qua điện thoại, hệ thống chống trộm, bộ gọi điện khẩn cấp, thiết bị giám sát từ xa, nhà thông minh, bộ điều khiển công nghiệp, hệ thống thông báo tự động, hệ thống IoT và các thiết bị cần truyền thông qua mạng di động 4G.

Sản phẩm đặc biệt phù hợp cho các mô hình robot, dự án STEM, đồ án học tập và thực hành điện – điện tử, giúp người học dễ dàng tiếp cận công nghệ truyền thông di động, giao tiếp UART, điều khiển module bằng tập lệnh AT Command và xây dựng các hệ thống IoT hiện đại. Đây là công cụ lý tưởng cho học sinh, sinh viên, giáo viên giảng dạy STEM, kỹ sư nghiên cứu và những người yêu thích sáng tạo công nghệ.

MKE-M21 hỗ trợ điện áp giao tiếp 3.3VDC và 5VDC, cho phép kết nối trực tiếp và an toàn với Arduino, Raspberry Pi, NVIDIA, Micro:bit Educational Foundation và nhiều nền tảng điều khiển khác. Sản phẩm đi kèm cáp kết nối 4P XH2.54 – Dupont, đảm bảo kết nối chắc chắn, ổn định và linh hoạt trong quá trình sử dụng.

## Thông số kỹ thuật
- IC chính: SIM7680C
- Công nghệ mạng: 4G LTE CAT1
- Chức năng hỗ trợ:
  - Gọi điện thoại (Voice Call)
  - Gửi và nhận tin nhắn SMS
  - Điều khiển bằng tập lệnh AT Command
- Loại SIM sử dụng: Nano SIM 4G
- Điện áp hoạt động:
  - Cấp trực tiếp vào khối SIM (không kèm khối cấp nguồn): 3.7 ~ 4.0VDC
  - Cấp qua khối cấp nguồn đi kèm: 5 ~ 24VDC
- Dòng điện tiêu thụ:
  - Trung bình khoảng 300mA
  - Khi gọi điện hoặc nhắn tin có thể xuất hiện các xung dòng tức thời lên đến 1A
- Chuẩn giao tiếp: UART
- Baudrate mặc định: 9600bps
- Khuyến nghị sử dụng:
  - Nên sử dụng baudrate 9600bps để đảm bảo truyền nhận dữ liệu ổn định
  - Thiết lập baudrate quá cao (ví dụ 115200bps) trên một số nền tảng như Arduino có thể gây lỗi truyền dữ liệu và làm module hoạt động kém ổn định
- Điện áp giao tiếp: TTL 3.3VDC / 5VDC
- Khả năng tương thích:
  - Arduino
  - Raspberry Pi
  - Jetson Nano
  - Micro:bit
  - Và các board điều khiển 3.3VDC / 5VDC khác
- Thiết kế mạch:
  - Hoạt động ổn định, chống nhiễu tốt
  - Khối nguồn tách rời linh hoạt
  - Giao tiếp UART đơn giản chỉ với hai chân TX và RX
  - Phù hợp cho ứng dụng học tập và thực tế
- Đi kèm cáp kết nối: 4P XH2.54 – Dupont

## Các chân tín hiệu
### Các chân tín hiệu trên khối SIM7680x

| Chân | Ghi chú |
|------|---------|
| NET  | Chân trạng thái, được nối với LED STT |
| NC   | Chân không kết nối (No Connect) |
| MIC+ | Chân kết nối Micro (+) |
| MIC- | Chân kết nối Micro (-) |
| SP+  | Chân kết nối Speaker (+) |
| SP-  | Chân kết nối Speaker (-) |
| ATN  | Chân kết nối Antenna |
| 4V   | Chân cấp nguồn dương 3.7 ~ 4.0VDC |
| RST  | Chân Reset của module |
| RX   | Chân UART RX, tương thích TTL 3.3VDC / 5VDC (có tích hợp mạch chuyển mức tín hiệu) |
| TX   | Chân UART TX, tương thích TTL 3.3VDC / 5VDC (có tích hợp mạch chuyển mức tín hiệu) |
| GND  | Chân cấp nguồn âm 0VDC |

### Các chân tín hiệu khi sử dụng kèm khối cấp nguồn

| Chân | Ghi chú |
|------|---------|
| GND  | Chân cấp nguồn âm 0VDC |
| 5V   | Chân cấp nguồn dương 5 ~ 24VDC |
| TX   | Chân UART TX |
| RX   | Chân UART RX |
## Hướng dẫn sử dụng
### Hướng dẫn kết nối khi sử dụng cùng với khối cấp nguồn
- Cấp nguồn 5VDC cho mạch qua hai chân GND và 5V.
- kết nối chân TX và RX của Module với chân điều khiển được khai báo trong chương trình.

### Hướng dẫn sử dụng với Arduino Uno / Vietduino Uno / ESP32
- Trong **Tools / Library Manager**, tìm và cài đặt bộ thư viện tổng hợp **"MKE_ONE" by MakerEdu.vn**
- Mở chương trình mẫu **"MKE_M21_SIM7680C_Serial_XXX"** tại **File / Examples / MAKEREDU / Module / M21_SIM7680C**
- Cấu hình board mạch tương ứng là **Arduino Uno / ESP32**, chọn đúng cổng **COM Port** của mạch và nhấn **Upload** để nạp chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân TX và RX của Module với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

### Hướng dẫn lập trình với Micro:bit (kéo thả khối)

- Khởi động [Microsoft MakeCode](https://makecode.microbit.org/) và **Import** chương trình theo đường link sau: `https://github.com/makereduvn/mke_s01_ultrasonic_microbit/`
- Kết nối mạch Micro:bit và **Download** chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân TX và RX của Module với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

Nếu bắt đầu tự án mới cần cài đặt Extension **MKE_ONE_MICROBIT** trên [Microsoft MakeCode](https://makecode.microbit.org/) theo [hướng dẫn tại đây](https://github.com/makereduvn/MKE_ONE_MICROBIT). Sau khi cài đặt thành công, các khối lệnh của Extension **MKE_ONE_MICROBIT** sẽ xuất hiện trong danh sách block và sẵn sàng để sử dụng.

## Kích thước sản phẩm
### Khối SIM7680x
![MKE-M21 SIM7680C](/extras/MKE-M21_1.jpg)
### Khối cấp nguồn
![MKE-M21 SIM7680C](/extras/MKE-M21_2.jpg)

## Hình ảnh sản phẩm
### Khối SIM7680x
![MKE-M21 SIM7680C](/extras/MKE-M21_3.png)
![MKE-M21 SIM7680C](/extras/MKE-M21_4.png)
### Khối cấp nguồn
![MKE-M21 SIM7680C](/extras/MKE-M21_5.png)
![MKE-M21 SIM7680C](/extras/MKE-M21_6.png)
