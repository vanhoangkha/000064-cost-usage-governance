+++
title = "Validate policy effectiveness"
weight = 2
chapter = false
pre = "<b>4.2 </b>"
+++

#### Validate the effectiveness of the policy by creating another EC2 instance t3.nano
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

7. At **Key pair name**, click in **Select** box.
  + Select **Proceed without a key pair (Not recommended)


![CostGovernance](/images/2-limit-region/0025.png?featherlight=false&width=90pc)

{{% notice tip %}}
We will need **key pair** to be able to make a connection to the EC2 instance. In this lab, we just want to check the service permissions so we won't need to connect to the EC2 instance.
{{% /notice %}}

7. Scroll down, and click on instance type **t2.micro**.

![CostGovernance](/images/3-limit-family/0009.png?featherlight=false&width=90pc)

8. In the search box, enter **t3**.
  + Click to select instance type **t3.micro**.

![CostGovernance](/images/3-limit-family/0010.png?featherlight=false&width=90pc)

9. Check **Instance type** has changed to **t3.micro**.
  + Click **Launch instance**.


![CostGovernance](/images/2-limit-region/0026.png?featherlight=false&width=90pc)

{{% notice tip %}}
In this step, we tried to create 1 EC2 instance with instance type **t3.micro** and this EC2 instance creation failed because we only have permission to create instances that belong to the T3 family and have nano size. ( **t3.nano** )
{{% /notice %}}


![CostGovernance](/images/4-limit-size/0005.png?featherlight=false&width=90pc)

#### Try creating a server with T3 family and size nano (t3.nano)

1. Click **Edit instance config**.

![CostGovernance](/images/4-limit-size/0006.png?featherlight=false&width=90pc)

2. Scroll down, click on instance type **t3.micro**.

3. In the search box, enter **t3**.
   + Click to select instance type **t3.nano**.

![CostGovernance](/images/4-limit-size/0007.png?featherlight=false&width=90pc)

4. Check **Instance type** has changed to **t3.nano**.
   + Click **Launch instance**.

![CostGovernance](/images/4-limit-size/0008.png?featherlight=false&width=90pc)
5. So we have successfully created EC2 instance with instance type **t3.nano**.

![CostGovernance](/images/4-limit-size/0009.png?featherlight=false&width=90pc)

#### Delete the created testserver
1. Click **View all instances**.

![CostGovernance](/images/4-limit-size/0010.png?featherlight=false&width=90pc)

2. At the list of EC2 instances.
   + Click to select **testserver**.

3. Click **Instance state**.
   + Click **Terminate instance** to proceed to delete the virtual server **testserver**.
   + Click **Terminate** to confirm.
  
4. Make sure you delete the instance successfully, avoiding unexpected costs.


![CostGovernance](/images/4-limit-size/0011.png?featherlight=false&width=90pc)

----

In this step, we have successfully created an EC2 instance with instance type **t3.nano**. In the next section, we will try to limit the creation of an instance with an EBS volume type of **io1**.