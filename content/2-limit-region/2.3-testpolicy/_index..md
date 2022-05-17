+++
title = "Validate policy effectiveness"
weight = 3
chapter = false
pre = "<b>2.3 </b>"
+++

#### Validate the effectiveness of the policy by creating an EC2 instance in the allowed Region

1. Click on the name of the currently logged-in user.
    + Click **Sign out**.

![CostGovernance](/images/2-limit-region/0017.png?featherlight=false&width=90pc)

2. Click **Log back in**

![CostGovernance](/images/2-limit-region/0018.png?featherlight=false&width=90pc)

3. At **IAM user name** enter the user we created (**testuser**).
    + At **Password** enter the password we have set up (**Testuser123**).
    + Click **Sign in**.

![CostGovernance](/images/2-limit-region/0019.png?featherlight=false&width=90pc)

{{% notice tip %}}
If you failed to log in, please check the user and password information created in the previous steps. Also, make sure you use the correct AWS account ID when logging in.
{{% /notice %}}

4. Click **Switch to the new Console Home** to switch to the new interface.

![CostGovernance](/images/2-limit-region/0020.png?featherlight=false&width=90pc)

5. Click on the Region menu next to the login user name.
    + Click on the Region where we have allowed testuser operations in the **RegionRestrict** policy.

![CostGovernance](/images/2-limit-region/0021.png?featherlight=false&width=90pc)

{{% notice tip %}}
You have just performed the Region conversion. After converting Region, the resources you create will be in the Region you are using.
{{% /notice %}}

6. Click the search box, and click **EC2** to go to the management interface of the EC2 service.

![CostGovernance](/images/2-limit-region/0022.png?featherlight=false&width=90pc)

7. Click **Launch instance**, then click **Launch instance**.

![CostGovernance](/images/2-limit-region/0023.png?featherlight=false&width=90pc)

8. At **Name** enter **testserver**

![CostGovernance](/images/2-limit-region/0024.png?featherlight=false&width=90pc)

9. At **Key pair name**, click in the **Select** box.
    + Select **Proceed without a key pair (Not recommended)


![CostGovernance](/images/2-limit-region/0025.png?featherlight=false&width=90pc)

{{% notice tip %}}
We will need **key pair** to be able to make a connection to the EC2 instance. In this lab, we just want to check the service permissions so we won't need to connect to the EC2 instance.
{{% /notice %}}

10. Click **Launch Instance**.

![CostGovernance](/images/2-limit-region/0026.png?featherlight=false&width=90pc)

In this step, we have successfully created 1 EC2 instance with instance type **t2.micro** in Region Singapore. Next, we try to switch to another Region to check if we have permission to create a server in another Region or not.

![CostGovernance](/images/2-limit-region/0027.png?featherlight=false&width=90pc)

#### Try creating a server in another Region

1. Click on the Region menu next to the login user name.
    + Click on the Region **different from the Region that we have allowed** the testuser's operation in the **RegionRestrict** policy.


![CostGovernance](/images/2-limit-region/0028.png?featherlight=false&width=90pc)


2. Try setting Key pair or instance type.
    + You will see that you do not have permission to create EC2 instances on this Region.

![CostGovernance](/images/2-limit-region/0029.png?featherlight=false&width=90pc)

3. Return to the original Region before performing the next step.

![CostGovernance](/images/2-limit-region/0030.png?featherlight=false&width=90pc)

#### Delete the created testserver

1. Check you are in the correct Region initially.
    + Click **Instances**.

![CostGovernance](/images/2-limit-region/0031.png?featherlight=false&width=90pc)

2. At the list of EC2 instances.
    + Click to select **testserver**.

![CostGovernance](/images/2-limit-region/0032.png?featherlight=false&width=90pc)

3. Click **Instance state**.
    + Click **Terminate instance** to proceed to delete the virtual server **testserver**.

![CostGovernance](/images/2-limit-region/0033.png?featherlight=false&width=90pc)

4. Click **Terminate** to confirm.
5. Make sure you delete the instance successfully, avoiding unexpected costs.

![CostGovernance](/images/2-limit-region/0034.png?featherlight=false&width=90pc)

----

In this step, we have successfully created 1 EC2 instance with instance type **t2.micro** in Region Singapore. In the next section we will try to limit the creation of a specific instance