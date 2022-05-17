+++
title = "Create IAM user"
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

#### Create IAM group

1. After creating the group successfully, at the menu on the left-hand side.
    + Click **Users**.

![CostGovernance](/images/1-preparation/0006.png?featherlight=false&width=90pc)

2. At the **Users** page.
    + Click **Add users**.

![CostGovernance](/images/1-preparation/0007.png?featherlight=false&width=90pc)

3. At the **Add user** page.
    + Set **User name** as **testuser**.
    + Click **Password - AWS Management Console access** to let the user login to the management console.
    + Click **Custom password** to set a custom password.
    + Set password as **Testuser123**.
    + Uncheck **User must create a new password at next sign-in**.
    + Click **Next:Permissions**.

![CostGovernance](/images/1-preparation/0008.png?featherlight=false&width=90pc)

4. Click **CostTest** group, then click **Next: Tags**.

![CostGovernance](/images/1-preparation/0009.png?featherlight=false&width=90pc)

5. Click **Next: Review**.

![CostGovernance](/images/1-preparation/0010.png?featherlight=false&width=90pc)

6. Check the information, click **Create user**.

![CostGovernance](/images/1-preparation/0011.png?featherlight=false&width=90pc)

7. Make sure the user created successfully. Click **Close**.

![CostGovernance](/images/1-preparation/0012.png?featherlight=false&width=90pc)

We have finished preparing the IAM user and group. Next, we will proceed to decentralize to limit resource usage by Region.