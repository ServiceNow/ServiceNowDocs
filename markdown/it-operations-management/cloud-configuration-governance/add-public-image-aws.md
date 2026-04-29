---
title: Add an AWS public image to Cloud Provisioning and Governance
description: You can make any AWS image selectable in an OS profile.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add an AWS public image to Cloud Provisioning and Governance

You can make any AWS image selectable in an OS profile.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the AWS console, select the EC2 service and then click **IMAGES** &gt; **AMIs**.

    ![AWS console](../image/public-image-aws.png)

2.  Filter the list of images and then take note of the **AMI Name** and **AMI ID** values for the image of interest.

3.  On the instance, enter `cmdb_ci_os_template.list` in the **Filter navigator** text box to open the Images \[cmdb\_ci\_os\_template\] table and then click **New**.

4.  On the **Image** form, enter the following values:

    |Field|Value|
    |-----|-----|
    |Object ID|**AMI ID** value from AWS.|
    |Name|Meaningful name that is based on the **AMI Name** value from AWS.|
    |Guest OS|Operating system.|

5.  On the **Credentials** field, click the magnifying glass and then click **New** on the Credentials page.

6.  In the list, click **Basic Auth Credentials**.

7.  On the Basic Auth Credentials form, enter a meaningful **Name** for the credential.

8.  Enter a **User name** to use for instances that are provisioned from this image.

    AWS uses SSH keys, so a password is not required.

    **Note:** If the name `ec2-user` or `root` does not work, check with your AMI provider.

    |Type|Name|
    |----|----|
    |Amazon Linux|`ec2-user`|
    |RHEL|`ec2-user` or `root`|
    |Ubuntu|`ubuntu` or `root`|
    |Centos|`centos`|
    |Fedora|`ec2-user`|
    |SUSE|`ec2-user` or `root`|

9.  Click **Submit** to close the Basic Auth Credentials form.

10. Right-click in the header and select **Save** to save the current configuration of the new image record.

    In the Related Items list, you can see that the image is associated with the specified datacenter.

11. Click **Update** to make the public image selectable in an OS profile.

    This step also creates a relationship between the public image and the logical datacenter \(LDC\) in the CMDB.


**Parent Topic:**[Resource Profiles](../concept/cloud-resource-profiles.md)

