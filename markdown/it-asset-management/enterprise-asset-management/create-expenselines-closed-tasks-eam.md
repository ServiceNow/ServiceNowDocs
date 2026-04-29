---
title: Create expense lines for closed tasks in Enterprise Asset Workspace
description: Automatically create expense lines for previously closed tasks, that originally had no expense lines, in order to calculate costs for those tasks.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Total Cost of Ownership \(TCO\) for enterprise assets, Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create expense lines for closed tasks in Enterprise Asset Workspace

Automatically create expense lines for previously closed tasks, that originally had no expense lines, in order to calculate costs for those tasks.

## Before you begin

If you haven't used task rate cards, then expense lines do not get created. When you upgrade to Australia, you can automatically create expense lines in bulk for all your closed tasks. This is only a one time process that runs on active task rate cards with a populated task rate value. Using time worked will not result in creation of expense lines if the time worked records are not present for tasks.

**Note:** To use task rate cards, you need to activate the ServiceNow® Cost Management \(com.snc.cost\_management\) plugin.

In order to avoid creation of duplicate expense lines, keep the following factors in mind:

-   Configure the task rate cards.
-   Configure the conditions within each task rate card.
-   Specify the amount you want to use for each task.
-   Do not create duplicate task rate cards where you create multiple task rate cards for the same task and condition.

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **TCO configuration** &gt; **Task rate card**.

2.  Select **Create expense lines for tasks**.

    A confirmation message box opens.

3.  Select **Create expense lines**.

    The background job **Asset Common Expense Lines for Historical tasks** runs only once and looks for closed tasks without any expense lines and creates expense lines for all those closed tasks. Once the expense lines are created, the **Create expense lines for tasks** button is no longer visible.


**Parent Topic:**[Total Cost of Ownership \(TCO\) for enterprise assets](../concept/confifure-eam-asset-tco.md)

