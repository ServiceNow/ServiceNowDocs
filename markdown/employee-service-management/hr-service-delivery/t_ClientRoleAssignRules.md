---
title: Client role assignment rules
description: Use Client Role Assignment Rules to automatically assign or reassign a role to an employee.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Client roles, Manage HR roles, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Client role assignment rules

Use Client Role Assignment Rules to automatically assign or reassign a role to an employee.

## Before you begin

Role required: sn\_hr\_core.admin

A condition or set of multiple condition clauses based on the HR profile \[sn\_hr\_core\_profile\] table are used to automate assigning roles.

**Note:** Client role assignment rules are for access to the Employee Center only.

For example:

-   A newly hired employee can be automatically assigned the new hire \[sn\_hr\_core.hrsm\_new\_hire\] role. This role provides limited access to the Employee Center or service portal.
-   The Update Client Roles scheduled job runs and acknowledges the employee start date for the new hire has not been reached.
-   The Assign HR Roles business rule assigns the new hire role based on the conditions set on the client role assignment rules.

To map conditions to a client role:

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Manage Roles** &gt; **Client Role Assignment Rules**.

2.  Click **New** to create a client role rule or click an existing client role rule to edit.

3.  **Active** is enabled by default.

4.  From **Condition**, click the **Lookup using list** and select an existing HR condition.

5.  Click **New** to create an HR condition.

    You can also click the **Preview this record** icon to open the record.

<table id="choicetable_myd_4sm_b2b"><thead><tr><th align="left" id="d374130e147">

Field

</th><th align="left" id="d374130e150">

Description

</th></tr></thead><tbody><tr><td id="d374130e156">

**Name**

</td><td>

Name of the HR condition.

</td></tr><tr><td id="d374130e165">

**Table**

</td><td>

Table conditions are built on the HR profile \[sn\_hr\_core\_profile\] table only.Changing the table for client role assignment is not recommended.

</td></tr><tr><td id="d374130e177">

**Active**

</td><td>

Check box for enabling condition.**Note:** Deactivate at the client role assignment level and not the conditions level.

</td></tr><tr><td id="d374130e189">

**User column**

</td><td>

Together with the HR profile \[sn\_hr\_core\_profile\] table, filters users when evaluating a condition.

</td></tr><tr><td id="d374130e199">

**Condition**

</td><td>

Conditions the Assign HR Roles business rule uses to automatically assign a role to an employee. For example, the base system automatically assigns the New Hire role to a user when Employment type is:-   Full Time Employee or
-   Part Time Employee or
-   Temporary Employee and
-   Employment start date is after Today
 **Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr></tbody>
</table>6.  Click **Submit** or **Update**.

7.  From **Role**, click and select the HR role you want to automatically assign when the conditions are met.

8.  Click **Submit** or **Update** to save your changes.


**Parent Topic:**[Client roles](../concept/c_ClientRoles.md)

