---
title: Create a project
description: Create a project with the imported external data. You must mine the project to analyze your data and improve your processes.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Working with external datasets, Using Process Mining, Process Mining, Platform Analytics]
---

# Create a project

Create a project with the imported external data. You must mine the project to analyze your data and improve your processes.

## Before you begin

Role required: sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the External data integration icon \( ![External data integration icon](../image/ext-dataset-modules.png)\).

3.  Select a dataset based on which you want to create a project.

    The dataset opens in a new tab.

4.  Select **Create project**.

    ![Create Project](../image/ext-data-edit.png)

    You are automatically taken to the **Scope your analysis** page on Project Builder.

5.  Add activity definitions to the project.

    You can add breakdown filters if required.

    For information, see [Scoping your analysis](../concept/scope-analysis.md)

6.  Select **Add child entity**.

    **Note:** You must add a child entity if you are doing multi-dimensional mining using external data.

7.  On the form, fill in the fields.

<table id="table_bxy_kqx_5zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

You can select one of the following source type:-   Table: Any database table
-   Report source: Select a table that has reports
-   Archived data: Select an archived table.


</td></tr><tr><td>

Select

</td><td>

Select the table that you want to link with the external dataset.

</td></tr><tr><td>

Parent table

</td><td>

Select the external data table that you are using to create the project.

</td></tr><tr><td>

Relation

</td><td>

Select **Reference** as this will be a reference field.

</td></tr><tr><td>

Source field

</td><td>

This is automatically populated.

</td></tr><tr><td>

Target field

</td><td>

Select the target reference field.**Note:** To provide a value for this field, you must create a custom field of the type **Reference** while creating the audit table. This will enable you to configure the source and target fields accordingly. For more information, see [Add custom fields to the audit table](add-custom-field.md).

</td></tr></tbody>
</table>    **Note:** You can add any activity definitions or breakdown filters that is required.

8.  Select Next.

9.  Create improvement opportunities if required.

    For information, see [Set improvement opportunities](improve-opportunities.md).

10. Review and mine the project.

    For information, see [Review and mine your project](review-mine.md).


**Parent Topic:**[Working with external datasets](../concept/external-dataset.md)

