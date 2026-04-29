---
title: Amazon Web Services EC2 Linux Out Of Box permissions
description: Amazon Web Services EC2 Linux OOB catalog items permissions
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services EC2 Linux Out Of Box Catalog items, Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Amazon Web Services EC2 Linux Out Of Box permissions

Amazon Web Services EC2 Linux OOB catalog items permissions

<table id="table_bsw_xy2_hzb"><thead><tr><th>

Catalog item

</th><th>

Services

</th><th>

Permissions

</th></tr></thead><tbody><tr><td rowspan="5">

CSC AWS EC2 Linux VM

</td><td>

AWS EC2 provision

</td><td>

1.  DescribeVolumes
2.  DescribeImages
3.  DescribeInstances
4.  DescribeVolumes
5.  DescribeInstanceCreditSpecifications
6.  DescribeInstanceAttribute
7.  DescribeInstances
8.  DescribeTags
9.  DescribeInstanceTypes
10. DescribeInstances
11. DescribeVpcs
12. RunInstances
13. DescribeImages
14. GetCallerIdentity

</td></tr><tr><td>

AWS EC2 instance- stop

</td><td>

1.  DescribeInstances
2.  StopInstances

</td></tr><tr><td>

AWS EC2 instance- start

</td><td>

1.  DescribeImages
2.  DescribeInstances
3.  StartInstances

</td></tr><tr><td>

AWS EC2 instance- deprovision vm **Note:** This de-provisions storage volume as well.

</td><td>

1.  DescribeAddresses
2.  TerminateInstances

</td></tr><tr><td>

AWS EC2 instance- deprovision stack**Note:** Terminates everything including nic.

</td><td>

1.  GetCallerIdentity
2.  DescribeInstances
3.  DescribeImages

</td></tr><tr><td rowspan="4">

CSC AWS EC2 Linux multiple disks

</td><td>

AWS EC2 Linux multiple disks provision

</td><td>

1.  DescribeVolumes
2.  DescribeImages
3.  DescribeInstances
4.  AttachVolume
5.  DescribeInstances
6.  CreateVolume
7.  DescribeInstanceCreditSpecifications
8.  DescribeInstanceAttribute DescribeVpcs
9.  DescribeInstanceTypes
10. DescribeTags RunInstances
11. GetCallerIdentity

</td></tr><tr><td>

AWS EC2 Linux multiple disks stop

</td><td>

1.  DescribeInstances
2.  StopInstances

</td></tr><tr><td>

AWS EC2 Linux multiple disks start

</td><td>

1.  DescribeImages
2.  DescribeInstances
3.  StartInstances

</td></tr><tr><td>

AWS EC2 Linux multiple disks stack deprovision- terminates all resources

</td><td>

1.  DescribeInstances
2.  TerminateInstances
3.  ModifyInstanceAttribute
4.  DescribeVolumes
5.  DeleteVolume
6.  GetCallerIdentity
7.  DetachVolume
8.  DescribeInstanceCreditSpecifications
9.  DescribeVpcs
10. DescribeInstanceTypes
11. DescribeTags
12. DescribeImages

</td></tr><tr><td rowspan="4">

CSC AWS EC2 Linux with security groups

</td><td>

AWS EC2 Linux with security groups- provision

</td><td>

1.  DescribeVolumes
2.  DescribeImages
3.  DescribeInstances
4.  DescribeInstanceCreditSpecifications
5.  DescribeInstanceAttribute
6.  DescribeVolumes
7.  DescribeTags
8.  DescribeVpcs
9.  DescribeInstanceTypes
10. RunInstances
11. GetCallerIdentity

</td></tr><tr><td>

AWS EC2 Linux with security groups stop

</td><td>

1.  DescribeInstances
2.  StopInstances

</td></tr><tr><td>

AWS EC2 Linux with security groups start

</td><td>

1.  DescribeInstances
2.  DescribeImages
3.  StartInstances

</td></tr><tr><td>

AWS EC2 Linux with security groups stack deprovision- terminate all resources

</td><td>

1.  DescribeInstances
2.  TerminateInstances
3.  ModifyInstanceAttribute
4.  GetCallerIdentity
5.  DescribeInstanceCreditSpecifications
6.  DescribeInstanceAttribute
7.  DescribeVolumes
8.  DescribeTags
9.  DescribeInstanceTypes
10. DescribeVpcs
11. DescribeImages

</td></tr></tbody>
</table>**Parent Topic:**[Amazon Web Services EC2 Linux Out Of Box Catalog items](aws-ec2-linux-oob-catalogs.md)

