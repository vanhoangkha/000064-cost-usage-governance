+++
title = "Tạo policy giới hạn"
weight = 1
chapter = false
pre = "<b>3.1 </b>"
+++

#### Tạo policy giới hạn sử dụng tài nguyên theo EC2 family

1. Signout và đăng nhập lại bằng IAM user có quyền admin.

2. Truy cập vào [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
    + Click **Policies**.
    + Click **Create Policy**.
 
![CostGovernance](/images/3-limit-family/0001.png?featherlight=false&width=90pc)

3. Tại trang **Create policy**.
    + Click **JSON** tab.
    + Copy đoạn policy dưới đây vào.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "ec2:*",
            "Resource": "*",
            "Condition": {
                "ForAllValues:StringLike": {
                    "ec2:InstanceType": [
                        "t3.*"
                    ]
                }
            }
        }
    ]
}
```
    + Click **Next: Tags**.

![CostGovernance](/images/3-limit-family/0002.png?featherlight=false&width=90pc)

4. Click **Next: Review**.
5. Tại **Name** điền **EC2_FamilyRestrict**.
     + Tại **Description** điền **Restrict to t3 families**.
     + Click **Create policy**.

![CostGovernance](/images/3-limit-family/0003.png?featherlight=false&width=90pc)

Bước tiếp theo, chúng ta sẽ gán policy vào **CostTest** group và sau đó kiểm tra hiệu quả của policy này nhé.