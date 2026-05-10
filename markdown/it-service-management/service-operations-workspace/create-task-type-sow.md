---
title: Create a task type for problem or change in Service Operations Workspace
description: Configure a task type that can be used during problem or change creation.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Problem Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a task type for problem or change in Service Operations Workspace

Configure a task type that can be used during problem or change creation.

## Before you begin

Role required: admin

## About this task

If you extend problem task or change task to add your own task type, you can set the child of problem or change task as the target table. Depending on the default values you set in the child of problem task or change task, you need not pass any values.

For information about creating a change task, see [Create a change task in Service Operations Workspace](create-change-task-sow.md).

For information about creating a problem task, see [Create a problem task in Service Operations Workspace](create-problem-task-sow.md).

## Procedure

1.  In the navigation filter, enter `sn_sow_interceptor_record_type_selector.list`.

2.  From the Record Type Selectors list, select **New**.

3.  On the Record Type Selector form, fill in the fields.

<table id="table_iyf_plx_5sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

Table that the task type applies to. Select Problem task \[problem\_task\] or Change Task \[change\_task\].

</td></tr><tr><td>

Order

</td><td>

Order of the task type in the Create problem task or Create change task dialog box.

</td></tr><tr><td>

Application

</td><td>

Scope of the application.

</td></tr><tr><td>

Active

</td><td>

Option for enabling the task type.

</td></tr><tr><td>

Title

</td><td>

Card title that is displayed in the Create problem task or Create change task dialog box.

</td></tr><tr><td>

Description

</td><td>

Card description.

</td></tr><tr><td>

Target table

</td><td>

Table where the record should be created when using this task type.**Note:** This field is not displayed if the table selected in the **Applies to** field does not have any child tables.

</td></tr><tr><td>

Values

</td><td>

Default values that are populated when creating a record using this task type.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring record pages in Service Operations Workspace for ITSM](../concept/configuring-record-pages-sow-itsm.md)

