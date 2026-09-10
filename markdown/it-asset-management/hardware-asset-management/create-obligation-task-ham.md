---
title: Create an ad hoc obligation task in Hardware Asset Workspace
description: Create an ad hoc obligation task required only once or at irregular intervals to track and fulfill an obligation specified in a contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/create-obligation-task-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 1
breadcrumb: [Create an obligation record, Manage obligations, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Create an ad hoc obligation task in Hardware Asset Workspace

Create an ad hoc obligation task required only once or at irregular intervals to track and fulfill an obligation specified in a contract.

## Before you begin

Role required: sn\_cm\_obligation.obligation\_fulfiller

## Procedure

1.  Open an active obligation record.

<table id="choicetable_a12_4dt_3kc"><thead><tr><th align="left" id="d333223e62">

Hardware Asset Workspace view

</th><th align="left" id="d333223e67">

Steps

</th></tr></thead><tbody><tr><td id="d333223e73">

**Contract management**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Contract management**.
2.  Select the **All contracts** tab.
3.  Select an active contract record.

**Note:** Obligation is associated with the following contract types:

    -   Leases
    -   Warranties
    -   Maintenance
    -   Purchasing agreements
4.  Select the **Obligations** tab.
5.  Select an active obligation record.


</td></tr><tr><td id="d333223e134">

**Asset operations**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.
2.  From the Contracts list, select **Obligations**.
3.  Select an active obligation record.


</td></tr></tbody>
</table>2.  Select the **Obligation tasks** tab.

3.  Select **New**.

4.  On the New obligation task form, fill in the required details.

    1.  In the **Assigned to** field, update the assigned user.

    2.  In the Schedule section, select the task completion date in the **Due date** field.

    3.  Select **Save**.


## Result

-   An obligation task record is created and listed in the **Obligations tasks** tab.

    **Note:** The obligation task record is saved in the Obligation Tasks \[sn\_cm\_obligation\_obligation\_task\] table.

-   The obligation task also appears under **Contracts** &gt; **Obligations tasks** in the Asset Operations view.
-   The system notifies the assigned user through email.

**Parent Topic:**[Create an obligation record in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-obligation-records-ham.md)

**Related topics**  


[Create obligations manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-work-on-ob-tasks.md)

[Approve or reject obligation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-manage-ob-tasks.md)

[Cancel an obligation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cancel-ob-task.md)

