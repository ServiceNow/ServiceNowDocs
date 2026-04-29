---
title: Action form
description: The following table describes the field values for the Action form.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Action form

The following table describes the field values for the Action form.

<table id="table_wtc_zfv_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description of the action.

</td></tr><tr><td>

Description

</td><td>

Description of the action and its purpose.

</td></tr><tr><td>

Functional location

</td><td>

Industrial facility work area where the action is completed. The location is defined using the ISA-95 standard. This field is automatically set based on the logged-in user's worker profile.

</td></tr><tr><td>

Equipment

</td><td>

Machine to which the action relates. This field is automatically set if equipment is specified in the standard.

</td></tr><tr><td>

Origin

</td><td>

Task from which the action originates.

</td></tr><tr><td>

Opened by

</td><td>

User opening the action. This field is automatically set by the system and can’t be modified.

</td></tr><tr><td>

Assignment group

</td><td>

Team or department responsible for completing the task.

</td></tr><tr><td>

Assigned to

</td><td>

User that the action should be assigned to.

</td></tr><tr><td>

Additional assignee list

</td><td>

List of users to be notified or contributing to the task, but not as the primary assignee. Available options vary depending on the selected functional location or assignment group.

</td></tr><tr><td>

Impact

</td><td>

Measure of effect the action has on an industrial process. Options are:-   1 - Safety
-   2 - Quality
-   3 - Reliability
-   4 - Operations
-   5 - Other

</td></tr><tr><td>

Urgency

</td><td>

Measure of how long the action can be delayed until there's a significant impact on an industrial process. Options are:-   1 - Critical
-   2 - Important
-   3 - Routine
-   4 - Not urgent

</td></tr><tr><td>

Priority

</td><td>

Priority of the action. This field is automatically set based on impact and urgency. Options are:-   1 - Direct
-   2 - This shift
-   3 - Today
-   4 - Within 7 days
-   5 - Within 30 days

For more details, see [Priority matrix for actions](priority-matrix-actions.md).

</td></tr><tr><td>

Due date

</td><td>

Date by which the task should be executed. If you don't set the due date, it is calculated based on priority when you save the form. For more details, see [Due date calculation](due-date-calculation.md).

</td></tr><tr><td>

Escalate to

</td><td>

User that the action should be escalated to.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Factory Workspace reference](digital-factory-workspace-reference.md)

