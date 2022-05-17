+++
title = "Giới hạn theo Region"
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

#### Tạo chính sách ( policy ) giới hạn sử dụng dịch vụ theo Region

Để quản lý chi phí, bạn cần quản lý và kiểm soát việc sử dụng của mình. AWS cung cấp nhiều Region, do đó, tùy thuộc vào yêu cầu của mình, bạn có thể giới hạn quyền truy cập vào các dịch vụ AWS tùy thuộc vào Region. 

Điều này có thể được sử dụng để đảm bảo việc sử dụng chỉ được phép ở các khu vực cụ thể tiết kiệm chi phí hơn và giảm thiểu việc sử dụng và chi phí liên quan, chẳng hạn như chi phí truyền dữ liệu.

Chúng ta sẽ tạo một chính sách cho phép tất cả các truy cập EC2, RDS và S3 chỉ trong một Region duy nhất. 

{{% notice tip %}}
Cách tốt nhất là chỉ cung cấp quyền truy cập tối thiểu cần thiết, chính sách được sử dụng ở đây là ngắn gọn và đơn giản và chỉ nên được sử dụng cho bài lab trước khi bị xóa.
{{% /notice %}}


#### Nội dung

- [Tạo policy giới hạn](2.1-createpolicy/)
- [Gán policy vào group](2.2-attachpolicy/)
- [Kiểm tra hiệu quả policy](2.3-testpolicy/)
