---
title: Run scheduled job to refresh maintenance plans
description: Run the job Update planned work records on Demand to refresh the planned work records of a maintenance plan on demand or regularly at scheduled intervals.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-10-13"
reading_time_minutes: 1
breadcrumb: [Manage a work order for the planned work, Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Run scheduled job to refresh maintenance plans

Run the job **Update planned work records on Demand** to refresh the planned work records of a maintenance plan on demand or regularly at scheduled intervals.

## Before you begin

Role required: admin

## About this task

The **Update planned work records on Demand** job refreshes the planned work records associated with a maintenance plan. The job updates, deletes, or creates new planned work records as needed. This ensures that all planned work records accurately reflect the current configuration of the maintenance plan.

Planned work records are not refreshed automatically when changes are made to a maintenance plan. After modifying any attribute or filter condition, you must manually run the **Update planned work records on Demand** job for the planned work records to reflect the latest updates.

For example, if you have a maintenance plan for printers filtered by manufacturer \(e.g., "Manufacturer is Canon"\), and you change the filter condition to include a specific model number or ID, the planned work records shown in the Planned Work Records tab will only update after the job is run.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Schedule Jobs**.

2.  In the **Search** field, enter **Update planned work records on Demand**.

3.  Select **Update planned work records on Demand**.

4.  Select **Active** check box.

5.  To specify a different schedule for running the job, change the **Run** and **Time** fields.

6.  Click **Update**.

7.  At any time, to run the scheduled job, click **Execute Now**.


## Result

The planned work records for the maintenance plan are refreshed.

