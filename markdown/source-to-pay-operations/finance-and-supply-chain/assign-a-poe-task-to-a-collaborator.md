---
title: Create and assign a purchase order exception task
description: Create a task associated with a purchase order exception and assign it to an operational buyer or collaborator. You can track the task status from the purchase order exception.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/finance-and-supply-chain/assign-a-poe-task-to-a-collaborator.html
release: australia
product: Finance and Supply Chain
classification: finance-and-supply-chain
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resolving purchase order exceptions, Use, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Create and assign a purchase order exception task

Create a task associated with a purchase order exception and assign it to an operational buyer or collaborator. You can track the task status from the purchase order exception.

## Before you begin

Role required: sn\_poem\_core.operational\_buyer

## Procedure

1.  Navigate to **Workspaces** &gt; **Source-to-Pay Workspace**.

2.  Select the **Purchase order management** tab.

3.  Select an exception that you want to work on.

4.  From the **Address exception** list, select **Assign task**.

    \[Omitted image "pom-create-poe-task.png"\] Alt text: Assigning a purchase order exception task

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Assign to|Name of the buyer or collaborator.|
    |Sub type|Type of task being assigned.|
    |Action type for task|Action to be performed for the task.|
    |Priority|Urgency level assigned to the task.|
    |Short description|Short description of the task.|

    \[Omitted image "pom-poe-create-task-modal.png"\] Alt text: Creating a new purchase order exception task and assigning to a collaborator

6.  Select **Create**.

    A purchase order exception task record is created.

7.  Update the record if needed and select **Submit task**.

    **Note:**

    To activate the **Submit task** button, complete the **Action type**, **Sub type**, and **Assign to** fields, then save your changes.


## Result

The task is assigned to the assignee. You can't make any changes to the record until the assignee completes the task.

**Parent Topic:**[Resolving purchase order exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/finance-and-supply-chain/resolving-purchase-order-exceptions.md)

