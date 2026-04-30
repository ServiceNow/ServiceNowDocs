---
title: Enable task configuration for approvals
description: Provide the approvers with more in-context information about the approval requests for informed and prioritized approval workflows.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Enable task configuration for approvals

Provide the approvers with more in-context information about the approval requests for informed and prioritized approval workflows.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

## About this task

Each task configuration is associated with a table that is an extension of the To-dos configuration. Define the following task configuration sections:

-   Task configuration
-   Common information
-   Primary information
-   Tab configuration
-   Actions

Here is a sample illustration of how these configurations appear on the approvals page.

![Approval hub workflow in Employee Center portal and NowMobile](../images/approval-hub-sap-workday.png "Approval hub workflow in Employee Center")

The information displayed on each section of the page depends on the individual approval request type. When a configurable section has no specified value or when a user does not have permission; information isn’t displayed.

-   Customize the experience by embedding widgets for all sections except task configuration.
-   Click the URLs for additional information and context.
-   Use the condition builder to specify the conditions that a task must meet to appear on the to-dos page.

## Procedure

1.  Go to **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configurations**, click an existing to-dos configuration, and navigate to the **Task Configuration** related list.

2.  Click an existing **Task Configuration** record.

3.  Fill in the fields on the form.

<table id="table_ipr_bbk_4fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the task configuration.

</td></tr><tr><td>

Application

</td><td>

Application for the task configuration.

</td></tr><tr><td>

Active

</td><td>

Check the box to activate the task configuration for use.

</td></tr><tr><td>

Table

</td><td>

Name of the table configured in the to-dos configuration to which the task config is associated.

</td></tr><tr><td>

Additional conditions

</td><td>

Conditions that a task must meet to apply configuration. You can dot-walk to the associated table to define conditions on other table columns. Conditions are implemented on top of conditions from To-dos config. Use the conditions to suit your requirements.

</td></tr><tr><td>

Reference column

</td><td>

To define conditions to the non-associated table, use a reference column from the selected table to help define conditions on reference tables. For example, the approvals reference column is **sysapproval**.**Note:** If the underlying submitted request is stored in a non-task table, select **Source table**.

</td></tr><tr><td>

Reference table

</td><td>

Reference table from above table to help define conditions on reference tables. For requests, the reference table is **sc\_request**. You can select task or non-task tables in a task configuration such as **sn\_wsd\_rsv\_reservation**. Also, use **Scripted Extension Points** to create **sn\_ex\_sp.RefNonTaskTables**.

</td></tr></tbody>
</table>4.  Go to **Common Info** to configure the to-dos configuration header.

<table id="table_yz2_tk3_dvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Common info fields type

</td><td>

Select one of the following options to pick fields from the parent table or reference table as common info.-   **Fields**
-   **Custom**


</td></tr><tr><td>

Common info fields - **Fields**

</td><td>

Fields you select from the parent table to appear as common info. When you select **Fields** from the parent table such as **Approval for.Number, Due date, Created, State**, the fields appear as common info.**Note:** When you select more than four fields, an error message appears.

</td></tr><tr><td>

Common info fields - **Custom**

</td><td>

Fields you specify from the parent and/or reference table to appear as common info. When you specify **Custom** fields such as **\{reference\_table.number\},\{table.state\}**, the number and state fields appear as common info.

</td></tr><tr><td>

Link to task

</td><td>

The link that opens the parent task or external links. You can link to a task or non-task table approvals. When you select the **External** option to open the link in a new tab. Also, adds an icon to denote an external link. Select one of the options as **URL source** to display as URL.

-   When you select **Custom**, specify the URL directly. URL can have values from table and reference table. For example, **\{table.&lt;fieldname&gt;\} or \{reference\_table.&lt;fieldname&gt;\}**.
-   When you select **Fields**, map a field from the table and specify a page parameter value.
-   When you select **Page**, specify page \(for example esc\_kb\_category\) and page parameter values.

**Note:** These options appear only for non-task tables and when you select **Link to task**.

</td></tr></tbody>
</table>5.  Go to **Primary Info** to configure the details.

<table id="table_kfs_qm1_wtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use widget

</td><td>

Select this option to use widget and widget parameters to customize experience of **Primary Info**.

</td></tr><tr><td>

Widget

</td><td>

Widget to display in the primary info section. Select the widget from the list. This field appears only when the **Use widget** option is selected. You can embed a custom or ootb widget for the entire primary section.

</td></tr><tr><td>

Widget parameters

</td><td>

Comma-separated list of widget parameters. You can specify a combination of static and dynamic text in the widget parameter values. This field appears only when the **Use widget** option is selected.

</td></tr><tr><td>

Title type

</td><td>

Indicates the title type that you want to display in the to-dos.-   **Custom**: Indicates the custom text that appears as the to-dos configuration details.
-   **Fields**: Maps a field from the table that you selected to appear as the title.


</td></tr><tr><td>

Title

</td><td>

Title of the record. -   Appears when you select **Custom** from the **Title type** list. Specify a combination of static text and dynamic field values as the title.

    -   To define the title from the table, use the Table **\{table.field\_name\}**.
    -   To define the title from the reference table, use the Reference table **\{reference\_table.field\_name2\}**.
Field name indicates the variable to be replaced with the column names from the respective tables.

**Note:** Ensure you append **table.** or **reference\_table.** as a prefix to avoid rendering issues.

-   Appears when you select **Field** from the **Title type** list. Map a field from the table that you selected to appear as the title.


</td></tr><tr><td>

Page

</td><td>

Page you want to open when you click the link. This field \(kb\_article\_view\) appears only when the Reference column is Source table and the Reference table is Knowledge \(kb\_knowledge\).

</td></tr><tr><td>

Page parameters

</td><td>

Additional parameters are required by some pages to look up a record \(sysparam\_article\).

</td></tr><tr><td>

Fields

</td><td>

The fields you want to appear in the detail row of to-dos. The fields you choose are based on the table you selected.Only appears when you select **Parent fields** from the **Detail type** list.

</td></tr><tr><td>

Fields \(Reference table\)

</td><td>

Indicates the fields that you want to appear as the to-dos configuration details. If you select multiple fields, they’re separated by a hyphen. Only appears when you select **Fields** from the **Detail type** list.**Note:** The price field mapping from the Primary section for OOTB REQ record is removed. However, Admin can add it if required.

</td></tr></tbody>
</table>6.  On the form, fill in the fields.

<table id="table_wdz_fcy_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Tab type based on which a widget is displayed. Possible options are:-   Activity Stream: To display activity from the source task or request.
-   Line Items: To display parent-child relationship in multi-lines.
-   Attachments: To add or display the attachments from the source task or request.
-   Custom: To select a widget and parameters.
-   Variable Summarizer: To display only variables user had selected while requesting the item in a summarized format.
-   Variable Editor \(Read-only\): To display all variables present in the task in the format while creating request.
-   Selectable Line items: To display multiple line items that you can select and perform actions as a batch.

**Note:** Using this option allows you to filter the requests by state.

</td></tr><tr><td>

Source

</td><td>

Source for the selected type.

</td></tr><tr><td>

Table

</td><td>

Name of the table that the tab is associated with.

</td></tr><tr><td>

Display name

</td><td>

Display name of the tab.

</td></tr><tr><td>

Application

</td><td>

Application associated with the approval configuration.

</td></tr><tr><td>

Order

</td><td>

Order in which the tab is displayed in the tabs section.

</td></tr><tr><td>

Visible

</td><td>

Conditions for the tab visibility.

</td></tr><tr><td>

Script

</td><td>

Option to enable adding a script for the tab visibility. By default, this check box is cleared.

</td></tr><tr><td>

Visible script

</td><td>

Script for the tab visibility.-   If the script returns true, the tab is visible on the standard ticket page.
-   If the script returns false, the tab is not visible on the standard ticket page.
**Note:** This field appears only when the **Script** check box is selected.

</td></tr><tr><td>

Widget

</td><td>

Widget displayed in the tabs section. This field appears only when **Custom** is selected from **Type**.

</td></tr><tr><td>

Widget parameters

</td><td>

Comma-separated list of tab widget parameters.

</td></tr></tbody>
</table>7.  Click **Actions** to search and select the required action group.

    Select the **Approvals action group** to display the frequently used actions such as **Approve** or **Reject**. For more information, see [Action framework](../concept/action-group-framework.md).

8.  Add **Comments** in a custom widget to show comments.

    **Note:**

    -   Ensure you have the write permissions to the Comment field. Check the ACL and grant permissions to add comments.
    -   For more information on adding comments while rejecting an approval request, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0760283](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0760283).
9.  Click **Submit** or **Update**.


## Result

Based on this configuration, the approvers see the in-context important information about the approval and complete the approval. For more reference info, see [Approvals experience reference](../reference/approval-hub-ootb.md).

**Note:** A user must have the approval\_user or business\_stakeholder role to approve IT requests \(not applicable to other requests such as HR approvals\) on Employee Centre. Role validation has not been implemented in Core UI16 because modifying ACLs in UI16 might have broader implications at the NowPlatform level.

Use the out-of-the-box **Approvals action group** to display the actions such as **Approve** and **Reject**. For more information, see [Action framework](../concept/action-group-framework.md).

**Note:** For actions to appear in the my items widget, you can add the OOTB **Approvals action group** from **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configurations**, click an existing to-dos configuration, navigate to the **To-do Configuration Details** record, and use the OOTB **Approvals action group** under **Fields Mapping**.

.

**Related topics**  


[Use Approvals hub](ec-to-dos-use-approval-hub.md)

[Approvals in Now Mobile](../concept/approvals-mesp-ec.md)

[Action framework](../concept/action-group-framework.md)

