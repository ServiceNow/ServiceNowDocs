---
title: Grant a time-limited user role
description: Learn how to assign a role to a user temporarily. Use this feature if you have a user who needs to perform a one-time action that is normally outside their roles.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Time-limited role, Managing roles, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Grant a time-limited user role

Learn how to assign a role to a user temporarily. Use this feature if you have a user who needs to perform a one-time action that is normally outside their roles.

## Before you begin

Role required: user\_admin

**Note:**

-   Time-limited user roles can be assigned to a user for a maximum of 5 days.
-   For a user, you can assign only `admin`, `snc_read_only`, `impersonator`, and \(or\) `snc_required_script_writer_permission` role as time-limited role.
-   Time-limited user roles are not displayed to the assigned users under the **Roles** tab of the user \(sys\_user\) record.
-   When the time-limited role assigned users log in, they see a notification regarding the role assignment.
-   Time-limited assignments can handle more than one role assignment to a user, even if the total duration across assignments is less than five days.

## About this task

**Warning:** Usage of Time-limited User Roles may consume access and use rights procured by customer and could result in additional subscription fees.

## Procedure

1.  Navigate to **All** &gt; **** &gt; **User Administration** &gt; **Time-limited user roles**.

2.  Select **New**.

3.  Fill in the fields on the form.

    All fields except Comments are mandatory.

<table id="table_dxg_2qw_m1c"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Determines if the time limited role assignment is active.

</td></tr><tr><td>

Role

</td><td>

The role assigned to the user. Only admin, impersonate, and snc\_readonly are allowed

</td></tr><tr><td>

User

</td><td>

The user to be assigned the time limited role

</td></tr><tr><td>

Start Time

</td><td>

The start time and date for the time limited role

</td></tr><tr><td>

End Time

</td><td>

The end time and date for the time limited role**Note:** **End Time** cannot be more than 5 days from the **Start Time**.

</td></tr><tr><td>

Comments \(Optional\)

</td><td>

Additional comments or information for the limited role assignment

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The specified user now has the role. They must complete their restricted task between the start time and the end time.

**Parent Topic:**[Time-limited role](time-limited-role-overview.md)

