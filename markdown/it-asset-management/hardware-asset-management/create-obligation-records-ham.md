---
title: Create an obligation record in the Hardware Asset Workspace
description: Create an obligation record for signed contracts in the Hardware Asset Workspace to fulfill the responsibilities specified in the contract through obligation tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/create-obligation-records-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 1
breadcrumb: [Manage obligations, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Create an obligation record in the Hardware Asset Workspace

Create an obligation record for signed contracts in the Hardware Asset Workspace to fulfill the responsibilities specified in the contract through obligation tasks.

## Before you begin

The contract record must be in the **Active** state.

Role required: sn\_cm\_obligation.obligation\_fulfiller

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Contract management**.

2.  Select the tab for the contract type for which you want to create an obligation.

    -   **Leases**
    -   **Maintenance**
    -   **Warranties**
    -   **Purchasing agreements**
3.  Select the active contract record.

4.  Select the **Obligations** tab.

5.  Select **New**.

6.  On the form, fill in the fields.

    For a description of the field values, see [Obligation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-obligation-form.md).

7.  Select **Save**.


## Result

-   An obligation record is created for the contract and listed in the **Obligations** tab.

    **Note:** The obligation record is saved in the Obligations \[sn\_cm\_obligation\_obligation\] table.

-   The obligation record also appears under **Contracts** &gt; **Obligations** in the Asset Operations view.

## What to do next

Create an obligation task for the obligation record. For details, see [Create an ad hoc obligation task in Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-obligation-task-ham.md).

-   **[Create an ad hoc obligation task in Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-obligation-task-ham.md)**  
Create an ad hoc obligation task required only once or at irregular intervals to track and fulfill an obligation specified in a contract.

**Parent Topic:**[Manage obligations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-obligations-in-ham.md)

**Related topics**  


[Create obligations manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-work-on-ob-tasks.md)

[Approve or reject obligation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-manage-ob-tasks.md)

[Cancel an obligation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cancel-ob-task.md)

