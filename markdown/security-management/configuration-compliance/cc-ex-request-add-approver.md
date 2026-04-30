---
title: Add an exception approver for Configuration Compliance
description: Add users to the approver groups so that you can request an exception for a remediation task in Configuration Compliance.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Add an exception approver for Configuration Compliance

Add users to the approver groups so that you can request an exception for a remediation task in Configuration Compliance.

## Before you begin

Role required: sn\_vulc.admin

## About this task

An exception request for a remediation task is approved using the default two-level approval workflow. Adding users to the first-level group is mandatory. If there are no users in the second level, the request is automatically approved after the first-level approval.

**Note:** If there's no first-level approver, an exception can't be requested.

**Note:** Upto Configuration Compliance v13.0, if there's no first-level approver, an exception can't be requested. However, starting from Configuration Compliance v13.0, if you are deploying the CC application for the first time, the flow designer for exception management is enabled by default. If you are already using the workflow, you can update to the flow designer. In both cases, you cannot change it back to workflow.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Groups**.

2.  In the Name column, search for **Exception**, and click **Exception Approver - Level 1 CC**.

    **Note:** Starting from Configuration Compliance v14.7.5, you can use the system properties provided in the base system for exception approvals via workflow in the System Properties \[sys\_properties\] table. So, when an exception request is raised via workflow, it’s sent for approval to the group IDs defined in the system property. Navigate to **All** &gt; **System Properties** and select **sn\_vulc.exception\_approver\_L1\_CC** or **sn\_vulc.exception\_approver\_L2\_CC** to change the property value.

3.  On the Group Exception Approver - Level 1 CC form, navigate to **Group Members** &gt; **New** \(or **Edit**\).

4.  On the form, fill in the fields.

<table id="table_m23_4gt_5lb"><thead><tr><th>

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

User's first name.

</td></tr><tr><td>

Last name

</td><td>

User's last name.

</td></tr><tr><td>

Title

</td><td>

User's job title. Enter a title or job description, or select one from the list.

</td></tr><tr><td>

Department

</td><td>

User's department.

</td></tr><tr><td>

Password

</td><td>

Password assigned to the user. This password can be permanent or temporary.

</td></tr><tr><td>

Password needs reset

</td><td>

Option to enable the user to reset the password to ensure security.

</td></tr><tr><td>

Locked out

</td><td>

Option to lock the user out of the instance and terminate all the user's active sessions. The system prevents users with the admin role from locking themselves out.

</td></tr><tr><td>

Active

</td><td>

Option to make this user active. Only you can see an inactive user in these areas:-   Lists of users
-   Selection list on reference fields \(magnifying glass icon\)
-   Auto-complete list that appears when you type into a reference field


</td></tr><tr><td>

Web service access only

</td><td>

Option to designate this user as a non-interactive user.

</td></tr><tr><td>

Internal Integration User

</td><td>

Option to designate this user as an internal integration user.

</td></tr><tr><td>

Email

</td><td>

User's email address.

</td></tr><tr><td>

Language

</td><td>

User's preferred language.

</td></tr><tr><td>

Calendar integration

</td><td>

Calendar used to manage the work schedule. For example, Outlook.

</td></tr><tr><td>

Time zone

</td><td>

Time zone for this user's location.

</td></tr><tr><td>

Date format

</td><td>

User's preferred format for dates.

</td></tr><tr><td>

Business phone

</td><td>

User's business phone.

</td></tr><tr><td>

Mobile phone

</td><td>

User's mobile phone.

</td></tr><tr><td>

Photo

</td><td>

Photo that you can upload by clicking on **Click to add...**.

</td></tr></tbody>
</table>5.  Click **Submit**.

6.  Repeat steps 1–5 to create an Exception Approver - Level 2 CC.

    **Note:** While creating a second level approver, select **Exception Approver - Level 2 CC**

7.  If you select **Edit**, move users from the **Collection** to the **Group Members** panel and click **Save**.

    The approver must navigate to **All** &gt; **Configuration Compliance** &gt; **My Approvals** and approve requests.


