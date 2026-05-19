# Mạch MKE-M21 SIM7680C 4G SMS/CALL Module

*****Lưu ý quan trọng:**
- SIM phải được đăng ký 4G và dịch vụ VoLTE (HD Voice) trước khi sử dụng!!!
- Sản phẩm này là mạch phát triển được thiết kế phục vụ cho mục đích nghiên cứu, thử nghiệm và học tập, không phải là một thiết bị hoàn chỉnh và không thể hoạt động độc lập như một sản phẩm thương mại. Trong trường hợp người dùng kết hợp mạch này với các linh kiện, thiết bị hoặc phần mềm khác để tạo thành một hệ thống hoặc sản phẩm hoàn chỉnh, mọi chức năng, độ an toàn và tính phù hợp của sản phẩm sau cùng đều thuộc trách nhiệm của người sử dụng.

## Giới thiệu
Mạch MKE-M21 SIM7680C 4G SMS/CALL Module giúp các bạn có thể dễ dàng gọi điện hoặc gửi tin nhắn SMS qua nền tảng 4G thay thế cho các Module SIM sử dụng 2G cũ hiện đã ngưng hoạt động, module được thiết kế nhỏ gọn với khối SIM và khối cấp nguồn tách rời giúp bạn dễ dàng lựa chọn phiên bản kèm khối cấp nguồn hoặc không kèm khối cấp nguồn (phiên bản không kèm khối cấp nguồn sẽ tương thích về kích thước và chuẩn chân với module SIM800C 2G cũ), thích hợp với các ứng dụng IoT, cảnh báo, gọi điện, nhắn tin qua 4G.

Mạch MKE-M21 SIM7680C 4G SMS/CALL Module hỗ trợ điện áp giao tiếp 3.3/5VDC, cho phép kết nối trực tiếp và an toàn với hầu hết các bo mạch điều khiển phổ biến hiện nay như: Arduino, Raspberry Pi, Jetson Nano, Micro:bit,… Mạch đi kèm cáp kết nối 3P XH2.54–Dupont đảm bảo chắc chắn, ổn định và linh hoạt khi kết nối.

## Thông số kỹ thuật
- IC chính: SIM7680C
- Sử dụng 4G LTE CAT1
- Sử dụng 4G Nano SIM
- Điện áp hoạt động:
  - Cấp nguồn trực tiếp vào khối SIM, không đi kèm khối cấp nguồn: 3.7~4VDC
  - Cấp nguồn qua khối cấp nguồn: 5~24VDC
- Dòng điện tiêu thụ khi hoạt động: Trung bình 300mA, khi gọi hoặc nhắn tin có những thời điểm có thể lên tới 1A.
- Chuẩn giao tiếp: UART, Baudrate được thiết lập mặc định 9600 (Quan trọng: Test thực tế với Arduino set baudrate cao như 115200 truyền nhận rất dễ lỗi khiến module hoạt động kém ổn định) 
- Điện áp giao tiếp: TTL 3.3VDC / 5VDC
- Sử dụng trực tiếp an toàn với các board mạch giao tiếp ở cả hai mức điện áp 3.3VDC và 5VDC như: Arduino, Raspberry Pi, Jetson Nano, Micro:bit,....
- Khả năng tương thích:
  - Arduino
  - Raspberry Pi
  - Jetson Nano
  - Micro:bit
  - Và các board điều khiển 3.3/5VDC khác
- Thiết kế mạch:
  - Hoạt động ổn định, chống nhiễu tốt
  - Giao tiếp đơn giản chỉ với 2 dây tín hiệu
  - Phù hợp cho ứng dụng học tập và thực tế
- Đi kèm cáp kết nối: 4P XH2.54 – Dupont

## Các chân tín hiệu
Chân tín hiệu trên khối SIM7680x:
- NET:	Chân trạng thái được nối với led STT
- NC:	Chân không kết nối
- MIC+: Chân Micro
- MIC-: Chân Micro
- SP+: Chân Speaker
- SP-: Chân Speaker
- ATN: Chân Antenna
- 4V: Chân cấp nguồn dương từ 3.7~4VDC
- RST: Chân Reset của
- RX: chân UART RX tương thích 3.3/5VDC (có qua mạch chuyển mức tín hiệu)
- TX: chân UART TX tương thích 3.3/5VDC (có qua mạch chuyển mức tín hiệu)
- GND: chân cấp nguồn âm 0VDC

Chân tín hiệu khi sử dụng kèm khối cấp nguồn:
- GND:	Chân cấp nguồn âm 0VDC
- 5V:	Chân cấp nguồn dương 5~24VDC
- TX: Chân UART TX
- RX: Chân UART RX

<table><thead>
  <tr>
    <th>MKE-S01</th>
    <th>Ghi chú</th>
  </tr></thead>
<tbody>
  <tr>
    <td>GND</td>
    <td>Chân cấp nguồn âm 0VDC</td>
  </tr>
  <tr>
    <td>5V</td>
    <td>Chân cấp nguồn dương 5VDC</td>
  </tr>
  <tr>
    <td>TRIG</td>
    <td>Chân tín hiệu ngõ vào Trigger</td>
  </tr>
  <tr>
    <td>ECHO</td>
    <td>Chân tín hiệu ngõ ra Echo</td>
  </tr>
</tbody>
</table>
## Hướng dẫn sử dụng
### Hướng dẫn kết nối
- Cấp nguồn 5VDC cho mạch qua hai chân GND và 5V.
- kết nối chân TRIG và ECHO của Sensor với chân điều khiển được khai báo trong chương trình.

### Hướng dẫn sử dụng với Arduino Uno / Vietduino Uno / ESP32
- Trong **Tools / Library Manager**, tìm và cài đặt bộ thư viện tổng hợp **"MKE_ONE" by MakerEdu.vn**
- Mở chương trình mẫu **"MKE_S01_Ultrasonic_Serial_XXX"** tại **File / Examples / MAKEREDU / Module / MKE_S01_Ultrasonic**
- Cấu hình board mạch tương ứng là **Arduino Uno / ESP32**, chọn đúng cổng **COM Port** của mạch và nhấn **Upload** để nạp chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân TRIG và ECHO của Sensor với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

### Hướng dẫn lập trình với Micro:bit (kéo thả khối)

- Khởi động [Microsoft MakeCode](https://makecode.microbit.org/) và **Import** chương trình theo đường link sau: `https://github.com/makereduvn/mke_s01_ultrasonic_microbit/`
- Kết nối mạch Micro:bit và **Download** chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân TRIG và ECHO của Sensor với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

Nếu bắt đầu tự án mới cần cài đặt Extension **MKE_ONE_MICROBIT** trên [Microsoft MakeCode](https://makecode.microbit.org/) theo [hướng dẫn tại đây](https://github.com/makereduvn/MKE_ONE_MICROBIT). Sau khi cài đặt thành công, các khối lệnh của Extension **MKE_ONE_MICROBIT** sẽ xuất hiện trong danh sách block và sẵn sàng để sử dụng.

## Kích thước sản phẩm
![MKE-S01 Ultrasonic](/extras/MKE-S01_1.jpg)

## Hình ảnh sản phẩm
![MKE-S01 Ultrasonic](/extras/MKE-S01_2.png)
![MKE-S01 Ultrasonic](/extras/MKE-S01_3.png)

