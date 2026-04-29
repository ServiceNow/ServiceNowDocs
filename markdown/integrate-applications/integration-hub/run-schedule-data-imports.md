---
title: Run or schedule a data import
description: Specify when to run a data import by creating a schedule. Schedule an import to run at a specific time, at regular intervals, or after a parent import. You can also run your import immediately.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub - Import, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Run or schedule a data import

Specify when to run a data import by creating a schedule. Schedule an import to run at a specific time, at regular intervals, or after a parent import. You can also run your import immediately.

## Before you begin

[Configure a data source](configure-data-source.md), then [Map source data to a target table](map-source-data-target.md).

Role required: admin or ih\_import.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **IntegrationHub - Import**.

2.  On the landing page, select your integration.

3.  On the left navigation panel, click **Schedule imports**.

4.  On the Run and schedule imports page, click **Schedule an import**.

5.  On the New schedule form, fill in the fields.

<table id="table_sjb_jk2_lpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td class="sub-head" colspan="2">

Scheduled Data Import

</td></tr><tr><td>

Name

</td><td>

Name to uniquely identify the import schedule.

</td></tr><tr><td>

Data source

</td><td>

Data source for the import. This field is automatically set to the name of your integration.

</td></tr><tr><td>

Run as

</td><td>

Name of the user or user role the import executes with. For example, the import may run as the System Administrator, or it may run with the roles of a specified user.

</td></tr><tr><td>

Application

</td><td>

Application scope for the import schedule.

</td></tr><tr><td>

Run

</td><td>

Option to specify when the import runs. Select one of the following.-   **Daily**: Runs every day.
-   **Weekly**: Runs every week.
-   **Monthly**: Runs every month.
-   **Periodically**: Runs at regular intervals.
-   **After Parent Runs**: Runs after another import.


</td></tr><tr><td>

Day

</td><td>

Day of the week or month to run the import. Entered as a number. This field appears only when **Weekly** or **Monthly** is selected from **Run**.

</td></tr><tr><td>

Repeat interval

</td><td>

Amount of time to wait between imports. Entered in days, hours, minutes, and seconds. This field appears only when **Periodically** is selected from **Run**.

</td></tr><tr><td>

Parent

</td><td>

Name of the parent import. The parent import must finish before the current import begins. This field appears only when **After Parent Runs** is selected from **Run**.

</td></tr><tr><td>

Time

</td><td>

Time of day to run the import. Entered in hours, minutes, and seconds.

</td></tr><tr><td>

Active

</td><td>

Option to make the import schedule active.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td>

Concurrent import

</td><td>

Option to divide the data into multiple import sets and process them concurrently.

</td></tr><tr><td>

Partition Method

</td><td>

Option to specify how to partition the data. Select one of the following.-   **Custom size**
-   **Round Robin**
This field appears only when **Concurrent import** is selected.

</td></tr><tr><td>

Partition Size

</td><td>

Number of records for the partition size. Must be greater than or equal to 1000. This field appears only when **Custom size** is selected from **Partition Method**.

</td></tr></tbody>
</table>6.  Click **Save**.

7.  To add a prescript or postscript, click the more options icon \(![More options icon](../images/more-options-icon.png)\) and select **Advanced setup**.

    This option opens the form for the scheduled data import, where you can add a script to run before or after your import.

8.  Run your scheduled import right away by clicking the **Run Import** button, and refresh the Executions list to view the execution record.


## What to do next

Your import will run at the scheduled time. After it runs, an Executions section appears on the Run and schedule imports page. The Execution section has execution records where you can view details about your import, including its runtime, the number of imported rows, and any errors or log messages.

**Parent Topic:**[Integration Hub - Import](../concept/integrationhub-imports.md)

