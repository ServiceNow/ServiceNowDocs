---
title: Add an Azure public image to Cloud Provisioning and Governance
description: You can make any Azure image selectable in an OS profile.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add an Azure public image to Cloud Provisioning and Governance

You can make any Azure image selectable in an OS profile.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the Azure command-line interface \(CLI\), make note of the values of the **Offer**, **Publisher**, **Sku**, and **Version**.

    On the command line, you can search by offer or by publisher or by both, as shown in the example. Each line item is an image of a particular version of CentOS from OpenLogic.

    You can use the following sample command on the CLI - `az vm image list -f Windows --output table` to fetch the values.

    ![Command-line interface](../image/public-image-azure.png)

2.  On the instance, enter `cmdb_ci_os_template.list` in the **Filter navigator** text box to open the Images \[cmdb\_ci\_os\_template\] table and then click **New**.

3.  Configure the form layout to show **Offer**, **Serial number**, **Version**, and **Vendor**.

4.  On the Image form, enter the following values:

<table id="table_hpm_hk3_qcb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Object ID

</td><td>

Enter `/publisher/offer/sku/version`. You can get these values from the Azure CLI. As an example, `/OpenLogic/CentOS/6.5/6.5.201501`.

</td></tr><tr><td>

Name

</td><td>

Meaningful name that represents the version of the OS. `CentOS 6.5` in the example.

</td></tr><tr><td>

Guest OS

</td><td>

Operating system.

</td></tr><tr><td>

Offer

</td><td>

**Offer** value from Azure.

</td></tr><tr><td>

Serial Number

</td><td>

**Sku** value from Azure.

</td></tr><tr><td>

Version

</td><td>

**Version** value from Azure.

</td></tr><tr><td>

Vendor

</td><td>

1.  Click the magnifying glass and then click **New**.
2.  In the **Name** field, enter the **Publisher** value from Azure.
3.  Click **Submit**.


</td></tr></tbody>
</table>5.  On the **Credentials** field, click the magnifying glass and then click **New** on the Credentials page.

6.  In the list, click **Basic Auth Credentials**.

7.  On the Basic Auth Credentials form, enter a meaningful **Name** for the credential.

8.  Enter a **User name** and **Password** to use for instances that are provisioned from this image.

9.  Click **Submit** to close the Basic Auth Credentials form.

10. Right-click in the header and select **Save** to save the current configuration of the new image record.

    In the Related Items list, you can see that the image is associated with the specified datacenter.

11. Click **Update** to make the public image selectable in an OS profile.

    This step also creates a relationship between the public image and the logical datacenter \(LDC\) in the CMDB.


**Parent Topic:**[Resource Profiles](../concept/cloud-resource-profiles.md)

