---
title: Close an asset reclamation request
description: Close an asset reclamation request to efficiently reclaim software assets when an employee leaves an organization or moves to a different role.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create a catalog request to reclaim assets, Setting up Software Asset Management, Software Asset Management, IT Asset Management]
---

# Close an asset reclamation request

Close an asset reclamation request to efficiently reclaim software assets when an employee leaves an organization or moves to a different role.

## Before you begin

Role required: sam\_user or asset.

## Procedure

1.  Navigate to **Inventory** &gt; **Asset Reclamation** &gt; **Asset Reclamation Requests**.

2.  Open the request that you want to fulfill.

    In the Software Asset Reclamation Lines related list, a device reclamation line item is created for each device that is returned, has a corresponding CI record, has software installations on it, and that device was selected in the Reclaim Asset form. For example, if five computers were assigned to an employee, then for each computer a separate device reclamation line item is created.

    An extra user reclamation line item is created if the **Employee Separation** check box was selected in the Reclaim Asset form.

3.  Click the device reclamation line item.

    The Software Asset Reclamation Line page opens, where a software asset reclamation task titled **Receive, evaluate and update asset** is created.

4.  Click the **Receive, evaluate, and update** task.

    The Software Asset Reclamation Task page opens. You now need to manually receive the asset, evaluate if the asset can be redeployed or reused, and then update the asset.

5.  Select values for the **Assignment group** and **Assigned to** fields.

6.  Click **Close Task** once you have completed all the tasks.

    The line item state now changes to **Closed Complete**

    For each software asset reclamation line item where the type is device reclamation, perform steps 3 to 6.

    **Note:** Once you receive the asset from the employee, navigate to the Asset page and change the values for the **State** and **Assigned to** fields. Since the asset is no longer assigned to a user, ensure that the **Assigned to** field is empty and the **State** field is not in the **In use** status.

    If the asset that was updated has device allocations, then a software asset reclamation line task titled **Remove device license allocations** is created. All the device allocations records on that Asset \(CI\) are removed, and the task is marked as **Closed complete**.

    If the asset that was updated has software install records, then a software asset reclamation line task titled **Remove software installs** is created. All the software install records on that Asset \(CI\) are removed, and the task is marked as **Closed complete**.

    Once all the device reclamation tasks are complete and if a user reclamation line item is not created, then the status of the catalog request changes to **Complete**. However, if a user reclamation task is created, then you need to take care of the following steps to complete and close the user reclamation line item.

    **Note:** A user reclamation task is created if the **Employee Separation** check box was selected in the Reclaim Asset form.

    A user reclamation workflow is initiated once the reclaimed date mentioned in the Asset Reclamation Request form has lapsed. A user license allocation task titled **Revoke user license allocations** is automatically created to remove all user license allocations. A few manual tasks are also created that need to be completed.

7.  Complete the following manual user reclamation tasks:

    -   Revoke SSO access \(if the employee had any SSO provider plugin enabled\)
    -   Revoke Citrix access \(if the employee had the Citrix plugin enabled\)
    -   Revoke SAP access \(if SAP publisher pack plugin was enabled\)
    -   Revoke user subscriptions. Open the task and ensure that removal candidate records are created for each user subscription record.
8.  Once all the user reclamation tasks are closed, the status of the catalog request changes to **complete**.


**Parent Topic:**[Create a catalog request to reclaim assets](create-catalog-req-offboardingsam.md)

