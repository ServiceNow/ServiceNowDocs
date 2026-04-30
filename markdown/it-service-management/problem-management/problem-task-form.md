---
title: Problem Task form
description: Description of the field values for the problem task form.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Problem Task form

Description of the field values for the problem task form.

<table id="table_ldc_lqq_pfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Read-only. Unique number to identify the task.

</td></tr><tr><td>

Type

</td><td>

Read-only state. Determines whether the problem task is created specifically to investigate the cause of the problem or is a general task.

**Note:** This field appears only for new customers from Madrid or a later release as it is part of the state management process.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the problem applies to. The CI class of the selected configuration item identifies the type of problem, for example, hardware, network, or database.

</td></tr><tr><td>

Due date

</td><td>

Date within which the problem task should be completed.

</td></tr><tr><td>

Source problem

</td><td>

Unique number of the problem for which the problem task is created.

</td></tr><tr><td>

State

</td><td>

For existing customers, the available states are: **Pending**, **Open**, **Work in Progress**, **Closed Complete**, **Closed Incomplete**, and **Closed Skipped**.

 For new customers from Madrid, the state management process is applied. This state field is a read-only field. The states available are: **New**, **Assess**, **Work in Progress**, and **Closed**.

</td></tr><tr><td>

Close code

</td><td>

Read-only field indicating whether the problem task was completed or canceled. **Note:** This field appears only for new customers from Madrid or a later release as it is part of the state management process.

</td></tr><tr><td>

Priority

</td><td>

How quickly the service desk should address the problem task \(Critical, High, Moderate, Low, or Planning\).

</td></tr><tr><td>

Assignment group

</td><td>

Specific group to whom the problem task is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

Specific problem analyst to whom the task is assigned to.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the problem task.

 When you update the short description, and move to another field, the **Related Search** field displays knowledge articles. If you configure the problem properties, then the **Related Search** field displays other related information related to the short description.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the problem task.

</td></tr><tr><td>

Related Search

</td><td>

Result of a search. **Note:** If you want to search and link a knowledge article to the Problem task, click **Attach**.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notification when work notes are added to the problem task.

</td></tr><tr><td>

Work notes

</td><td>

Inscription about the work that you perform on the problem task.

</td></tr><tr><td class="sub-head" colspan="2">

Analysis Information

</td></tr><tr><td>

Cause code

</td><td>

Cause of the Problem such as Environmental disaster, Hardware issue, People/Process/Documentation.

</td></tr><tr><td>

Workaround \(Root Cause Analysis only\)

</td><td>

Method that you have used to overcome the Problem. It can be a way of dealing with a problem or making something work despite the problem not being resolved.

</td></tr><tr><td class="sub-head" colspan="2">

Closure Information

</td></tr><tr><td>

Completed by

</td><td>

Read-only field. Name of the user who completed the task.

</td></tr><tr><td>

Completed

</td><td>

The reason why this problem task has been canceled.

</td></tr><tr><td>

Proposed fix notes \(Root Cause Analysis only\)

</td><td>

Inscription on how you have fixed the problem task.

</td></tr><tr><td>

Close notes \(General task only\)

</td><td>

Inscription on the work you have completed.

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Problem Management](../concept/reference-section-for-problem-management.md)

