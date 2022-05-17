+++
title = "Tạo IAM Group"
weight = 1
chapter = false
pre = "<b>1.1 </b>"
+++

#### Tạo IAM group

1. Truy cập vào [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
    + Tại menu bên trái, click **User groups**.

![CostGovernance](/images/1-preparation/0001.png?featherlight=false&width=90pc)

2. Tại trang **User groups**.
   + Click **Create group**.

![CostGovernance](/images/1-preparation/0002.png?featherlight=false&width=90pc)

3. Tại trang **Create user group**.
    + Đặt User group name là **CostTest**.

![CostGovernance](/images/1-preparation/0003.png?featherlight=false&width=90pc)

4. Kéo trang xuống dưới cùng và click **Create group**.


![CostGovernance](/images/1-preparation/0004.png?featherlight=false&width=90pc)

5. Chúng ta sẽ thấy **CostTest** user group được tạo thành công như hình dưới.


Trong bước tiếp theo chúng ta sẽ tạo IAM user **testuser** nằm trong **CostTest** group.