+++
title = "Kiểm tra hiệu quả policy"
weight = 2
chapter = false
pre = "<b>4.2 </b>"
+++

#### Kiểm tra hiệu quả policy thông qua việc tạo EC2 instance khác t3.nano
1. Click vào tên user hiện tại đang login.
   + Click **Sign out**.

2. Click **Log back in**

![CostGovernance](/images/2-limit-region/0018.png?featherlight=false&width=90pc)

3. Tại **IAM user name** điền user mà chúng ta đã tạo (**testuser**).
   + Tại **Password** điền password chúng ta đã thiết lập (**Testuser123**).
   + Click **Sign in**.

![CostGovernance](/images/2-limit-region/0019.png?featherlight=false&width=90pc)

{{% notice tip %}}
Nếu bạn login không thành công hãy kiểm tra lại thông tin user và password đã tạo ở các bước trước. Ngoài ra hãy đảm bảo bạn sử dụng đúng AWS account ID khi login.
{{% /notice %}}

4. Click vào ô tìm kiếm, click **EC2** để chuyển đến giao diện quản lý của dịch vụ EC2.


5. Click **Launch instance**, sau đó click **Launch instance**.

![CostGovernance](/images/2-limit-region/0023.png?featherlight=false&width=90pc)

6. Tại **Name** điền **testserver**

![CostGovernance](/images/2-limit-region/0024.png?featherlight=false&width=90pc)

7. Tại **Key pair name**, click vào ô **Select**.
  + Chọn **Proceed without a key pair (Not recommended)


![CostGovernance](/images/2-limit-region/0025.png?featherlight=false&width=90pc)

{{% notice tip %}}
Chúng ta sẽ cần **key pair** để có thể thực hiện kết nối tới EC2 instance. Trong bài lab này chúng ta chỉ muốn kiểm tra quyền thao tác trên dịch vụ nên sẽ không cần kết nối tới EC2 instance.
{{% /notice %}}

7. Kéo xuống phía dưới, click vào instance type **t2.micro**.

![CostGovernance](/images/3-limit-family/0009.png?featherlight=false&width=90pc)

8. Tại ô  tìm kiếm , điền **t3**.
  + Click chọn instance type **t3.micro**.

![CostGovernance](/images/3-limit-family/0010.png?featherlight=false&width=90pc)

9. Kiểm tra **Instance type** đã thay đổi sang **t3.micro**.
  + Click **Launch instance**.


![CostGovernance](/images/2-limit-region/0026.png?featherlight=false&width=90pc)

{{% notice tip %}}
Trong bước này, chúng ta đã cố tạo 1 EC2 instance với instance type là **t3.micro** và quá trình tạo EC2 instance này không thành công do chúng ta chỉ có quyền để tạo các instance thuộc T3 family và có size là nano. ( **t3.nano** )
{{% /notice %}}


![CostGovernance](/images/4-limit-size/0005.png?featherlight=false&width=90pc)

#### Thử tạo máy chủ với T3 family và size nano (t3.nano)

1. Click **Edit instance config**.

![CostGovernance](/images/4-limit-size/0006.png?featherlight=false&width=90pc)

2. Kéo xuống phía dưới, click vào instance type **t3.micro**.

3. Tại ô  tìm kiếm , điền **t3**.
   + Click chọn instance type **t3.nano**.

![CostGovernance](/images/4-limit-size/0007.png?featherlight=false&width=90pc)

4. Kiểm tra **Instance type** đã thay đổi sang **t3.nano**.
   + Click **Launch instance**.

![CostGovernance](/images/4-limit-size/0008.png?featherlight=false&width=90pc)
5. Như vậy chúng ta đã tạo thành công EC2 instance với instance type là **t3.nano**.

![CostGovernance](/images/4-limit-size/0009.png?featherlight=false&width=90pc)

#### Xoá máy chủ testserver đã tạo
1. Click **View all instance**.

![CostGovernance](/images/4-limit-size/0010.png?featherlight=false&width=90pc)

2. Tại danh sách EC2 instance.
   + Click chọn **testserver**.

3. Click **Instance state**.
   + Click **Terminate instance** để tiến hành xoá máy chủ ảo **testserver**.
   + Click **Terminate** để xác nhận.
  
4. Đảm bảo bạn xoá instance thành công, tránh để phát sinh chi phí ngoài mong muốn.


![CostGovernance](/images/4-limit-size/0011.png?featherlight=false&width=90pc)

----

Trong bước này, chúng ta đã tạo thành công 1 EC2 instance với instance type là **t3.nano**. Trong phần sau chúng ta sẽ thử hạn chế việc tạo một instance với EBS volume type là **io1** nhé.