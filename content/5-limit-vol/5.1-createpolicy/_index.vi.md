+++
title = "Tạo policy giới hạn"
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++

#### Tạo policy giới hạn sử dụng tài nguyên theo EBS volume type

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
            "Sid": "VisualEditor0",
            "Effect": "Deny",
            "Action": "ec2:*",
            "Resource": "*",
            "Condition": {
                "StringEquals": {
                    "ec2:VolumeType": "io1"
                }
            }
        }
    ]
}
```
    + Click **Next: Tags**.

![CostGovernance](/images/5-limit-vol/0001.png?featherlight=false&width=90pc)

4. Click **Next: Review**.
5. Tại **Name** điền **EC2EBS_Restrict**.
     + Tại **Description** điền **Dont allow EBS io1 volumes**.
     + Click **Create policy**.

![CostGovernance](/images/5-limit-vol/0002.png?featherlight=false&width=90pc)

Bước tiếp theo, chúng ta sẽ gán policy vào **CostTest** group và sau đó kiểm tra hiệu quả của policy này nhé.