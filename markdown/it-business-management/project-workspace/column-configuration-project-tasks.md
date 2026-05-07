---
title: Supported columns for project and task generation
description: Now Assist extracts project and project task details from uploaded documents \(e.g., excel workbooks\). Recognized data is mapped to pm\_project and pm\_project\_task columns. Columns not present in the document are initialized with valid defaults internally.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Project Workspace reference, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Supported columns for project and task generation

Now Assist extracts project and project task details from uploaded documents \(e.g., excel workbooks\). Recognized data is mapped to pm\_project and pm\_project\_task columns. Columns not present in the document are initialized with valid defaults internally.

|Column|Description|
|------|-----------|
|`short_description`|Project name/title|
|`description`|Detailed project description|
|`approved_start_date`|Project start date|
|`approved_end_date`|Project end date|
|`business_case`|Business case/objectives|

<table id="table_fvh_l1c_cjc"><thead><tr><th>

Column

</th><th>

Extracted from/Default behavior

</th></tr></thead><tbody><tr><td>

`short_description`

</td><td>

Task name: mandatory, extracted from document

</td></tr><tr><td>

`description`

</td><td>

Task details/deliverables. If only a name exists, a brief description is generated from context.

</td></tr><tr><td>

`start_date`

</td><td>

Task start date

</td></tr><tr><td>

`end_date`

</td><td>

Task end date

</td></tr><tr><td>

`duration`

</td><td>

Task duration \(derived or explicit\)

</td></tr><tr><td>

`work_start`

</td><td>

Work start date/time

</td></tr><tr><td>

`work_end`

</td><td>

Work end date/time

</td></tr><tr><td>

`work_duration`

</td><td>

Actual work duration

</td></tr><tr><td>

`state`

</td><td>

Task state \(defaults internally if absent\)

</td></tr><tr><td>

`milestone`

</td><td>

Whether the task is a milestone

</td></tr><tr><td>

`key_milestone`

</td><td>

Whether it is a key milestone

</td></tr><tr><td>

`constraint_date`

</td><td>

Date constraint for scheduling

</td></tr><tr><td>

`time_constraint`

</td><td>

Type of time constraint applied

</td></tr><tr><td colspan="2">

**Note:**

If a column value is not present in the excel document, it is handled internally and initialized with a valid default.

</td></tr></tbody>
</table>**Parent Topic:**[Project Workspace reference](../../project-workspace/reference/project-workspace-reference.md)

