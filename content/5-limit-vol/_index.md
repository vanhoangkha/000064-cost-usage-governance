+++
title = "Limited by EBS volume"
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

#### Create a limit policy ( policy ) according to EBS volume type.

**Elastic Block Store (EBS)** is a service that provides storage infrastructure for EC2. We can choose from many different types of storage depending on the purpose of use. Managing the type of usable storage is also important in managing costs.
In this step we will create an IAM policy that does not allow the use of the **Provision IOPS (io1)** volume type. **Provision IOPS (io1)** is a volume class that provides high performance and is intended for mission-critical applications.

#### Content

- [Create restriction policy](5.1-createpolicy/)
- [Assign policy to group](5.2-attachpolicy/)
- [Check policy effectiveness](5.3-testpolicy/)