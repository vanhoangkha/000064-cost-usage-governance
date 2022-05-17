+++
title = "Giới hạn theo EBS volume"
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

#### Tạo chính sách ( policy ) giới hạn theo EBS volume type.

**Elastic Block Store (EBS)** là dịch vụ cung cấp hạ tầng lưu trữ cho EC2. Chúng ta có thể chọn lựa nhiều kiểu lưu trữ khác nhau tuỳ theo mục đích sử dụng. Việc quản lý loại lưu trữ có thể sử dụng cũng rất quan trọng  trong việc quản lý chi phí.
Trong bước này chúng ta sẽ tạo IAM policy không cho phép sử dụng loại volume **Provision IOPS (io1)**. **Provision IOPS (io1)** là loại volume cung cấp hiệu năng cao và chỉ dành cho những ứng dụng quan trọng.

#### Nội dung

- [Tạo policy giới hạn](5.1-createpolicy/)
- [Gán policy vào group](5.2-attachpolicy/)
- [Kiểm tra hiệu quả policy](5.3-testpolicy/)
