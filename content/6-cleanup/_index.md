+++
title = "Clean up resources"
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

We will proceed to delete the resources in the following order

#### Delete IAM Policy RegionRestrict

1. Sign out and log back in with a user with admin rights.

2. Go to [IAM service administration interface](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)
    + Click **Policies**.

3. In the search box, enter **RegionRestrict**.
    + Press **Enter**.

4. Click the **RegionRestrict** policy.
    + Click **Actions**.
    + Click **Delete**.

![CostGovernance](/images/6-cleanup/0001.png?featherlight=false&width=90pc)

5. Enter **RegionRestrict** to confirm policy deletion.
    + Click **Delete**.
    
![CostGovernance](/images/6-cleanup/0002.png?featherlight=false&width=90pc)

#### Delete IAM Policy EC2EBS_Restrict

1. Click the **X** icon to clear the Filter.

2. In the search box, enter **EC2EBS_Restrict**
    + Press **Enter**.

3. Click the policy **EC2EBS_Restrict**
    + Click **Actions**.
    + Click **Delete**.

4. Enter **EC2EBS_Restrict** to confirm policy deletion.
    + Click **Delete**.

#### Delete IAM Policy EC2_FamilyRestrict

1. Click the **X** icon to clear the Filter.
  
2. In the search box, enter **EC2_FamilyRestrict**
    + Press **Enter**.

3. Click the policy **EC2_FamilyRestrict**
    + Click **Actions**.
    + Click **Delete**.

4. Enter **EC2_FamilyRestrict** to confirm policy deletion.
    + Click **Delete**.


#### Delete IAM user testuser
1. Click **Users**.
    + Click to select **testuser**.
    + Click **Delete**.

![CostGovernance](/images/6-cleanup/0004.png?featherlight=false&width=90pc)

2. Enter **testuser** to confirm.
    + Click **Delete**.

#### Delete IAM group CostTest

1. Click **User groups**.
    + Click on **CostTest** group.
    + Click **Delete**.

![CostGovernance](/images/6-cleanup/0005.png?featherlight=false&width=90pc)

2. Enter **CostTest** to confirm.
    + Click **Delete**.