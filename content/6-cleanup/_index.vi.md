+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

Chúng ta sẽ tiến hành xóa các tài nguyên theo thứ tự sau 

#### Xoá IAM Policy RegionRestrict

1. Sign out và đăng nhập lại với user có quyền admin.

2. Truy cập vào [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
    + Click **Policies**.

3. Tại ô tìm kiếm, điền **RegionRestrict**. 
    + Ấn **Enter**.

4. Click chọn policy **RegionRestrict**. 
    + Click **Actions**.
    + Click **Delete**.

![CostGovernance](/images/6-cleanup/0001.png?featherlight=false&width=90pc)

5. Điền **RegionRestrict** để xác nhận xoá policy.
    + Click **Delete**.
    
![CostGovernance](/images/6-cleanup/0002.png?featherlight=false&width=90pc)

#### Xoá IAM Policy EC2EBS_Restrict

1. Click biếu tưởng **X** để xoá Filter.

2. Tại ô tìm kiếm, điền **EC2EBS_Restrict**
    + Ấn **Enter**.

3. Click chọn policy **EC2EBS_Restrict**
    + Click **Actions**.
    + Click **Delete**.

4. Điền **EC2EBS_Restrict** để xác nhận xoá policy.
    + Click **Delete**.

#### Xoá IAM Policy EC2_FamilyRestrict

1. Click biếu tưởng **X** để xoá Filter.
  
2. Tại ô tìm kiếm, điền **EC2_FamilyRestrict**
    + Ấn **Enter**.

3. Click chọn policy **EC2_FamilyRestrict**
    + Click **Actions**.
    + Click **Delete**.

4. Điền **EC2_FamilyRestrict** để xác nhận xoá policy.
    + Click **Delete**.


#### Xoá IAM user testuser
1. Click **Users**.
    + Click chọn **testuser**.
    + Click **Delete**.

![CostGovernance](/images/6-cleanup/0004.png?featherlight=false&width=90pc)

2. Điền **testuser** để xác nhận.
    + Click **Delete**.

#### Xoá IAM group CostTest

1. Click **User groups**.
    + Click chọn **CostTest** group.
    + Click **Delete**.

![CostGovernance](/images/6-cleanup/0005.png?featherlight=false&width=90pc)

2. Điền **CostTest** để xác nhận.
    + Click **Delete**.
