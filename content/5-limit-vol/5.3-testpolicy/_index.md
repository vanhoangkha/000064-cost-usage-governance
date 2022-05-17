+++
title = "Validate policy effectiveness"
weight = 3
chapter = false
pre = "<b>5.3 </b>"
+++

#### Validate the effectiveness of the policy by creating an EC2 instance with a volume type of io1

1. Click on the name of the currently logged-in user.
   + Click **Sign out**.

2. Click **Log back in**

![CostGovernance](/images/2-limit-region/0018.png?featherlight=false&width=90pc)

3. At **IAM user name** enter the user we created (**testuser**).
   + At **Password** enter the password we have set up (**Testuser123**).
   + Click **Sign in**.

![CostGovernance](/images/2-limit-region/0019.png?featherlight=false&width=90pc)

{{% notice tip %}}
If you failed to log in, please check the user and password information created in the previous steps. Also, make sure you use the correct AWS account ID when logging in.
{{% /notice %}}

4. Click the search box, and click **EC2** to go to the management interface of the EC2 service.


5. Click **Launch instance**, then click **Launch instance**.

![CostGovernance](/images/2-limit-region/0023.png?featherlight=false&width=90pc)

6. At **Name** enter **testserver**

![CostGovernance](/images/2-limit-region/0024.png?featherlight=false&width=90pc)

7. Scroll down, click on instance type **t2.micro**.

![CostGovernance](/images/3-limit-family/0009.png?featherlight=false&width=90pc)

8. In the search box, enter **t3**.
   + Click to select instance type **t3.nano**.

![CostGovernance](/images/4-limit-size/0007.png?featherlight=false&width=90pc)

9. At **Key pair name**, click in the **Select** box.
   + Select **Proceed without a key pair (Not recommended)

![CostGovernance](/images/2-limit-region/0025.png?featherlight=false&width=90pc)


{{% notice tip %}}
We will need **key pair** to be able to make a connection to the EC2 instance. In this lab, we just want to check the service permissions so we won't need to connect to the EC2 instance.
{{% /notice %}}

10. Scroll down to **Configure storage**.
    + Click **Add new volume**.

![CostGovernance](/images/5-limit-vol/0004.png?featherlight=false&width=90pc)

11. Click **gp3**.
    + Click **Provisioned IOPS SSD (io1)** to change the volume type to **io1**.
    + Click **Launch instance**.

![CostGovernance](/images/5-limit-vol/0005.png?featherlight=false&width=90pc)

12. We will see that launching an instance with volume type **io1** will fail.
![CostGovernance](/images/5-limit-vol/0006.png?featherlight=false&width=90pc)


#### Try creating a server with volume type gp3

1. Click **Edit instance config**.

![CostGovernance](/images/5-limit-vol/0007.png?featherlight=false&width=90pc)


2. Scroll down, click **io1**.
    + Click **General purpose SSD(gp3)** to convert the volume type to **gp3**.
    + Click **Launch instance**.

![CostGovernance](/images/5-limit-vol/0008.png?featherlight=false&width=90pc)


3. So we have successfully created EC2 instance with instance type **t3.nano** and volume type **gp3**.

![CostGovernance](/images/5-limit-vol/0009.png?featherlight=false&width=90pc)

#### Delete the created testserver

1. Click **View all instances**.

![CostGovernance](/images/5-limit-vol/0010.png?featherlight=false&width=90pc)


2. At the list of EC2 instances.
     + Click to select **testserver**.

3. Click **Instance state**.
     + Click **Terminate instance** to proceed to delete the virtual server **testserver**.
     + Click **Terminate** to confirm.
  
4. Make sure you delete the instance successfully, avoiding unexpected costs.

![CostGovernance](/images/5-limit-vol/0011.png?featherlight=false&width=90pc)

----

In this step, we have successfully created 1 EC2 instance with instance type of **t3.nano** and volume type of **gp3** (forbid users from creating volume type of **io1**). The next step is to clean up resources.