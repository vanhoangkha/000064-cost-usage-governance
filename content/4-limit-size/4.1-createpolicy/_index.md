+++
title = "Update restriction policy"
weight = 1
chapter = false
pre = "<b>4.1 </b>"
+++

#### Update policy to limit resource usage according to EC2 instance size

1. Sign out and log in again with an IAM user with admin rights.

2. Go to [IAM service administration interface](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
   + Click **Policies**.
   + In the search box, enter **EC2_FamilyRestrict**.
   + Press the **Enter** key.
 
![CostGovernance](/images/4-limit-size/0001.png?featherlight=false&width=90pc)

3. Click policy **EC2_FamilyRestrict**.

![CostGovernance](/images/4-limit-size/0002.png?featherlight=false&width=90pc)

4. Click **Edit policy**.

![CostGovernance](/images/4-limit-size/0003.png?featherlight=false&width=90pc)

5. Copy the policy below instead.
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

In this step, we have specified that we can only create instances with family and size as **t3.nano**. In the next step, we will test the effectiveness of this policy.