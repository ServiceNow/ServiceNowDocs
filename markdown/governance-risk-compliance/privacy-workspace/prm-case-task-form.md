---
title: Case task form
description: On the new case task form, fill in the fields.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a case task, Case task workflow, Use, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Case task form

On the new case task form, fill in the fields.

<table id="table_g2y_bgb_pvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the case task. This field is automatically set.

</td></tr><tr><td>

Title

</td><td>

Name of the task being created for the case. For example, `Investigation for loss of data`.

</td></tr><tr><td>

Type

</td><td>

Type of task. The choices are as follows:-   **Assessment**: Use this option if you want to perform an assessment to collect responses from users regarding the case.

**Note:** Only case tasks with type Assessment type can be reassigned to a different task owner if required.

-   **Investigation**: Use this option if you want to create a case task to perform any investigation for the case reported. For example, you may want to determine the type of data lost.
-   **Others**: Use this option for any other type of task that you configure.

</td></tr><tr><td>

Assessment template

</td><td>

[Assessment template](../../grc-compliance-case-mgmt/task/ccm-create-assessment-template.md) to assess the case. This field appears only when **Assessment** is selected from the **Type** field. **Note:** Each case type can be mapped to specific assessment templates during configuration. Only the templates mapped to the case are available for selection. For example, if the case type is **Financial**, then the assessment templates specific to the Financial type will be available for selection. You cannot select the same assessment template if there is already an open assessment with the assessment template that you have selected is being worked upon.

</td></tr><tr><td>

State

</td><td>

Workflow state of the case task. This field is automatically set to **Draft**.

</td></tr><tr><td>

Description

</td><td>

Brief description of the task. This description is useful for the user who works on the task.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group that will work on the case task. Any user who belongs to the selected group can work on the case task if a case task owner is not specified.

</td></tr><tr><td>

Case task owner

</td><td>

Person who owns the case task. The user selected in this field must be a member from the assignment group.

</td></tr><tr><td>

Watch list

</td><td>

Users who must have the access to view the case task.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Date within which the case task must be completed. The due date must be before the date specified in the **Case closure SLA** field on the case form.

</td></tr><tr><td>

Accepted date

</td><td>

Date the case is accepted.

</td></tr><tr><td>

Created

</td><td>

Date the case is created and assigned to the case task owner.

</td></tr><tr><td>

Task closure date

</td><td>

Date of the task closure.

</td></tr><tr><td class="sub-head" colspan="2">

Summary

</td></tr><tr><td>

Observations

</td><td>

Observations you make about the case while working on the case task.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Worknotes for the case task.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Comments related to the case task, if any.

</td></tr></tbody>
</table>**Parent Topic:**[Create a case task](../task/prm-create-a-case-task.md)

