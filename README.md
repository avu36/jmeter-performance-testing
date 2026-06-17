# Báo cáo Bài tập Kiểm thử Hiệu năng với Apache JMeter

## Thông tin sinh viên
- **Họ và tên**: Đỗ Nguyên Anh Vũ
- **MSSV**:23010334
- **Lớp**: CSE703010-1-3-25(COUR01.LT3)
- **Môn học**: Kiểm thử Phần mềm / Performance Testing

## Mục tiêu bài tập
- Hiểu và sử dụng công cụ Apache JMeter để thực hiện kiểm thử tải (Load Testing).
- Xây dựng Test Plan cơ bản cho API/Web.
- Phân tích kết quả và viết báo cáo.

## 1. Giới thiệu về Apache JMeter
Apache JMeter là công cụ mã nguồn mở dùng để kiểm thử hiệu năng, load testing và stress testing. JMeter hỗ trợ nhiều giao thức: HTTP, HTTPS, JDBC, FTP, JMS...

**Ưu điểm**:
- Miễn phí, dễ sử dụng
- Giao diện GUI thân thiện
- Hỗ trợ recording script
- Báo cáo chi tiết (HTML Dashboard, Aggregate Report...)

## 2. Môi trường thực hiện
- **Công cụ**: Apache JMeter 5.6.3 (hoặc phiên bản mới nhất)
- **Ngôn ngữ**: Java JDK 17
- **Hệ điều hành**: Windows 11 / macOS / Linux
- **Ứng dụng kiểm thử**: [Ví dụ: JSONPlaceholder](https://jsonplaceholder.typicode.com) hoặc website/API của bạn

## 3. Test Plan đã thực hiện

### Kịch bản kiểm thử
- **Thread Group**: 10 users ảo, Ramp-up period 5 giây, Loop Count 3
- **HTTP Requests**:
  - GET `/posts`
  - GET `/users`
  - POST tạo bài viết mới
- **Elements sử dụng**:
  - HTTP Request Defaults
  - HTTP Cookie Manager
  - HTTP Header Manager
  - CSV Data Set Config (nếu có dữ liệu động)
  - Assertions (Response Assertion, JSON Assertion)
  - Listeners: View Results Tree, Aggregate Report, Summary Report

**File Test Plan**: [jmeter-test/TestPlan.jmx](jmeter-test/TestPlan.jmx)

## 4. Kết quả thực hiện

*(Bạn sẽ chụp ảnh và chèn vào đây)*

**Tóm tắt kết quả**:
- **Average Response Time**: XX ms
- **Error Rate**: 0%
- **Throughput**: XX requests/second
- **90% Percentile**: XX ms

**Ảnh minh họa**:
- Screenshot Test Plan
- Aggregate Report
- HTML Dashboard Report

## 5. Khó khăn gặp phải & Bài học rút ra
- Khó khăn: ...
- Bài học: Hiểu rõ hơn về khái niệm Load Testing, cách thiết kế kịch bản thực tế, tầm quan trọng của Ramp-up time và Assertions.

## 6. Tài liệu tham khảo
1. Video hướng dẫn: [JMeter Load Testing - Simplilearn](https://www.youtube.com/watch?v=NTyY8wKSvik)
2. Tài liệu chính thức: [https://jmeter.apache.org/](https://jmeter.apache.org/)
3. Các tutorial bổ sung: TutorialsPoint, BlazeMeter, YouTube channels...

## 7. Link nộp bài
- **GitHub Repository**:(https://github.com/avu36/jmeter-performance-testing/tree/main)

---
**Ngày hoàn thành**: 17/06/2026
