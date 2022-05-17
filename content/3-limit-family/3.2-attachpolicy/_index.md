+++
title = "Assign policy to group"
weight = 2
chapter = false
pre = "<b>3.2 </b>"
+++

#### Assign policy to group **CostTest**

1. After creating the policy successfully. In the left-hand menu, click **User groups**.
    + Click on **CostTest** group.

![CostGovernance](/images/3-limit-family/0004.png?featherlight=false&width=90pc)

3. On the group page **CostTest**.
    + Click the **Permissions** tab.
    + Click **Add permissions**.
    + Click **Attach policies**.

4. In the Filter box, click **Type**.

![CostGovernance](/images/2-limit-region/0012.png?featherlight=false&width=90pc)

5. Click **Type: Customer managed**.

![CostGovernance](/images/2-limit-region/0013.png?featherlight=false&width=90pc)


{{% notice tip %}}
Customer managed are the IAM Policies we create and manage ourselves.
{{% /notice %}}

6. Click the Filter box, enter the name of the policy we created in the previous step ( **EC2_FamilyRestrict** ).
    + Press the **Enter** key.

7. Click the checkbox next to **EC2_FamilyRestrict** policy.
    + Click **Add permissions**.

![CostGovernance](/images/3-limit-family/0005.png?featherlight=false&width=90pc)

8. Make sure the policy is successfully assigned.

![CostGovernance](/images/2-limit-region/0016.png?featherlight=false&width=90pc)

9. Click **RegionRestrict** policy.
     + Click **Remove**.

![CostGovernance](/images/3-limit-family/0006.png?featherlight=false&width=90pc)

{{% notice tip %}}
We need to remove the **RegionRestrict** policy because this policy provides full permissions on the EC2 service.
{{% /notice %}}

Next step, we will log in with user **testuser** to check if we can create an EC2 server with a family other than T3.