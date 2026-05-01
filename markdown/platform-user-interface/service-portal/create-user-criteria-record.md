---
title: Create a user criteria record for Service Portal
description: Create a user criteria record to apply to items in Service Portal and control user access to pages, widgets, widget instances, and search sources.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [User criteria for Service Portal, Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create a user criteria record for Service Portal

Create a user criteria record to apply to items in Service Portal and control user access to pages, widgets, widget instances, and search sources.

## Before you begin

Role required: admin

## About this task

You can [apply existing user criteria](widget-user-criteria.md) to records in Service Portal through Service Portal configuration \(**Service Portal** &gt; **Service Portal configuration**\). You can only create user criteria within the platform UI.

## Procedure

1.  In the navigation filter, type **Service Portal**.

2.  Select a page, widget, or widget instance record.

3.  In the related list at the bottom of the record, select the **Can View** or **Cannot View** tab, then click **New**.

    If a user criteria record is already created, you can click **Edit** to apply user criteria to the page, widget, or widget instance.

    User criteria records are stored in the \[user\_criteria\] table.

4.  Complete the fields on the form, as appropriate.

<table id="table_ojq_r1g_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the criteria record.

</td></tr><tr><td>

Users

</td><td>

User records to match access criteria.

</td></tr><tr><td>

Groups

</td><td>

Group records to match access criteria.

</td></tr><tr><td>

Roles

</td><td>

Roles to match access criteria.

</td></tr><tr><td>

Advanced

</td><td>

Displays or hides the **Script** field.

</td></tr><tr><td>

Script

</td><td>

Defines any additional criteria, and returns true or false. This field is available only if **Advanced** is selected. **Note:**

-   Because scripts are evaluated dynamically, including scripts in user criteria records can decrease performance.
-   Do not use a function with its name as answer, that is, answer\(\).


</td></tr><tr><td>

Application

</td><td>

Application scope for the user criteria record.

</td></tr><tr><td>

Active

</td><td>

Activate or deactivates this criteria record.

</td></tr><tr><td>

Companies

</td><td>

Companies to match access criteria.

</td></tr><tr><td>

Locations

</td><td>

Locations to match access criteria.

</td></tr><tr><td>

Departments

</td><td>

Departments to match access criteria.

</td></tr><tr><td>

Match All

</td><td>

Determines whether all elements from each populated criteria field must match. If selected, only users who match all criteria are given access. If cleared, the user must meet one or more of the set criteria to be given access. By default, this check box is cleared so that any condition met provides a match.

 For example, consider a user criteria record for the following:

-   Locations A or B
-   Company C or D
 With **Match All** selected, only users meeting all these conditions are matched. For example, a user with a location A and a company C.

 With **Match All** cleared, users meeting any of these conditions are matched. For example, a user with a location B.

 **Note:** If you select **Match All**, ensure that you do not create contradictory conditions that can never be met. For example, if all users in location A work for company G, then the conditions in this example can never be met.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[User criteria for Service Portal](../concept/user-criteria.md)

