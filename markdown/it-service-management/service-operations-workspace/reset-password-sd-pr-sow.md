---
title: Reset password using service-desk assistance
description: Resetting the password enables the user to log in to their system and resume their work.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Resetting password using Service-desk assisted Password Reset in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Reset password using service-desk assistance

Resetting the password enables the user to log in to their system and resume their work.

## About this task

Resetting the password will both unlock the account and set a new password if the user account is locked.

Reset password in Service Operations Workspace 

## Before you begin

Role required: password\_reset\_service\_desk or password\_reset\_admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation list, select **List**.

3.  Do one of the following:

    -   Navigate to list of incidents, and select an incident record.
    -   Navigate to list of interactions, and select an interaction record.
4.  Select the **More actions** icon, and then select **Reset password**.

    **Note:** This option is displayed only to the agent having password reset service desk role who are assigned to the incident or an interaction.

5.  Identify the user.

    1.  In the **Identify** section, select the user from the drop-down menu.

    2.  Select the password reset process for the user.

        **Note:** You can only reset the password using a specified process for three times in a 24-hour time interval.

    3.  Select **Continue to verify**.

6.  Verify the user.

<table id="table_gwk_34n_zbc"><thead><tr><th>

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

8.  Reset the password.

    |Password reset method|Description|
    |---------------------|-----------|
    |Send email with instructions|An email is sent to the user with the password reset details.|
    |Auto-generate new password|The system automatically generates a new password for the user. You must read the password to the user.|
    |Reset password manually|You must enter a new password in Enter new password and Re-enter new password fields. Select Reset password. You must read the password to the user.|

9.  Select **Close**.

10. Select **Exit** in the confirmation modal displays to indicate that the password has been shared with the user.

    To know about errors that you encounter while you reset the password, refer [Password Reset in Service Operations Workspace reference](../reference/pr-sow-reference.md).


**Parent Topic:**[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace](../concept/resetting-password-pr-sow.md)

