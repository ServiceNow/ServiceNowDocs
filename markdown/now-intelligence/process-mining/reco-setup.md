---
title: Configure recommendations setup
description: Set up recommendations to simplify project creation and get help in the analysis.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [With Process Configuration Builder, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure recommendations setup

Set up recommendations to simplify project creation and get help in the analysis.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the side of the page, select the Process configurations icon \(![Process configuration builder](../image/icon-process-config.png)\).

3.  Open a table from the **Configurations** tab.

    The **Process details** page is displayed. Select **Recommendations setup** from the left bar.

    If you’re proceeding from the **Process details** page, then you come to this page. For more information, see [Configure process details](process-details.md).

    The **Recommendations setup** page has three sections:

    -   Activity fields
    -   Breakdown fields
    -   Child tables
4.  Fill the details in the **Activity fields** section.

    ![Activity fields in the Recommendations setup of process configuration](../image/process-config-activity.png)

    Activity fields are the most important fields in a project. They determine what kind of data you see on the process map.

    Provide columns in the **Fields representing process nodes** field.

    The columns that you had selected in the **State definition** and **Team definition** fields in the **Process details** tab, are automatically populated in the **Activity fields** area. You can add any other columns that you think are important for your process.

    The fields provided here are available as recommendations in for activity definition when creating a project on this table. For more information about how the recommended fields are displayed when setting activity definitions, see the table in the [Set activity definitions](set-activity-def.md) section.

5.  Fill the details in the **Breakdown fields** section.

    ![Breakdown fields in process configuration](../image/proces-det-2.png)

    Breakdown fields are used to segment the process, enabling the analysis of specific subsets of the process data. Configuring breakdown fields enables analysis of process subsets. It provides you with recommendations for the most suitable breakdown in your projects, and surfaces recommendations for automated root cause analysis fields in this process configuration.

    **Note:**

    -   Only fields that have a maximum column length of 250 characters are allowed.
    -   For parent table configurations, all the string breakdowns \(such as short description\) combined, a total of 6400 values are allowed.
    -   For child table configurations, breakdowns that are over the limit are excluded and no statistics are generated for them. For string breakdowns, fields are excluded when there are more than 640 unique values per field.
    -   For child table configurations, for non-string breakdowns, a maximum of 5000 unique values are allowed per field.
    -   If the total number of unique breakdown values for all child entities \(string and non-string\) is above 100k, all breakdowns for child tables is excluded regardless of whether or not they are over limit.
    For information about how these recommendations are provided when setting the breakdown definitions in a project, see [Set breakdown definitions](breakdown.md).

<table id="table_a1j_5m3_yfc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

**Fields representing classification of records**

</td><td>

Select the fields that describe how records are classified. The limit for dot-walking is 3 levels. For example: CI.BusinessService.assignment group.

The fields selected here are used as recommendations for automated root cause analysis during process configuration.

</td><td>

Category, Channel

</td></tr><tr><td>

**Field representing importance of records**

</td><td>

Select the fields that describe the importance of the records.

</td><td>

Priority

</td></tr></tbody>
</table>6.  Fill the details in the **Child tables** section.

    ![Child table in process configuration](../image/process-det-child.png)

    Child tables include data of dependent subprocesses that are important for the execution of the parent process. Analyzing child tables helps uncover inefficiencies in subprocesses that impact the main process's performance. Including child tables in the process configuration provides you with a list of related processes to add as an extra dimension of analysis to your project.

    For example, the Incident table serves as the parent table with general information about incidents. The Incident Task is the child table that stores specific tasks related to each incident.

    For more information about how these settings are available in the child tables when creating a project, see [Set use cases](adv-settings.md).

    1.  Select the **+** sign in the field.

        The **Add child table** dialog box is displayed.

    2.  Select a table.

    3.  Select a **Source field** value to identify the relationship.

    4.  The **Target field** is populated by default.

7.  Select **Continue to investigative features**.


**Parent Topic:**[Create process configuration using Process Configuration Builder](process-config-builder.md)

