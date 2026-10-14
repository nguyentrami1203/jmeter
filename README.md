# THỰC HÀNH VỚI JMETER
# Kiểm tra hiệu năng web
Mục tiêu: 
- Sử dụng jMeter để tạo một kịch bản kiểm tra mô phỏng người dùng truy cập trang web https://phenikaa-uni.edu.vn/vi.
- Chạy kịch bản kiểm tra và ghi lại kết quả.
- Phân tích kết quả kiểm tra, bao gồm thời gian phản hồi, số lượng yêu cầu thành công, số lượng yêu cầu thất bại, v.v.
- Dựa trên kết quả phân tích, đưa ra kết luận về hiệu năng của trang web.
Kịch bản kiểm tra:
- Thread Group:
  - Số lượng thread: 500
  - Thời gian chạy: 60 giây
  - Ramp-up period: 50 giây
- HTTP Request:
   - URL: https://phenikaa-uni.edu.vn/vi
   - Method: GET
   - Content encoding: UTF-8
- Listeners:
  - View Results Tree
  - Aggregate Report
# Kết quả kiểm tra
<img width="2033" height="1271" alt="image" src="https://github.com/user-attachments/assets/c4ae3c14-60a0-47ac-9cef-cde216e5dae9" />

# Phân tích kết quả kiểm tra

- Số lượng yêu cầu được ghi nhận: 500

- Số lượng yêu cầu thành công: khoảng 51/500 = 10,2%

- Số lượng yêu cầu thất bại: khoảng 449/500 = 89,8%

- Thời gian phản hồi trung bình: 5.660 ms

- Thời gian phản hồi trung vị: 9.597 ms

- Thời gian phản hồi phân vị 90 (P90): 10.040 ms

- Chuyển tải (Throughput): 10 yêu cầu/giây

# Kết luận:

Kết quả kiểm thử bằng Apache JMeter 5.6.3 cho thấy website https://phenikaa-uni.edu.vn/vi có tỷ lệ yêu cầu thất bại cao (89,8%) và thời gian phản hồi tương đối lớn. Thời gian phản hồi trung bình đạt 5,66 giây, trong khi 90% số mẫu có thời gian phản hồi không vượt quá khoảng 10,04 giây. Thông lượng ghi nhận đạt 10 yêu cầu/giây.

Các kết quả này cho thấy kịch bản kiểm thử chưa đạt được mức ổn định mong đợi. Tuy nhiên, chưa thể khẳng định website không đáp ứng được 500 người dùng đồng thời khi chưa xác định nguyên nhân của các yêu cầu thất bại. Cần kiểm tra mã phản hồi HTTP, thông báo lỗi và khả năng kết nối để xác định nguyên nhân, sau đó thực hiện kiểm thử bổ sung trước khi đưa ra đánh giá cuối cùng về hiệu năng của website.

# Hình ảnh tổng quát
<img width="2036" height="1274" alt="image" src="https://github.com/user-attachments/assets/dc7317ce-05e6-4a0a-86b6-50787e020993" />
<img width="2032" height="1272" alt="image" src="https://github.com/user-attachments/assets/ee65ac06-1c6e-4904-8901-21819db7378d" />
