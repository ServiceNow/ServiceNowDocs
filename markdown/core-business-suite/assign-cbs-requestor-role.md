---
title: Assign the CBS Requestor role
description: Assign the CBS requestor role to enable users to access services and submit requests through Employee Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/assign-cbs-requestor-role.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Core Business Suite]
---

# Assign the CBS Requestor role

Assign the CBS requestor role to enable users to access services and submit requests through Employee Center.

## Before you begin

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite card, select **View product overview**.

3.  In the Configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the Configuration Console.

4.  From the Configuration Summary navigation menu, select **Requestor role** under Requester experience.

5.  Select **Requestor role configuration**.

    **Note:** The CBS Requestor role is preassigned to the CBS Requestors group.

6.  To add an existing user group:

    1.  In the Parent field, Search for and select the existing group.
    2.  Select **Update**.
7.  To add users to the group:

    1.  Under the Group Members tab, select **New**.
    2.  On the form, fill in the fields.

<table id="table_mzy_fzs_s3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

Unique identifier for the user.

</td></tr><tr><td>

First name

</td><td>

First name of the user.

</td></tr><tr><td>

Last name

</td><td>

Last name of the user.

</td></tr><tr><td>

Title

</td><td>

Job title of the user.

</td></tr><tr><td>

Department

</td><td>

Department the user belongs to.

</td></tr><tr><td>

Password needs reset

</td><td>

Select to require the user to reset their password at next login.

</td></tr><tr><td>

Locked out

</td><td>

Indicates whether the user account is locked out.

</td></tr><tr><td>

Active

</td><td>

Select to activate the user account. Selected by default.

</td></tr><tr><td>

Identity type

</td><td>

Type of identity assigned to the user.Default value is Human.

</td></tr><tr><td>

Internal Integration User

</td><td>

Select if the user is an internal integration account and not a human user.

</td></tr><tr><td>

Email

</td><td>

Email address of the user.

</td></tr><tr><td>

Language

</td><td>

Preferred language for the user interface.

</td></tr><tr><td>

Calendar integration

</td><td>

Calendar application integrated with the user account.Default value is Outlook.

</td></tr><tr><td>

Time zone

</td><td>

Time zone for the user.Default value is the system time zone.

</td></tr><tr><td>

Date format

</td><td>

Date display format for the user.Default value is the system date format.

</td></tr><tr><td>

Business phone

</td><td>

Business phone number of the user.

</td></tr><tr><td>

Mobile phone

</td><td>

Mobile phone number of the user.

</td></tr><tr><td>

Photo

</td><td>

Profile photo of the user.

</td></tr></tbody>
</table>    3.  Select **Submit**.
8.  On the Manage requestor role page, select **Mark as configured**.


**Parent Topic:**[Configure Core Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/configure-cbs.md)

