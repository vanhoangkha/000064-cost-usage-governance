+++
title = "Create restriction policy"
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++

#### Create policy to limit resource usage according to EBS volume type

1. Signout and login again with IAM user with admin rights.

2. Go to [IAM service management console](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
    + Click **Policies**.
    + Click **Create Policy**.
 
![CostGovernance](/images/3-limit-family/0001.png?featherlight=false&width=90pc)

3. At the **Create policy** page.
    + Click **JSON** tab.
    + Copy the policy below.

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
5. At **Name** enter **EC2_FamilyRestrict**.
     + At **Description** enter **Dont allow EBS io1 volumes**.
     + Click **Create policy**.

![CostGovernance](/images/5-limit-vol/0002.png?featherlight=false&width=90pc)

In the next step, we will assign the policy to the **CostTest** group and then test the effectiveness of this policy.