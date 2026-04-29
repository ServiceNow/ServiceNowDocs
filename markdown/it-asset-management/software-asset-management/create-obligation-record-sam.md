---
title: Create an obligation record in the Software Asset Workspace
description: Create obligation records for signed contracts in Software Asset Workspace to fulfill the responsibilities specified in the contract through obligation tasks.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [obligation in software asset workspace, obligation record]
breadcrumb: [Manage obligation tasks in the Software Asset Workspace, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create an obligation record in the Software Asset Workspace

Create obligation records for signed contracts in Software Asset Workspace to fulfill the responsibilities specified in the contract through obligation tasks.

## Before you begin

The contract record must be in the **Activate** state.

Role required: sn\_cm\_obligation.obligation\_fulfiller

## About this task

Recurring obligation tasks are automatically created from the obligation record. You can also add ad hoc obligation tasks that are performed only once or at irregular intervals. For more information about creating adhoc obligation task, see [Create an ad hoc obligation task in Software Asset Workspace](create-adhoc-obligation-task-sam.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select **Software contracts**.

3.  Select the active contract record.

4.  Select the **Obligations** tab.

5.  Select **New**.

6.  On the form, fill in the fields.

    For a description of the field values, see [Obligation form](https://www.servicenow.com/docs/access?context=cncore-obligation-form&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

7.  Select **Save**.


## Result

-   An obligation record is created for the contract and listed in the **Obligations** tab.
-   The obligation record is saved in the Obligations \[sn\_cm\_obligation\_obligation\] table.

## What to do next

View the obligation record by navigating to any of the following paths:

-   Navigate to the **Obligations** tab within the software contract record.
-   Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Obligations**.

**Parent Topic:**[Manage obligation tasks in the Software Asset Workspace](../concept/manage-obligation-tasks-software-asset-workspace.md)

**Related topics**  


[Create an ad hoc obligation task in Software Asset Workspace](create-adhoc-obligation-task-sam.md)

[Manage obligation tasks in the Software Asset Workspace](../concept/manage-obligation-tasks-software-asset-workspace.md)

[Use Software Asset Management with Contract Management Pro](../concept/sam-integration-cmpro.md)

[Create an ad hoc obligation task in Software Asset Workspace](create-adhoc-obligation-task-sam.md)

