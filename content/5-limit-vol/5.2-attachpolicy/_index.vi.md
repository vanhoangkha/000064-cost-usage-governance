+++
title = "Gán policy vào group"
weight = 2
chapter = false
pre = "<b>5.2 </b>"
+++

#### Gán policy vào group **CostTest**

1. Sau khi tạo policy thành công. Tại menu bên tay trái, click **User groups**.
   + Click vào group **CostTest**.

![CostGovernance](/images/3-limit-family/0004.png?featherlight=false&width=90pc)

3. Tại trang của group **CostTest**.
   + Click tab **Permissions**.
   + Click **Add permissions**.
   + Click **Attach policies**.

4. Tại ô Filter, click **Type**.

![CostGovernance](/images/2-limit-region/0012.png?featherlight=false&width=90pc)

5. Click **Type: Customer managed**.

![CostGovernance](/images/2-limit-region/0013.png?featherlight=false&width=90pc)


{{% notice tip %}}
Customer managed là các IAM Policy chúng ta tự tạo ra và quản lý.
{{% /notice %}}

6. Click vào ô Filter, điền tên policy chúng ta đã tạo ở bước trước ( **EC2EBS_Restrict** ).
   + Ấn phím **Enter**.

7. Click chọn checkbox kế bên **EC2EBS_Restrict** policy.
   + Click **Add permissions**.

![CostGovernance](/images/5-limit-vol/0003.png?featherlight=false&width=90pc)

8. Đảm bảo policy được gán thành công.

![CostGovernance](/images/2-limit-region/0016.png?featherlight=false&width=90pc)


Bước tiếp theo, chúng ta sẽ login bằng user **testuser** để kiểm tra xem chúng ta có thể tạo được máy chủ EC2 có kèm EBS volume với type là **io1** hay không.