---
title: Create a task for a customer service case
description: Create a task for a customer service case for additional work that needs to be completed as part of resolving the case.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Create a task for a customer service case

Create a task for a customer service case for additional work that needs to be completed as part of resolving the case.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager, or admin

## About this task

When you create a task, the system uses information from the case to automatically fill in fields on the Case Task form. After you create and save a task, it appears in the **Tasks** related list on the Case form.

## Procedure

1.  Open the desired case.

2.  From the **Tasks** related list, click **New**.

3.  Fill in the fields on the Case Task form.

<table id="table_case_task_form_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically assigned case task number.

</td></tr><tr><td>

Parent case

</td><td>

The number of the parent case. This can be a case from the Case \[sn\_customerservice\_case\] table or any child tables of the Case table.

</td></tr><tr><td>

Parent

</td><td>

The number of the parent record if the task is created from a type of record other than a case. This field is populated when a case task is created from a non-case record such as an incident, problem, change, or request. This field is a reference to the Task \[task\] table.**Note:** You may need to configure the case task record to display the **Parent** field. For more information about adding fields to a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Contact

</td><td>

The contact for the parent case. This field is a reference to the Contact \[customer\_contact\] table.

</td></tr><tr><td>

Account

</td><td>

The account for the parent case. This field is a reference to the Account \[customer\_account\] table.

</td></tr><tr><td>

Consumer

</td><td>

The consumer for the parent case. This field is a reference to the Consumer \[csm\_consumer\] table.

</td></tr><tr><td>

Subject

</td><td>

The subject of the case task.

</td></tr><tr><td>

Description

</td><td>

A description of the work that needs to be done in order to complete the case task.

</td></tr><tr><td>

Priority

</td><td>

The assigned priority of the case task:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low \(default\)


</td></tr><tr><td>

State

</td><td>

The current state of the case task:-   Open
-   Closed


</td></tr><tr><td>

Assigned to

</td><td>

The assigned user.

</td></tr><tr><td>

Service Definition

</td><td>

This field is a reference to the Service Definition \[sn\_case\_type\_selection\] table.

</td></tr><tr><td>

Work notes list

</td><td>

Internal users who receive a notification about this case when work notes are added. You can only add internal users to the work notes list.

</td></tr><tr><td>

Work notes

</td><td>

Information about the case task, such as steps taken toward resolution. Internal users who have been added to the **Work notes list** receive a notification when work notes are added to a case task.

</td></tr><tr><td>

Additional comments

</td><td>

Customer-viewable comments. Each comment is inserted into the **Activity** field when the user selects **Post**.

</td></tr></tbody>
</table>4.  Click **Update**.


