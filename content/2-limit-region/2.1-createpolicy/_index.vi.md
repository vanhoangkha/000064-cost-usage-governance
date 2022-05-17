+++
title = "Tạo policy giới hạn"
weight = 1
chapter = false
pre = "<b>2.1 </b>"
+++

#### Tạo policy giới hạn sử dụng tài nguyên theo Region

1. Sau khi tạo user thành công. Tại menu bên tay trái, click **Policies**.

![CostGovernance](/images/2-limit-region/0001.png?featherlight=false&width=90pc)

2. Tại trang **Policies**. 
   + Click **Create Policy**.

 
![CostGovernance](/images/2-limit-region/0002.png?featherlight=false&width=90pc)

3. Tại trang **Create policy**.
   + Click tab **JSON**.

  
![CostGovernance](/images/2-limit-region/0003.png?featherlight=false&width=90pc)

4. Copy và Paste nội dung policy dưới đây.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "ec2:*",
                "rds:*",
                "s3:*"
            ],
            "Resource": "*",
    "Condition": {"StringEquals": {"aws:RequestedRegion": "ap-southeast-1"}}
        }
    ]
}
```

![CostGovernance](/images/2-limit-region/0004.png?featherlight=false&width=90pc)

{{% notice info %}}
Bạn có thể thay đổi thông tin Region ở policy trên cho phù hợp với Region mà bạn muốn cấp quyền các dịch vụ EC2, RDS và S3.
{{% /notice %}}

5. Click **Next: Tags**.

![CostGovernance](/images/2-limit-region/0005.png?featherlight=false&width=90pc)

6. Click **Next: Review**.

![CostGovernance](/images/2-limit-region/0006.png?featherlight=false&width=90pc)

7. Tại trang **Review policy**.
   + Đặt **Name** là **RegionRestrict**.
   + Đặt **Description*** là **EC2, RDS, S3 access in a single Region only**.
   + Click **Create policy**.

![CostGovernance](/images/2-limit-region/0007.png?featherlight=false&width=90pc)

8. Đảm bảo policy **RegionRestrict** được tạo thành công.

![CostGovernance](/images/2-limit-region/0008.png?featherlight=false&width=90pc)

Bước tiếp theo, chúng ta sẽ gán policy vào **CostTest** group và sau đó kiểm tra hiệu quả của policy này nhé.