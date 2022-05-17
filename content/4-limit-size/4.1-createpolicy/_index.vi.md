+++
title = "Cập nhật policy giới hạn"
weight = 1
chapter = false
pre = "<b>4.1 </b>"
+++

#### Cập nhật policy giới hạn sử dụng tài nguyên theo EC2 instance size

1. Signout và đăng nhập lại bằng IAM user có quyền admin.

2. Truy cập vào [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
   + Click **Policies**.
   + Tại ô tìm kiếm, điền **EC2_FamilyRestrict**.
   + Ấn phím **Enter**.
 
![CostGovernance](/images/4-limit-size/0001.png?featherlight=false&width=90pc)

3. Click policy **EC2_FamilyRestrict**.

![CostGovernance](/images/4-limit-size/0002.png?featherlight=false&width=90pc)

4. Click **Edit policy**.

![CostGovernance](/images/4-limit-size/0003.png?featherlight=false&width=90pc)

5. Copy đoạn policy dưới đây để thay thế.
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
                        "t3.nano"
                    ]
                }
            }
        }
    ]
}
```
  + Click **Review policy**.

![CostGovernance](/images/4-limit-size/0004.png?featherlight=false&width=90pc)

6. Click **Save changes**.

Trong bước này chúng ta đã chỉ định rõ chúng ta chỉ có thể tạo instance với family và size là **t3.nano**.Bước tiếp theo, chúng ta sẽ kiểm tra hiệu quả của policy này nhé.