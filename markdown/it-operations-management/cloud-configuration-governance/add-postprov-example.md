---
title: Add post-provisioning to a Cloud Formation Template-based catalog item
description: Create a workflow post-provisioning operation on a Cloud Formation Template \(CFT\)-based catalog item.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create post-provision operations, Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add post-provisioning to a Cloud Formation Template-based catalog item

Create a workflow post-provisioning operation on a Cloud Formation Template \(CFT\)-based catalog item.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer.

## About this task

In this example, create a key pair at the AWS console, then select the appropriate credentials, discover cloud accounts, create a CFT-based catalog item, add a workflow post provisioning operation to the catalog item, and lastly provision the catalog item.

Ensure that you've met the following prerequisites before you start working on this example:

-   The Cloud Provisioning and Governance plugin is activated.
-   AWS Credentials and Service Account are set up.
-   The Cloud Account for AWS Logical Data Center is created.
-   The Key pair is configured on AWS and is available in CMP as “cmdb\_ci\_cloud\_key\_pair”.
-   A workflow is available on an instance. This example uses the `SSH_Workflow_New` workflow.
-   A script include to fetch the private and public IP is available.

## Procedure

1.  At the AWS console, create a new key pair.

    Give the key pair a name, for example, `ItappWOP`.

    When you create a key pair, a PEM file is automatically downloaded onto your system.

2.  Open the PEM file and copy all the contents of the file.

3.  Navigate to the Credentials application using the filter navigator in your instance.

4.  Click **New** and then select **SSH Private Key Credentials**.

5.  In the **Name** field, enter a name \(`Itappwop`\) .

6.  In the **SSH Private Key** field, paste the contents of the PEM file.

7.  In the **Credential alias** field, enter an alias name \(`Itappwop`\).

    The Alias name must be the same name that you entered in the **Name** field.

8.  Click **Submit**.

9.  To discover cloud accounts to sync data from AWS, run ServiceNow® Discovery.

10. Create a cloud catalog item based on AWS CFT to provision a stack.

    1.  Navigate to **Cloud Admin Portal** &gt; **Design** &gt; **Cloud Catalog items**

    2.  Click **New**.

        The Cloud Catalog Item screen appears.

11. Enter a unique name for the catalog item in the **Name** field, select **Cloud Template** in the **Source** field and **Cloud Formation Template** in **Template type** field.

12. Click **Submit**.

    The catalog item is generated.

13. Create a cloud template and associate the template with the catalog item.

    1.  Navigate to **Cloud Admin Portal** &gt; **Design** &gt; **Cloud Catalog Items**.

    2.  Open the catalog item record that you want to create a cloud template for and click **Cloud Templates** &gt; **New**.

        The Cloud Template Versions screen appears.

    3.  In the Ingestion Method list, select **Use template body** and paste the contents of the AWS CFT in the **Body** field.

    4.  Click **Save**.

        All variables extracted from the AWS CFT appear in the Template Version Parameters section.

        ![Template parameters](../image/template-param-example.png)

    5.  Click **Activate**.

        The catalog item is generated.

14. Go to the Cloud User Portal and open the catalog item that you just generated.

    On the **Provision** tab, you can see all variables extracted from the template. You can add a workflow post provision operation to the catalog item.

15. Navigate to **Cloud Admin Portal** &gt; **Design** &gt; **Cloud Catalog Items**.

16. Open the catalog item record that you want to create the workflow post provisioning operation for.

17. Click the **Post Provisioning Operation** subtab and then click **New**.

    The Operation Step screen appears.

18. Select **Workflow** in the **Setup Type** list and select **SSH\_Workflow\_New** in the **Flow** list.

19. Click **Submit**.

    Parameters for the workflow operation are automatically created as operation attributes in the Manage Attributes screen.

20. Click **Manage Attributes**.

    The **Manage Attributes** screen appears.

21. Click **Provision EC2 Instance with SSH Script.Post Provision**.

22. Click the **key\_name** attribute and enter either the Credential alias value \(`Itappwop`\), or enter an expression mapping in the **Mapping** field.

    Mappings specify where to pull the information in the system. See [Using expressions in Cloud Provisioning and Governance](../reference/expressions-cloud-mgt.md).

23. Click the **Stack ID** attribute and enter the expression mapping `$(context.order.stack)`.

24. Click **Apply Changes**.

    Workflow is mapped as a post provision operation to the catalog item that you generated.

25. Provision the CFT-based catalog item in the Cloud User Portal.

    1.  Navigate to **Cloud User Portal** and click **Launch a Stack**.

    2.  Open the catalog item that you want to provision and enter values in all the mandatory fields on the **General Info** and **Provision** tabs.

26. To provision the catalog item, click **Submit**.

27. Validate the provisioned catalog item upon completion.


