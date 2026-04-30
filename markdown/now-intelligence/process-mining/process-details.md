---
title: Configure process details
description: Describe the process to get help with further configuration and enhance the quality of the project setup and analysis.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [With Process Configuration Builder, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure process details

Describe the process to get help with further configuration and enhance the quality of the project setup and analysis.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the Process configurations icon \(![Process configuration builder](../image/icon-process-config.png)\).

3.  Open a table from the **Configurations** tab.

    The **Process details** page is displayed. This page has three sections:

    -   Process perspectives
    -   Breakdown fields
    -   Child tables
    **Note:** Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

4.  Fill the details in the **Process perspectives** section.

    Process perspectives provide varied viewpoints for analyzing a business process. Adding fields to process perspectives provides you with recommendations for the most suitable activity definitions when creating a project. For more information about how the recommended fields are displayed when setting activity definitions, see the table in the [Set activity definitions](set-activity-def.md) section.

    Additionally, perspectives are used within the process configuration to recommend automated and rule-based improvement opportunity definitions and fields for automated root cause analysis. To see how the recommendations are made when setting the automated root cause analysis, see automated root cause analysis section in the [Configure investigative features](investigative-features.md) section. To see how recommendations are made when setting the improvement opportunities, see [Configure improvement opportunities](improvement-opportunities.md).

    ![Process details for process configuration](../image/process-det-1.png)

5.  Select the **+** sign under each section.

    The **Add field** dialog box is displayed.

    1.  Select a field.

    2.  Select **Save**.

<table id="table_wmj_zsq_ndc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

**Which fields represent progression of records through steps?**

</td><td>

Select the fields that describe the order in which the activities are executed. It’s usually the starting point for a process mining analysis.This is also known as control-flow perspective.

</td><td>

State, substate

</td></tr><tr><td>

**Which field represents teams owning a record?**

</td><td>

Select the fields that describe the resources \(such as teams\) required for the execution of a process and how they interact with each other.The fields selected here are used as recommendation for automated root cause analysis during process configuration.

This is also known as resource perspective.

</td><td>

Assignment group

</td></tr><tr><td>

**Which field represents the person working on a record?**

</td><td>

Select the fields that describe the resources \(such as people\) required for the execution of a process and how they interact with each other.This is also known as resource perspective.

</td><td>

Assigned to

</td></tr><tr><td>

**Which other fields would you like to analyze?**

</td><td>

Any other field of your choice. You can choose from the recommended fields. These fields are recommended for their high frequency of changes in your process.

</td><td>

Priority

</td></tr></tbody>
</table>6.  Fill the details in the **Breakdown fields** section.

    ![Breakdown fields in process configuration](../image/proces-det-2.png)

    Breakdown fields are used to segment the process, enabling the analysis of specific subsets of the process data. Configuring breakdown fields enables analysis of process subsets, provides you with recommendations for the most suitable breakdown in your projects, and surfaces recommendations for automated root cause analysis fields in this process configuration.

    For information about how these recommendations are provided when setting the breakdown definitions in a project, see [Set breakdown definitions](breakdown.md).

<table id="table_xqk_jhr_ndc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

**Fields representing classification of records**

</td><td>

Select the fields that describe how records are classified. The limit for dot-walking is 3 levels. For example: CI.BusinessService.assignment group.

The fields selected here are used as recommendation for automated root cause analysis during process configuration.

</td><td>

Category, Channel

</td></tr><tr><td>

**Field representing importance of records**

</td><td>

Select the fields that describe the importance of the records.

</td><td>

Priority

</td></tr></tbody>
</table>7.  Fill the details in the **Child tables** section.

    ![Child table in process configuration](../image/process-det-child.png)

    Child tables include data of dependent subprocesses that are important for the execution of the parent process. Analyzing child tables helps uncover inefficiencies in subprocesses that impact the main process's performance. Including child tables in the process configuration provides you with a list of related processes to add as an extra dimension of analysis to your project.

    For example, the Incident table serves as the parent table with general information about incidents, while the Incident Task is the child table that stores specific tasks related to each incident.

    For more information about how these settings are available in the child tables when creating a project, see [Set use cases](adv-settings.md).

    1.  Select the **+** sign in the field.

        The **Add child table** dialog box is displayed.

    2.  Select a table.

    3.  Select a **Source field** value to identify the relationship.

    4.  The **Target field** is populated by default.

8.  Select **Continue to investigative features**.


**Parent Topic:**[Create process configuration using Process Configuration Builder](process-config-builder.md)

