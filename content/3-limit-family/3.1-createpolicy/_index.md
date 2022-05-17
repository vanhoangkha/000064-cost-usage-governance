+++
title = "Create restriction policy"
weight = 1
chapter = false
pre = "<b>3.1 </b>"
+++

#### Create a policy to limit resource usage according to the EC2 family

1. Sign out and log in again with an IAM user with admin rights.

2. Go to [IAM service administration interface](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
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
5. At **Name** enter **EC2_FamilyRestrict**.
     + At **Description** enter **Restrict to t3 families**.
     + Click **Create policy**.

![CostGovernance](/images/3-limit-family/0003.png?featherlight=false&width=90pc)

In the next step, we will assign the policy to the **CostTest** group and then test the effectiveness of this policy.