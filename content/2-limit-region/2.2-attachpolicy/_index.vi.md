+++
title = "Gán policy vào group"
weight = 2
chapter = false
pre = "<b>2.2 </b>"
+++

#### Gán policy vào group **CostTest**

1. Sau khi tạo policy thành công. Tại menu bên tay trái, click **User groups**.

![CostGovernance](/images/2-limit-region/0009.png?featherlight=false&width=90pc)

2. Click vào group **CostTest**.

![CostGovernance](/images/2-limit-region/0010.png?featherlight=false&width=90pc)

3. Tại trang của group **CostTest**.
    + Click tab **Permissions**.
    + Click **Add permissions**.
    + Click **Attach policies**.

![CostGovernance](/images/2-limit-region/0011.png?featherlight=false&width=90pc)

4. Tại ô Filter, click **Type**.

![CostGovernance](/images/2-limit-region/0012.png?featherlight=false&width=90pc)

5. Click **Type: Customer managed**.

![CostGovernance](/images/2-limit-region/0013.png?featherlight=false&width=90pc)


{{% notice tip %}}
Customer managed là các IAM Policy chúng ta tự tạo ra và quản lý.
{{% /notice %}}

6. Click vào ô Filter, điền tên policy chúng ta đã tạo ở bước trước ( **RegionRestrict** ).
    + Ấn phím **Enter**.

![CostGovernance](/images/2-limit-region/0014.png?featherlight=false&width=90pc)

7. Click chọn checkbox kế bên **RegionRestrict** policy.
    + Click **Add permissions**.

![CostGovernance](/images/2-limit-region/0015.png?featherlight=false&width=90pc)

8. Đảm bảo policy được gán thành công.

![CostGovernance](/images/2-limit-region/0016.png?featherlight=false&width=90pc)

Bước tiếp theo, chúng ta sẽ login bằng user **testuser** để kiểm tra quyền trên Region mà chúng ta đã gán.