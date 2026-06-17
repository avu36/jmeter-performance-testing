# Báo cáo Bài tập Kiểm thử Hiệu năng với Apache JMeter

## Thông tin sinh viên
- **Họ và tên**: Đỗ Nguyên Anh Vũ
- **MSSV**: 23010334
- **Lớp**: CSE703010-1-3-25(COUR01.LT3)
- **Môn học**: Kiểm thử Phần mềm / Performance Testing

## Mục tiêu bài tập
- Làm quen với công cụ Apache JMeter.
- Xây dựng và thực hiện Load Testing cho REST API.
- Phân tích kết quả kiểm thử và viết báo cáo.

## 1. Giới thiệu về Apache JMeter
Apache JMeter là công cụ mã nguồn mở phổ biến dùng để kiểm thử hiệu năng (Performance Testing), Load Testing và Stress Testing. JMeter hỗ trợ nhiều giao thức, đặc biệt là HTTP/HTTPS.

**Công cụ sử dụng**: BlazeMeter (Cloud-based JMeter)

## 2. Môi trường thực hiện
- **Công cụ**: Apache JMeter + BlazeMeter
- **API kiểm thử**: JSONPlaceholder[](https://jsonplaceholder.typicode.com)
- **Cấu hình Thread Group**: 10 Virtual Users, Ramp-up 5 giây, Loop 3 lần

## 3. Test Plan
- **Kịch bản**: Thực hiện GET `/posts` và GET `/users`
- **File Test Plan**: [jmeter-test/TestPlan.jmx](jmeter-test/TestPlan.jmx)

## 4. Kết quả thực hiện

### 4.1. Tổng quan kết quả (Summary Report)
<img width="1920" height="924" alt="pass" src="https://github.com/user-attachments/assets/a576a11a-76c0-4527-8ea2-deae182e3d28" />

### 4.2. Cấu hình Test Plan
<img width="1919" height="870" alt="test" src="https://github.com/user-attachments/assets/c8efbe23-fed6-4d03-a631-a9e8e91a4c8f" />

### 4.3. Báo cáo chi tiết (Request Stats / Aggregate Report)
<img width="1914" height="870" alt="request" src="https://github.com/user-attachments/assets/81dd86b3-f611-4cd8-878e-3097b4f5167d" />

### 4.4. Biểu đồ Response Time & Throughput
<img width="1914" height="870" alt="timeline" src="https://github.com/user-attachments/assets/8ba6c292-828b-4a7a-893c-c682b347d07e" />

**Tóm tắt kết quả**:
- **Error Rate**: 0%
- **Average Response Time**: ~21.26 ms
- **Throughput**: ~127.77 Hits/s
- **90% Response Time**: ~27 ms

Kết quả cho thấy API phản hồi rất nhanh và ổn định dưới tải 10 users.

## 5. Khó khăn gặp phải & Bài học rút ra
- **Khó khăn**: Ban đầu gặp lỗi khi upload file .jmx lên BlazeMeter nên phải chỉnh sửa lại file test plan.
- **Bài học**: 
  - Hiểu rõ hơn về cách cấu hình Test Plan.
  - Biết cách sử dụng công cụ cloud (BlazeMeter) để chạy test mà không cần cài đặt JMeter cục bộ.
  - Tầm quan trọng của việc kiểm tra log khi test bị lỗi.

## 6. Tài liệu tham khảo
1. Video hướng dẫn: https://www.youtube.com/watch?v=NTyY8wKSvik
2. Tài liệu chính thức Apache JMeter: https://jmeter.apache.org/
3. Công cụ chạy test: BlazeMeter

## 7. Link nộp bài
- **GitHub Repository**: https://github.com/avu36/jmeter-performance-testing

---
**Ngày hoàn thành**: 17/06/2026
