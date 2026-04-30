---
title: Modify marketplace eligibility criteria for Field Service Marketplace
description: Configure the eligibility criteria within task filter settings for Field Service Marketplace.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Marketplace, Configuring contractor capabilities, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Modify marketplace eligibility criteria for Field Service Marketplace

Configure the eligibility criteria within task filter settings for Field Service Marketplace.

## Before you begin

Role required: admin

Ensure that the Field Service Marketplace plugin is active. For more information, see [Activate Field Service Marketplace](activate-contractor-marketplace.md).

**Note:** To utilize automation in Field Service Marketplace, the Dynamic Scheduling plugin must also be installed and the **Use task filters for determining contractor tasks** property must be enabled.

## About this task

Field Service Marketplace comes with the **Marketplace tasks** filter, which determines if work order tasks are eligible for marketplace. This task filter is shipped as demo data with the Field Service Marketplace plugin.

For more information on task filters, see [Create a task filter for dynamic scheduling](create-task-filter.md).

## Procedure

1.  Navigate to **All** &gt; **Outsourced Field Service** &gt; **Eligibility criteria** or **All** &gt; **Marketplace** &gt; **Eligibility criteria**.

2.  Select the task filter you wish to configure.

3.  Modify the following fields as needed:

    -   Eligible for contractor assignment - Determines if this task filter allows for tasks to be assigned to contractors when meeting specified criteria.
    -   Eligible for Marketplace - Determines if this task filter allows for tasks to be assigned to Marketplace when meeting specified criteria.
4.  Modify the **Select Criteria** as needed.

    Select criteria is used to rate contractor groups. The two available select criteria are as follows:

    -   Matching skills of contractors
    -   Distance between task and contractors
5.  Navigate to the Eligible engagement methods related list and set **Auto push** to true for that method if you wish to enable Auto Push for an engagement method, if there are no eligible engagement methods listed, click New to add an engagement method eligible for this task filter.

    **Note:** Only one eligible engagement method can have auto push set to true, and therefore be utilized by the automation flow logic.

6.  Click **Update**.


