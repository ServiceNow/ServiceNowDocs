---
title: Case task form
description: The case task form displays information about case tasks, which are created and assigned to users to complete the work necessary to resolve customer service cases.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-08"
reading_time_minutes: 2
breadcrumb: [Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Case task form

The case task form displays information about case tasks, which are created and assigned to users to complete the work necessary to resolve customer service cases.

The case task form includes the following fields.

<table id="table_vyg_gzg_lvb"><thead><tr><th>

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

The number of the parent record if the task is created from a type of record other than a case. This field is populated when a case task is created from a non-case record such as an incident, problem, change, or request. This field is a reference to the Task \[task\] table.**Note:** You may need to configure the case task record to display the **Parent** field.

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

Service

</td><td>

If a service has been selected for a case task, the service is displayed in this field. The **Service** field is a reference to the [Service Definitions](../concept/csm-service-definitions.md) table \(sn\_case\_type\_selection\).

 **Note:** The Customer Service plugin \(com.sn\_customerservice\) and the Customer Service Case Types plugin \(com.snc.csm\_case\_types\) are required for the **Service** field to appear on case task lists and forms.

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

Service

</td><td>

This field is a reference to the Service \[cmdb\_ci\_service\] table.

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

</td></tr><tr><td>

Visible to customer

</td><td>

If this check box is enabled, the case task is visible to end users from the Customer or Consumer Portals.

</td></tr></tbody>
</table>