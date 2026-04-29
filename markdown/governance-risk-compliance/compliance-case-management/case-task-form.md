---
title: Case task form
description: Use the Case Task form in the GRC: Compliance Case Management application to create a case task for a reported compliance case.
locale: en-US
release: australia
product: Compliance Case Management
classification: compliance-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create action task, Compliance case task workflow, Use, Compliance Case Management, Governance, Risk, and Compliance]
---

# Case task form

Use the Case Task form in the GRC: Compliance Case Management application to create a case task for a reported compliance case.

See the following table for a description of the field values.

<table id="table_g2y_bgb_pvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the case task. This field is automatically set.

</td></tr><tr><td>

State

</td><td>

Workflow state of the case task. This field is automatically set to **Draft**.

</td></tr><tr><td>

Title

</td><td>

Name of the task that is being created for the case. For example, Investigation for wrongly charged late payment fees.

</td></tr><tr><td>

Type

</td><td>

Type of task:-   **Assessment**: Collect the responses from the users about the case.

**Note:** Only case tasks with the Assessment case task type can be reassigned to a different task owner if required.

-   **Investigation**: Create a case task to perform any investigation for the case reported. For example, you may want to determine the cause of wrongly charged late payment fees.
-   **Others**: Any other type of task that you configure.

</td></tr><tr><td>

Priority

</td><td>

Priority of the case task.

</td></tr><tr><td>

Assessment template

</td><td>

Assessment template available to assess the case recorded. This field appears only when **Assessment** is selected from **Type**. **Note:** Each case type can be mapped to specific assessment templates during the configuration. Only the templates that are mapped to the case are available for selection. For example, if the case type is **Financial fraud**, then the assessment templates that are specific to the financial fraud type are available for selection. You can’t select the same assessment template if an open assessment with the selected assessment template is already being worked on.

</td></tr><tr><td>

Description

</td><td>

Brief description of the case task. This description is useful for the user who works on the case task.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group that works on the case task. Any user who belongs to the selected group can work on the case task if a case task owner isn’t specified.

</td></tr><tr><td>

Case task owner

</td><td>

Person who owns the case task. The user selected in this field must be a member from the assignment group.

</td></tr><tr><td>

Watch list

</td><td>

Users who must be informed about the case.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Date within which the case task must be completed.**Note:** The due date must be before the date specified in the **Case closure SLA** field on the case form.

</td></tr><tr><td>

Accepted date

</td><td>

Date when the case is accepted.

</td></tr><tr><td>

Created

</td><td>

Date when the case is created and assigned to the case task owner.

</td></tr><tr><td>

Task closure date

</td><td>

Date when the task is closed.

</td></tr><tr><td class="sub-head" colspan="2">

Summary

</td></tr><tr><td>

Observations

</td><td>

Observations that you make about the case while you’re working on the case task.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Additional comments

</td><td>

Additional information about the case task.

</td></tr></tbody>
</table>**Parent Topic:**[Create an action task](../task/create-a-case-task.md)

