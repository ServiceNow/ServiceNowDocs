---
title: Work set sub-activity form
description: The following table describes the field values for the sub-activity form on a work set standard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/work-set-sub-activity-form.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-05-25"
reading_time_minutes: 2
keywords: [sub-activity form, work set sub-activity]
breadcrumb: [Industrial Standards, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Work set sub-activity form

The following table describes the field values for the sub-activity form on a work set standard.

<table id="table_sub_activity_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of record that the sub-activity creates when the work set runs. Options are:-   **Standard**: Runs a referenced Industrial Guided Task standard as a child task.
-   **Action**: Creates an industrial action with the specified short description.

</td></tr><tr><td>

Standard

</td><td>

Industrial Guided Task standard to run. Visible and required when **Type** is **Standard**. Work set standards are excluded from selection because a work set can't contain another work set. Available standards are filtered to those that are global or in the user's site.

</td></tr><tr><td>

Short description

</td><td>

Short description for the generated action. Visible when **Type** is **Action**.

</td></tr><tr><td>

Functional location

</td><td>

Work area where the sub-activity runs. Filtered to the location of the parent standard when the parent is of scope local. When the parent is global, all functional locations are available.

</td></tr><tr><td>

Equipment

</td><td>

Equipment for which the sub-activity runs. This field is hidden when **Functional location** is empty. Filtered to equipment in the selected functional location.

</td></tr><tr><td>

Values to copy from work set task

</td><td>

Fields whose values are copied from the parent work set task to the generated child task or action at runtime. Use this field when a value should be supplied at execution time instead of on the sub-activity.

</td></tr><tr><td>

Schedule-based exception

</td><td>

When clear, the planned start and planned end of the generated child task follow the planned times of the work set task.

</td></tr></tbody>
</table>## How field values are resolved at runtime

When instantiating sub-activities, the system applies the following rules:

1.  Short description \(for action\): The short description from the sub-activity configuration is used as the short description for the child task \(sub-activity\).
2.  Functional location and equipment: When no functional location and equipment are defined in the sub-activity configuration, the functional location and equipment of the Work Set Standard are inherited by the child task.
3.  Collision handling: In case values for the sub-activity are defined in multiple locations for the same field, the follow order is used \(top is most important\):
    -   Functional location
    -   equipment field
    -   short description
    -   Values to copy from work set task
4.  If the dedicated field on the sub-activity is set.
5.  If the **Values to copy from work set task** field is empty.

If a functional location is not provided in either location, the standard can't be saved. A message prompts you to set a custom location on the sub-activity or to add the field to **Values to copy from work set task**.

**Parent Topic:**[Industrial Standards reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-standards-reference.md)

**Related topics**  


[Work set standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standards.md)

[Work set standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.md)

