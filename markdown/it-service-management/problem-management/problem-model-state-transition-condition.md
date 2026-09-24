---
title: Problem Management model state transition condition form
description: Description of the field values for the model state transition condition form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/problem-management/problem-model-state-transition-condition.html
release: brazil
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Problem Management model state transition condition form

Description of the field values for the model state transition condition form.

<table id="table_ybk_z2v_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the condition.

</td></tr><tr><td>

State Transition

</td><td>

State that you're applying the transition condition to. This field is automatically set with the state that you're applying the condition to.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the condition.

</td></tr><tr><td>

Requires

</td><td>

Condition for your transition. You can select a pre-defined condition or select **Transition Condition** to define a condition. To create pre-defined conditions, see [Create predefined conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-predefined-transition-condition-type.md).

</td></tr><tr><td>

Condition \(condition builder\)

</td><td>

Condition on the problem task record that must be fulfilled to enable the transition.

</td></tr><tr><td>

Condition \(Script\)

</td><td>

Script that must be fulfilled to enable the transition. The script returns a value of **True** when passed. This field is available only when **Transition Script** is selected from **Requires** field.**Note:** To edit the Condition \(Script\) field, you need the problem\_model\_script\_admin role. Without it, the script editor is read-only. No existing role inherits this role, so it must be assigned directly. For information on assigning a role to a user, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignARoleToAUser.md).

</td></tr><tr><td>

Active

</td><td>

Option to make the condition active.

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/problem-management/reference-section-for-problem-management.md)

