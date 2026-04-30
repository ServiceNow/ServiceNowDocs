---
title: Unlock the user account
description: You can unlock a blocked user to enable them to log in to their system.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Resetting password using Service-desk assisted Password Reset in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Unlock the user account

You can unlock a blocked user to enable them to log in to their system.

## About this task

This option is available only if the account is locked.

## Before you begin

Role required: password\_reset\_admin or password\_reset\_service\_desk

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation list, select **List**.

3.  Do one of the following:

    -   Navigate to list of incidents, and select an incident record.
    -   Navigate to list of interactions, and select an interaction record.
4.  Select the **More actions** icon, and then select **Reset password**.

    **Note:**

    -   Incident: The option is displayed only if the category of the incident is **Password Reset**, and is assigned to an agent having password reset service desk role.
    -   Interaction: The option is displayed only if an interaction is assigned to the agent having password reset service desk role.
5.  Identify the user.

    1.  In the **Identify** section, select the user from the drop-down menu.

    2.  Select the password reset process for the user.

        **Note:** You can only reset the password using a specified process for three times in a 24-hour time interval.

    3.  Select **Continue to verify**.

6.  Verify the user.

<table id="table_gwk_34n_23e"><thead><tr><th>

Verification method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email verification

</td><td>

A verification code is sent to the registered email address displayed. Select Send verification code and enter the code in the code in Enter verification code field.

 **Note:** You have only three attempts to perform an email verification.

</td></tr><tr><td>

SMS verification

</td><td>

A verification code is sent to the registered mobile numbers. The same verification code is sent to all the registered mobile numbers of the user. Select **Send verification code** and enter the code in the code in **Enter verification code field**.

 **Note:**

You have only three attempts to perform an SMS verification.

 If the Notify plugin isn’t active in your instance, you must select the service provider for the registered mobile number.

</td></tr><tr><td>

Security question verification

</td><td>

You must ask the security questions to the user and enter the answer of the security question in the respective fields.

</td></tr><tr><td>

Personal data verification

</td><td>

Enter the email address of the user in the Enter user’s email address field.

</td></tr><tr><td>

Personal data confirmation

</td><td>

The email address of the user is displayed. You must ask the email address of the user and confirm if the email address is correct.

</td></tr></tbody>
</table>7.  Select **continue to reset**.

8.  Select **Unlock account** option.


## Result

The user account is unlocked and they can access the system.

**Parent Topic:**[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace](../concept/resetting-password-pr-sow.md)

