---
title: Run a scheduled job to execute a planned work schedule
description: Planned work schedules are implemented regularly using the Planned Maintenance Nightly Run scheduled job. Planned work schedules are executed whenever it's meter, duration, script, or condition criteria meets.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Generate work orders, Work plans, Planned Work Management, Work orders and tasks, Configure, Field Service Management]
---

# Run a scheduled job to execute a planned work schedule

Planned work schedules are implemented regularly using the **Planned Maintenance Nightly Run** scheduled job. Planned work schedules are executed whenever it's meter, duration, script, or condition criteria meets.

## Before you begin

Role required: admin

## About this task

The **Planned Maintenance Nightly Run** scheduled job runs at the specified time to evaluate all the schedule occurrences associated with a schedule of the work plan. For each schedule, work orders are generated for all records that meet the conditions specified in the schedule \(including all records for the current day\).

The timing of work order creation is controlled using **Lead Time** and **Days in Future to Create Work Orders** values. The work orders are generated if the following conditions are met:

-   The **Earliest Start Date** of the schedule occurrence is earlier than the end of the day the job runs.
-   The current date \(the day on which the job runs\) is later than or same as the date calculated by the formula `Requested Due By date – Lead Time – Days in Future`.
-   The state of any associated schedule occurrence is **Pending**.
-   No suppression is applied on the schedule occurrences associated with the schedule.

This ensures that work orders are created neither too early nor too late, and become available at the right time for planning and execution.

For example, consider the job is scheduled to run at 12.00 AM on 12 March, 2026. The job evaluates if the **Earliest Start Date** of the schedule occurrence is earlier than 11 March 2026. The work orders are generated as shown on the below mentioned table.

|Schedule occurrence|Earliest start date|Is work order generated?|
|-------------------|-------------------|------------------------|
|Schedule Occurrence 1|8 March, 20206|Yes|
|Schedule Occurrence 2|15 March, 2026|No|
|Schedule Occurrence 3|At 10 PM on 11 March, 2026|Yes|

**Note:**

-   The work orders are generated only for the next immediate implementation.
-   You can generate the work orders manually as well for a schedule occurrence. This creates the work orders only for that specific schedule occurrence. For more information, see [Generate work orders for schedule occurrences](create_wo_schedule_occurrence.md)

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Schedule Jobs**.

2.  In the **Search** field, enter **Planned Maintenance Nightly Run**.

3.  Select **Planned Maintenance Nightly Run**.

4.  To specify a different schedule for running the job, change the **Run** and **Time** fields.

    A scheduled job does not run based on the value set in the Next run time field in the maintenance plan record for this job. For more information, see [Configure a work schedule](configure-work-plan.md).

    **Note:**

    -   If you select the time zone, the job runs at the specified time in the selected time zone.
    -   If you don't specify the time zone, the job runs at the specified time in your time zone.
    -   If you select **Use System Time Zone**, the job runs at the set time in the instance's time zone.
5.  Click **Update**.

6.  At any time, to run the scheduled job, click **Execute Now**.

    **Note:**

    The scheduled job evaluates all previously defined schedules and executes the ones that are scheduled to run.

    If one or more records in the table associated with the work plan are deleted after the matching records were associated with the work plan, the next nightly run removes all the records associated with those removed assets.


## Result

Work orders for the existing schedule occurrences are generated and the next schedule occurrences are created.

