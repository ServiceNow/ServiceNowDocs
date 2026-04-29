---
title: Field map form
description: Understand the fields of the field map form. This form is used to create mappings for a corresponding table map.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Form field information for Strategic Planning, Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Field map form

Understand the fields of the field map form. This form is used to create mappings for a corresponding table map.

<table id="table_bwj_x2l_v5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution table

</td><td>

Table in Agile Development 2.0, SAFe, or PPM that needs to be mapped with a table in Strategic Planning. The value in this field is automatically added based on the selection made in the table map configuration.

</td></tr><tr><td>

Execution table column

</td><td>

Field column of the selected execution table that needs to be mapped.

</td></tr><tr><td>

Alignment table

</td><td>

Table in Strategic Planning that needs to be mapped with a table in Agile Development 2.0, SAFe, or PPM. The value in this field is automatically added based on the selection made in the table map configuration.

</td></tr><tr><td>

Alignment table column

</td><td>

Field column of the selected alignment table that needs to be mapped.

</td></tr><tr><td>

Flow type

</td><td>

Specifies whether the mapping is done from alignment to execution, execution to alignment, or both.Here, alignment implies Strategic Planning, and execution implies PPM, Agile Development 2.0, and SAFe applications.

</td></tr></tbody>
</table>You can also create custom fields and map them to the required source fields as needed. For example, if you want to display the execution project number, you can create a custom field called 'Project number' in the Project planning item \[sn\_align\_core\_project\] table within the Portfolio Planning Core application scope. Then, map this field to the 'Number' field of the Project table \(pm\_project\) using the project field map.

**Parent Topic:**[Form field information for Strategic Planning](../../alignment-planner-workspace/reference/form-field-information-for-strategic-planning.md)

