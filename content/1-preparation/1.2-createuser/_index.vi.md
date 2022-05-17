+++
title = "Tạo IAM user"
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

#### Tạo IAM group

1. Sau khi tạo group thành công, tại menu bên tay trái.
    + Click **Users**.

![CostGovernance](/images/1-preparation/0006.png?featherlight=false&width=90pc)

2. Tại trang **Users**.
    + Click **Add users**.

![CostGovernance](/images/1-preparation/0007.png?featherlight=false&width=90pc)

3. Tại trang **Add user**.
    + Đặt **User name** là **testuser**.
    + Click chọn **Password - AWS Management Console access** để cho user login vào management console.
    + Click chọn **Custom password** để đặt password tuỳ chỉnh.
    + Đặt password là **Testuser123**.
    + Bỏ chọn **User must create a new password at next sign-in**.
    + Click **Next:Permissions**.

![CostGovernance](/images/1-preparation/0008.png?featherlight=false&width=90pc)

4. Click chọn **CostTest** group, sau đó click **Next: Tags**.

![CostGovernance](/images/1-preparation/0009.png?featherlight=false&width=90pc)

5. Click **Next: Review**.

![CostGovernance](/images/1-preparation/0010.png?featherlight=false&width=90pc)

6. Kiểm tra lại thông tin, click **Create user**.

![CostGovernance](/images/1-preparation/0011.png?featherlight=false&width=90pc)

7. Đảm bảo user tạo thành công. Click **Close**.

![CostGovernance](/images/1-preparation/0012.png?featherlight=false&width=90pc)

Chúng ta đã xong phần chuẩn bị IAM user và group, tiếp theo chúng ta sẽ tiến hành phân quyền để hạn chế việc sử dụng tài nguyên theo Region.