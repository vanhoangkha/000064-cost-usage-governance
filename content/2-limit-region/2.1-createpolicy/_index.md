+++
title = "Create restriction policy"
weight = 1
chapter = false
pre = "<b>2.1 </b>"
+++

#### Create policy to limit resource usage by Region

1. After creating user successfully. In the left hand menu, click **Policies**.

![CostGovernance](/images/2-limit-region/0001.png?featherlight=false&width=90pc)

2. At the **Policies** page.
   + Click **Create Policy**.

 
![CostGovernance](/images/2-limit-region/0002.png?featherlight=false&width=90pc)

3. At the **Create policy** page.
   + Click tab **JSON**.

  
![CostGovernance](/images/2-limit-region/0003.png?featherlight=false&width=90pc)

4. Copy and Paste the policy content below.

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
You can change the Region information in the above policy to suit the Region to which you want to authorize EC2, RDS and S3 services.
{{% /notice %}}

5. Click **Next: Tags**.

![CostGovernance](/images/2-limit-region/0005.png?featherlight=false&width=90pc)

6. Click **Next: Review**.

![CostGovernance](/images/2-limit-region/0006.png?featherlight=false&width=90pc)

7. At **Review policy** page.
   + Set **Name** as **RegionRestrict**.
   + Set **Description*** to **EC2, RDS, S3 access in a single Region only**.
   + Click **Create policy**.

![CostGovernance](/images/2-limit-region/0007.png?featherlight=false&width=90pc)

8. Make sure the **RegionRestrict** policy is created successfully.

![CostGovernance](/images/2-limit-region/0008.png?featherlight=false&width=90pc)

In the next step, we will assign the policy to the **CostTest** group and then test the effectiveness of this policy.