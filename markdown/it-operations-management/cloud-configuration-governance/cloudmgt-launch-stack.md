---
title: Launch a stack
description: Launch a stack of cloud resources to submit a request for an item in the service catalog. You can launch a stack from the Cloud User Portal overview page.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Launch a stack

Launch a stack of cloud resources to submit a request for an item in the service catalog. You can launch a stack from the Cloud User Portal overview page.

## Before you begin

Role required: sn\_cmp.cloud\_service\_user

When you submit a request for an item in the service catalog, the system typically provisions the stack immediately. Sometimes, your request must be approved first.

If a resource on a stack requires credentials when being accessed via SSH, then you must create an SSH key pair before you can launch the stack. See [Create an SSH key](cloudmgt-create-ssh-key.md) and [Download an SSH key](cloudmgt-download-ssh-key.md).

## Procedure

1.  Open the request form using either of the following methods:

    -   On the overview page, click **Launch a Stack**. By default, all catalog items in all service categories are listed. Select a **Service Category**, and then click a catalog item **Name**.
    -   Open the **Catalog** page. By default, all catalog items in all service categories are listed. Select a **Service Category** and then click **Launch** on the catalog item.
2.  In each section of the form, enter the values that configure your request.

    The form fields differ for each catalog offering. Contact your Cloud Provisioning and Governance administrator if you have any questions about the fields.

    **Important:** When you select a user group on the form, the quota limits for you and the user group \(that you are part of\) are shown in the Quota section.

    The following sub-steps are applicable only if you are using the Terraform connector and Terraform config installables.

    1.  On the General Info section, select **Yes** for the **UseExistingWorkspace** option, to use existing workspaces that are already discovered.

    2.  Select the Workspace where your config installable resides, from the **Workspace** list.

    **Note:** If you are configuring a Windows VM, set the **IncludeManagementKey** field to **No**. After the VM is provisioned, you can use the day-2 operation called InfuseKey to add key credentials \(**UserName** and **Password** values\) to the VM.

3.  On the General Info section, select the Agent pool you have created in your Terraform Enterprise organization to communicate with private or on-premise infrastructure.

    **Note:** Agent pool selection is applicable only to VMware via Terraform Enterprise setups for provisioning. You need to have created agent pools in your Terraform Enterprise organization and have VMware-Terraform Enterprise templates in your workspaces for the agent pools option to appear on the GUI.

4.  Click the section header to move to the next section.

    The remaining quota is updated based on the user group that you select. For required fields, the system selects the first item in the list by default and you can select any value that you need.

5.  Click **Submit** to request the stack.

    -   The **Activities** page opens to the **Status** tab on the **Track** &gt; **Requests** activity. The tab displays the progress and status of the request. The following color codes show the stage of the request:
    -   -   Green: Completed or Approved.
-   Orange: Processing.
-   Red: Rejected, Error, or Canceled.
    -   If approval is required, then after the administrator approves your request, the system launches the stack and updates the **Request Status**.
    -   If the quota limit exceeds for you or your user group, then an error message appears or the system triggers a policy-based approval. For more information about the quota limits, see [Viewing resource quota limits](../concept/resource-quota.md).
    -   Select another request to view its **Request Status** and **Stack Status**.
    -   To view a summary of all your pending requests, click the **Pending Requests** link in the title bar at any time.
    ![Activities tab in the Cloud User Portal.](../image/activities.png)


