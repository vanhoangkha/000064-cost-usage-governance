
+++
title = "Limit by Region"
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

#### Create a policy to limit service usage by Region

To manage costs, you need to manage and control your usage. AWS provides multiple Regions, so depend on your requirements, you can limit access to AWS services depending on the Region.

This can be used to ensure that usage is only allowed in specific areas more cost-effectively and to reduce usage and associated costs, such as data transmission costs.

We will create a policy that allows all EC2, RDS, and S3 access in only a single Region.

{{% notice tip %}}
It is best practice to provide only the minimum necessary access, the policy used here is short and simple and should only be used for the lab before being deleted.
{{% /notice %}}


#### Content

- [Create restriction policy](2.1-createpolicy/)
- [Assign policy to group](2.2-attachpolicy/)
- [Validate policy effectiveness](2.3-testpolicy/)