---
title: Mine a project
description: After you’ve configured the data you want to visualize, you can begin mining the project.An analyst, power user, or administrator can cancel a mining job currently in process.When attempting to mine a project, the project workflow record shows one of these states.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a project using Classic view, Using Process Mining, Process Mining, Platform Analytics]
---

# Mine a project

After you’ve configured the data you want to visualize, you can begin mining the project.

## Before you begin

Role required: po\_analyst

## About this task

Process Mining extracts a maximum limit of 500,000 records for a single table. If that limit is reached with the table you selected, add additional filters to refine the data set.

This limit will decrease depending on the number of tables you have configured on your project. For example, if you configure two tables, a parent table \(like Incident\) and a child table \(like Task\_sla\), the limit calculated on the incident table will be 250,000 records.

**Note:**

-   Optimizing a project may take significant time. While extraction is in progress for a project, you cannot explore its process map.
-   During a full or sample mining, Process Mining analyzes the audit log.

## Procedure

1.  From the application navigator, navigate to **Process Mining** &gt; **Process Mining Workspace**.

2.  From the project's card menu, select:

    -   **Mine project \(Full\)** to mine the full project.
    -   **Mine project \(Sample\)** to mine up to 3,600 records, rather than mining all records applicable to a project.

        **Note:** Mining a sample enables an analyst to validate project configuration settings before performing a full data extraction of the project.

3.  Select **OK** to confirm you want to begin mining the project.

4.  Select **Notify once complete** if you want to be added to the watch list.

    You will receive an email notification after the mining is complete. The job limit per day is set to 50 by default. If you exceed the limit, an error message is displayed.

5.  Select **View progress** to see the details of the mining.

    After the mining is complete, a **Mining Summary** page is displayed. This page provides additional details about the mining. It also lists any finding definition that wasn’t included in the mining and provides a link to understand the actual cause. You can also view the logs or go to the Process Mining Workspace and view the graph.

    ![Mining summary](../image/mining-summary.png)


## Result

If the extraction completes successfully, the project card shows the mining state as **Available**.

**Parent Topic:**[Create a project using Classic view](create-proj.md)

## Cancel a mining job

An analyst, power user, or administrator can cancel a mining job currently in process.

### Before you begin

Role required: none

### Procedure

1.  Select **Cancel** during mining of a project to cancel the process.

    It can take several minutes before the cancel process completes. The unit of work in progress at the time of canceling mining must complete before cancellation occurs.

    The mining state on the Project Definition form shows as **Cancelled**.


## Mine states

When attempting to mine a project, the project workflow record shows one of these states.

<table id="table_znt_3ld_tkb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Mining has not been attempted on the project data.

</td></tr><tr><td>

Mining Data

</td><td>

Mining is in process for the project.

</td></tr><tr><td>

Cancelling

</td><td>

Mining is in process of user-initiated cancellation.

</td></tr><tr><td>

Cancelled

</td><td>

A user cancelled mining that was in process for the project.

</td></tr><tr><td>

Available

</td><td>

Mining has been performed on the data and the process map visualization is available to view.

</td></tr><tr><td>

Error

</td><td>

Mining was attempted but did not complete successfully. -   New projects that have not yet been successfully mined cannot be opened in the Analyst Workbench.
-   You can attempt a data refresh from the Analyst Workbench on a project that has been successfully mined from its workflow record. An error icon ![error icon](../image/extract-error-icon.png) displays when project data does not refresh successfully. To investigate for details, view the **Extract Data Log** tab from the Project Definition form.

</td></tr><tr><td>

Scheduled

</td><td>

A job has been scheduled for the project to be mined at a specified time interval. **Note:** If there are several projects scheduled for mining within a job, the projects execute sequentially. For example, a job which has Projects 1 and 2 scheduled within it will mine Project 1 first, then begin mining Project 2 after mining of Project 1 completes.

</td></tr></tbody>
</table>