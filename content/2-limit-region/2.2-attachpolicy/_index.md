+++
title = "Assign policy to group"
weight = 2
chapter = false
pre = "<b>2.2 </b>"
+++

#### Assign policy to group **CostTest**

1. After creating the policy successfully. In the left-hand menu, click **User groups**.

![CostGovernance](/images/2-limit-region/0009.png?featherlight=false&width=90pc)

2. Click on the **CostTest** group.

![CostGovernance](/images/2-limit-region/0010.png?featherlight=false&width=90pc)

3. On the group page **CostTest**.
    + Click the **Permissions** tab.
    + Click **Add permissions**.
    + Click **Attach policies**.

![CostGovernance](/images/2-limit-region/0011.png?featherlight=false&width=90pc)

4. In the Filter box, click **Type**.

![CostGovernance](/images/2-limit-region/0012.png?featherlight=false&width=90pc)

5. Click **Type: Customer managed**.

![CostGovernance](/images/2-limit-region/0013.png?featherlight=false&width=90pc)


{{% notice tip %}}
Customer managed are the IAM Policies we create and manage ourselves.
{{% /notice %}}

6. Click the Filter box, and enter the name of the policy we created in the previous step ( **RegionRestrict** ).
    + Press the **Enter** key.

![CostGovernance](/images/2-limit-region/0014.png?featherlight=false&width=90pc)

7. Click the checkbox next to **RegionRestrict** policy.
    + Click **Add permissions**.

![CostGovernance](/images/2-limit-region/0015.png?featherlight=false&width=90pc)

8. Make sure the policy is successfully assigned.

![CostGovernance](/images/2-limit-region/0016.png?featherlight=false&width=90pc)

In the next step, we will log in with the user **testuser** to check the permissions on the Region that we have assigned.