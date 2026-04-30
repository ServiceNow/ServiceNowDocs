---
title: Configure and perform life-cycle operations on discovered resources
description: Configure life-cycle operations on cloud resources that are not provisioned using ServiceNow Cloud Provisioning and Governance. Provision resources and modify resource block operations to perform day-2 operations on cloud resources that are discovered using Cloud Discovery but not provisioned using Cloud Provisioning and Governance.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Configure and perform life-cycle operations on discovered resources

Configure life-cycle operations on cloud resources that are not provisioned using ServiceNow® Cloud Provisioning and Governance. Provision resources and modify resource block operations to perform day-2 operations on cloud resources that are discovered using Cloud Discovery but not provisioned using Cloud Provisioning and Governance.

## Before you begin

-   Assign the configuration item \(CI\) to a user who performs the operation.
-   Role required: sn\_cmp.cloud\_service\_user, root\_admin, admin, or sn\_cmp.cloud\_admin

## About this task

If a resource is provisioned from the Cloud Provisioning and Governance catalog, you can perform base system life-cycle operations on a stack or on a resource. However, if a resource is discovered as part of Cloud Discovery and is not provisioned from Cloud Provisioning and Governance, the same Start/Stop, Deprovision operations are not available, by default. The following procedure is applicable for a Stop operation on a virtual machine that is not provisioned from Cloud Provisioning and Governance.

## Procedure

1.  Navigate to **All** &gt; **Cloud Admin Portal** &gt; **Design** &gt; **Resource Blocks**.

2.  Search and open the resource/CI you want to perform life-cycle operations on.

3.  Set toggle switch to **Draft**, to make the resource block editable.

4.  In the selected **Resource Block** &gt; **Operations** tab, select the required **Interface** and **Operation** from their respective lists.

    **Note:** The **Interface** and **Operations** fields are only available for resources that are discovered but not added or generated to catalog.

5.  Click the **Override Operation** icon.

6.  In the **Override Operation** dialog, specify a name for the Interface-operation.

    The **Create New** check box is selected, by default.

7.  Click **Submit**.

    You have enabled the selected operation for the interface you created.

8.  In the **Input Parameters** form, click the **Add Input Parameters** icon.

9.  Specify `resourceID` as the parameter **Name** and click **Save**.

    By default, a system assigned expression is generated and appears in the **Mapping** field.

10. For the `ServerID` parameter, replace the default expression in the **Mapping** field with `${parameter.resourceId}` and click **Save**.

11. Navigate to **Operations** &gt; **Steps** subtab.

12. In the **Input** form, change the `NodeId` parameter value to `${parameter.resourceId}`.

13. Navigate back to the **Input Parameters** form, and click **Generate Catalog**.

14. Set toggle switch to **Published**, to publish the resource block again.

    You have configured the resource operation for the specific resource/CI.

15. Navigate to **Cloud User Portal** &gt; **Resources** &gt; **Virtual Machine Instance**, and select the virtual machine instance for which you created the resource operation.

16. Select the new interface operation you created from the **Select Resource Operations** list.


## What to do next

Navigate to the **Cloud User Portal** &gt; **Resources** &gt; **Virtual Machine Instance** and select the new interface operation you created from the **Select Resource Operations** list.

