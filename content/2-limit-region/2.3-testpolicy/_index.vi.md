+++
title = "Kiểm tra hiệu quả policy"
weight = 3
chapter = false
pre = "<b>2.3 </b>"
+++

#### Kiểm tra hiệu quả policy thông qua việc tạo EC2 instance ở Region cho phép

1. Click vào tên user hiện tại đang login.
    + Click **Sign out**.

![CostGovernance](/images/2-limit-region/0017.png?featherlight=false&width=90pc)

2. Click **Log back in**

![CostGovernance](/images/2-limit-region/0018.png?featherlight=false&width=90pc)

3. Tại **IAM user name** điền user mà chúng ta đã tạo (**testuser**).
    + Tại **Password** điền password chúng ta đã thiết lập (**Testuser123**).
    + Click **Sign in**.

![CostGovernance](/images/2-limit-region/0019.png?featherlight=false&width=90pc)

{{% notice tip %}}
Nếu bạn login không thành công hãy kiểm tra lại thông tin user và password đã tạo ở các bước trước. Ngoài ra hãy đảm bảo bạn sử dụng đúng AWS account ID khi login.
{{% /notice %}}

4. Click **Switch to the new Console Home** để chuyển sang giao diện mới.

![CostGovernance](/images/2-limit-region/0020.png?featherlight=false&width=90pc)

5. Click vào menu Region kế bên tên user login.
    + Click vào Region mà chúng ta đã cho phép thao tác của testuser trong policy **RegionRestrict**.

![CostGovernance](/images/2-limit-region/0021.png?featherlight=false&width=90pc)

{{% notice tip %}}
Bạn vừa thực hiện thao tác chuyển đổi Region. Sau khi chuyển đổi Region, các tài nguyên bạn tạo ra sẽ nằm trong Region bạn đang sử dụng.
{{% /notice %}}

6. Click vào ô tìm kiếm, click **EC2** để chuyển đến giao diện quản lý của dịch vụ EC2.

![CostGovernance](/images/2-limit-region/0022.png?featherlight=false&width=90pc)

7. Click **Launch instance**, sau đó click **Launch instance**.

![CostGovernance](/images/2-limit-region/0023.png?featherlight=false&width=90pc)

8. Tại **Name** điền **testserver**

![CostGovernance](/images/2-limit-region/0024.png?featherlight=false&width=90pc)

9. Tại **Key pair name**, click vào ô **Select**.
    + Chọn **Proceed without a key pair (Not recommended)


![CostGovernance](/images/2-limit-region/0025.png?featherlight=false&width=90pc)

{{% notice tip %}}
Chúng ta sẽ cần **key pair** để có thể thực hiện kết nối tới EC2 instance. Trong bài lab này chúng ta chỉ muốn kiểm tra quyền thao tác trên dịch vụ nên sẽ không cần kết nối tới EC2 instance.
{{% /notice %}}

10. Click **Launch Instance**.

![CostGovernance](/images/2-limit-region/0026.png?featherlight=false&width=90pc)

Trong bước này, chúng ta đã tạo thành công 1 EC2 instance với instance type là **t2.micro** trong Region Singapore.Tiếp theo chúng ta thử chuyển sang Region khác để kiểm tra xem chúng ta có quyền tạo máy chủ ở Region khác hay không.

![CostGovernance](/images/2-limit-region/0027.png?featherlight=false&width=90pc)

#### Thử tạo máy chủ ở Region khác

1. Click vào menu Region kế bên tên user login.
    + Click vào Region **khác với Region mà chúng ta đã cho phép** thao tác của testuser trong policy **RegionRestrict**.


![CostGovernance](/images/2-limit-region/0028.png?featherlight=false&width=90pc)


2. Thử các thao tác thiết lập Key pair hoặc instance type.
    + Bạn sẽ thấy là bạn không có quyền để tạo EC2 instance trên Region này.

![CostGovernance](/images/2-limit-region/0029.png?featherlight=false&width=90pc)

3. Quay trở về Region ban đầu trước khi thực hiện bước tiếp theo.

![CostGovernance](/images/2-limit-region/0030.png?featherlight=false&width=90pc)

#### Xoá máy chủ testserver đã tạo

1. Kiểm tra bạn đang ở đúng Region ban đầu.
    + Click **Instances**.

![CostGovernance](/images/2-limit-region/0031.png?featherlight=false&width=90pc)

2. Tại danh sách EC2 instance.
    + Click chọn **testserver**.

![CostGovernance](/images/2-limit-region/0032.png?featherlight=false&width=90pc)

3. Click **Instance state**.
    + Click **Terminate instance** để tiến hành xoá máy chủ ảo **testserver**.

![CostGovernance](/images/2-limit-region/0033.png?featherlight=false&width=90pc)

4. Click **Terminate** để xác nhận.
5. Đảm bảo bạn xoá instance thành công, tránh để phát sinh chi phí ngoài mong muốn.

![CostGovernance](/images/2-limit-region/0034.png?featherlight=false&width=90pc)

----

Trong bước này, chúng ta đã tạo thành công 1 EC2 instance với instance type là **t2.micro** trong Region Singapore. Trong phần sau chúng ta sẽ thử hạn chế việc tạo một instance type chỉ định nhé.

![CostGovernance](/images/2-limit-region/0027.png?featherlight=false&width=90pc)