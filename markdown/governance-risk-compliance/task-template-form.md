---
title: Task template form
description: Use the Task template form to define a reusable recovery task or event task that can be inserted into plans, loss scenarios, recovery strategies, exercise events, crisis events, or activated plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/task-template-form.html
release: australia
topic_type: reference
last_updated: "2026-05-16"
reading_time_minutes: 2
breadcrumb: [Configure Task templates and Task template groups, Configuring plan template, Setup for a BCP, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Task template form

Use the Task template form to define a reusable recovery task or event task that can be inserted into plans, loss scenarios, recovery strategies, exercise events, crisis events, or activated plans.

## Task template form

\[Omitted image "recovery-task-template-form.png"\] Alt text: Recovery task template form showing Number, Active, Short description, Dependencies, Phase, Task classification, and related lists.

For description of the field values, see the table.

<table id="table_task_template_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identifier for the task template \(for example, RTT0010003\).

</td></tr><tr><td>

Active

</td><td>

Set to true to make the template selectable from **Add tasks** and **Add groups** dialogs.

</td></tr><tr><td>

Short description

</td><td>

Short description shown on tasks created from this template.

</td></tr><tr><td>

Description

</td><td>

Full task description.

</td></tr><tr><td>

Dependencies

</td><td>

Other task templates within the same task template group that must be completed before this one starts.**Note:** Dependencies apply only when the template belongs to a task template group.

</td></tr><tr><td>

Phase

</td><td>

Recovery phase that the task belongs to. The Phase set here takes precedence over a Phase filter on the parent list. See [Add recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-a-recovery-task.md).

</td></tr><tr><td>

Task classification

</td><td>

Manual or Automated.

</td></tr><tr><td>

Tag

</td><td>

Tag to categorize the task.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item the task applies to.

</td></tr><tr><td>

Asset recovery level

</td><td>

Recovery level the task contributes to: **Not recovered**, **Partially recovered**, or **Recovered**.

</td></tr><tr><td>

Tag assets

</td><td>

**All** or **None**. You can change it to **Specific** after it is added to the plan. Controls how impacted assets are computed when the task is materialized.

</td></tr><tr><td>

Include task in

</td><td>

**Both actual events and exercises**, **Actual events only**, or **Exercises only**.

</td></tr><tr><td>

Planned duration \(Days, Hours, Minutes, Seconds\)

</td><td>

Estimated duration that pre-populates the **Planned duration** on the created task.

</td></tr><tr><td>

Owner

</td><td>

Default owner assigned to created tasks.

</td></tr><tr><td>

Assignment group

</td><td>

Default assignment group.

</td></tr><tr><td>

Additional assignees

</td><td>

Additional assignees for the created task.

</td></tr><tr><td>

Task template group

</td><td>

Read-only. The parent task template group when the template was created inside one.

</td></tr></tbody>
</table>## Related lists

|Related list|Description|
|------------|-----------|
|Plan templates|Plan templates that include this task template.|
|Loss scenarios|Loss scenarios that include this template through their task template groups.|
|Recovery strategies|Recovery strategies that include this template.|

**Parent Topic:**[Configure Task templates and Task template groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-task-temp-temp-groups.md)

