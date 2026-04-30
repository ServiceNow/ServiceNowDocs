---
title: Migrate target breakdowns
description: After upgrading to Goal Framework for SPM v2.3.0 or later, run the Migrate BreakdownInterval To Checkinfrequency scheduled job to migrate the existing values from the Review frequency field to the Check-in frequency field in the target records.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2024-10-22"
reading_time_minutes: 1
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Migrate target breakdowns

After upgrading to Goal Framework for SPM v2.3.0 or later, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job to migrate the existing values from the **Review frequency** field to the **Check-in frequency** field in the target records.

## About this task

After running the job, the value in the **Check-in frequency** field for a target is populated based on the existing value in the **Review frequency** field of the target. If the existing value in the **Review frequency** field was set to any option other than **None**, then target breakdowns will be created for such targets based on the value in the existing check-in frequency of the target. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](../concept/target-breakdowns-migration.md).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and select the **Migrate BreakdownInterval To Checkinfrequency** scheduled job.

3.  On the Scheduled Script Execution form, ensure that the frequency is selected as **On Demand** in the **Run** field.

4.  Select **Execute Now**.


-   **[Target breakdowns migration](../concept/target-breakdowns-migration.md)**  
As an administrator, when you run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job, the existing values in the **Review frequency** and **Breakdown interval** fields are migrated to the **Check-in frequency** field in the target records.

**Parent Topic:**[Configuring Goal Framework and Goal Framework for SPM](../concept/configuring-goal-framework.md)

