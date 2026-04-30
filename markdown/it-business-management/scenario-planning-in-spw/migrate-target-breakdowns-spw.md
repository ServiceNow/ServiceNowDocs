---
title: Migrate target breakdowns
description: After upgrading to Strategic Planning v4.3.2 or later, run the Migrate BreakdownInterval To Checkinfrequency scheduled job to migrate the existing values from the Review frequency field to the Check-in frequency field in the target records.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Migrate target breakdowns

After upgrading to Strategic Planning v4.3.2 or later, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job to migrate the existing values from the **Review frequency** field to the **Check-in frequency** field in the target records.

## About this task

After running the job, the value in the **Check-in frequency** field for a target is populated based on the existing value in the **Review frequency** field of the target. If the existing value in the **Review frequency** field was set to any option other than **None**, then target breakdowns will be created for such targets based on the value in the existing check-in frequency of the target. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](../concept/target-breakdowns-migration-spw.md).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and select the **Migrate BreakdownInterval To Checkinfrequency** scheduled job.

3.  On the Scheduled Script Execution form, ensure that the frequency is selected as **On Demand** in the **Run** field.

4.  Select **Execute Now**.


-   **[Target breakdowns migration](../concept/target-breakdowns-migration-spw.md)**  
As an administrator, when you run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job, the existing values in the **Review frequency** and **Breakdown interval** fields are migrated to the **Check-in frequency** field in the target records.

**Parent Topic:**[Configuring goals in Strategic Planning](../concept/configuring-goal-framework-apw.md)

