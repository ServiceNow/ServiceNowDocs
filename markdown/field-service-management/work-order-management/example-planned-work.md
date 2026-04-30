---
title: Work plan example
description: You can create a work plan to define a maintenance schedule for multiple assets based on their installation date.To schedule a warranty maintenance for assets based on their installation date, define a general plan by applying filtering conditions to the assets table, \[alm\_assets\] to identify the matching record of assets require maintenance.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a work order for the planned work, Manage work orders, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Work plan example

You can create a work plan to define a maintenance schedule for multiple assets based on their installation date.

The following image illustrates the maintenance plan for two assets installed on different dates.

![Calendar view of a fifteen-year maintenance plan for installing multiple assets. Maintenance is planned every two years on the same date.](../image/planned-work-example.png)

For example, A hospital has two MRI machines installed on different dates and hence follows a different life cycle. Create a flexible work plan for 15 years to provide the maintenance service to these assets at the following intervals based on their installation date:

-   Perform the first two warranty maintenance at the interval of 365 days from the date of installation.
-   After the first two warranty maintenance are over, perform maintenance every two years for the next eight years.
-   After ten years, perform maintenance every year.

**Parent Topic:**[Create a work order for the planned work](../concept/creating-work-orders-from-planned-work.md)

## Define a maintenance schedule for multiple assets

To schedule a warranty maintenance for assets based on their installation date, define a general plan by applying filtering conditions to the assets table, \[alm\_assets\] to identify the matching record of assets require maintenance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Planned Work Management** &gt; **Plans**.

2.  Click **New** and create a work plan.

    -   **Name**: Hospital device maintenance plan
    -   **Type**: general
    -   **Table**: alm\_asset
    -   **Filter condition**: active is true
3.  Click **Submit**.

    The work plan is created successfully and applied to the matching records from the \[alm\_asset\] table.

4.  Configure multiple schedules for the work plan.

5.  <table id="table_uh3_2hw_h5b"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Create first schedule

</td><td>

1.  In the Planned Work Schedules related list, click **New**.
2.  Enter the following values in the fields.
    -   **Name**: Warranty maintenance
    -   **Trigger**: Duration
    -   **Trigger type**: Interval
    -   **Repeat**: 365 days
    -   **Start planned schedule based on**: field value
    -   **Effective start\_reference**: Installed
    -   **End planned schedule based on**: Frequency
    -   **Frequency**: 2
3.  Click **Submit**.


</td></tr><tr><td>

Create second schedule

</td><td>

1.  In the Planned Work Schedules related list, click **New**.
2.  Enter the following values in the fields.
    -   **Name**: Schedule for 2-8 years
    -   **Trigger**: Duration
    -   **Trigger type**: Annually
    -   **Annually type**: Fixed
    -   **Repeat every**: 2
    -   **Start planned schedule based on**: Schedule
    -   **Schedule**: Warranty maintenance
    -   **End planned schedule based on**: Frequency
    -   **Frequency**: 4
3.  Click **Submit**.


</td></tr><tr><td>

Create third schedule

</td><td>

1.  In the Planned Work Schedules related list, click **New**.
2.  Enter the following values in the fields.
    -   **Name**: Schedule for remaining years
    -   **Trigger**: Duration
    -   **Trigger type**: Annually
    -   **Annually type**: Fixed
    -   **Repeat every**: 1
    -   **Start planned schedule based on**: Schedule
    -   **Schedule**: Schedule for 2-8 years
    -   **End planned schedule based on**: Frequency
    -   **Frequency**: 5
3.  Click **Submit**.


</td></tr></tbody>
</table>6.  Complete the remaining configurations.

    For more information, see [Associate a work order template to a work schedule](../task/associate-work-schedule-to-wotemplate.md) and [Create planned work records](../task/create-planned-work-records.md).

7.  Create work orders for the planed work.

    For more information, see [Create a work order for the planned work](../concept/creating-work-orders-from-planned-work.md).


### Result

The Hospital device maintenance plan schedules all assets for maintenance based on their installation date as mentioned in the [15 years Maintenance Plan](example-planned-work.md#) image.

