---
title: Create password reset process in Service Operations Workspace
description: Create configure credentials, verification methods and settings, and enrollment settings to create a password reset process.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up Service Desk assisted Password Reset in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Create password reset process in Service Operations Workspace

Create configure credentials, verification methods and settings, and enrollment settings to create a password reset process.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Overview**.

2.  On the **Admin Center** page, do one of the following:

    -   In the **Overview** tab, select the **Configure** button in the **Service Desk Assisted Password Reset** card.
    -   In the **Configurations** tab, select **Service Desk Assisted Password Reset** card.
3.  On the **Password reset process** card, select **Configure**.

    The default password process is displayed.

4.  To create a new password reset process, select **New**.

5.  On the form, fill in the fields.

<table id="table_sdt_2dm_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the password reset process

</td></tr><tr><td>

Description

</td><td>

Detailed information about the credential store.

</td></tr><tr><td>

Credential store

</td><td>

Credential store that contains user credentials and information.

</td></tr><tr><td>

Password reset

</td><td>

Option to apply the password reset process to a specific group or all users.

</td></tr><tr><td>

Enable account unlock

</td><td>

Option to unlock the account for all the users.

</td></tr><tr><td>

Apply to all users

</td><td>

Option to apply the password reset process to all the users.You can also select a specific group by deselecting this option, and add a group from **Groups** related list.

</td></tr></tbody>
</table>6.  Select **Submit**.

7.  Select the created password reset process.

8.  On the **Password Reset Details** tab, configure the following settings.

<table id="table_jl5_qfn_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum verifications

</td><td>

Number of verifications that a user must successfully submit to reset the password.

 If the number exceeds the number of required verifications, then the user must submit additional verifications to match the number specified for **Minimum verifications**.

</td></tr><tr><td>

Allow user to choose from optional verifications

</td><td>

Option to enable a user on the Verifications page during the process of resetting the password.

 The choice of optional verifications appears only if the **Minimum verifications** setting is greater than the number of mandatory verifications.

</td></tr><tr><td>

Auto-generate password

</td><td>

Option to auto-generate a new password for the user.

 When this check box is selected, you must select the **Email/SMS password** or **Display password** check box, or both.

</td></tr><tr><td>

User must reset password

</td><td>

Option to reset the user password immediately after logging in with the auto-generated password.

 **Note:** This check box is available only when the Auto-generate password check box is selected.

</td></tr><tr><td>

Display password

</td><td>

Option to display the new password on the screen.

 **Note:** Note: This check box is available only when the **Auto-generate password** check box is selected.

</td></tr><tr><td>

Email/SMS password

</td><td>

Option to send an email or SMS the new password to the user.

 **Note:** Note: This check box is available only when the **Auto-generate password** check box is selected.

</td></tr></tbody>
</table>9.  Right-click on the form header, and select **Save**.

10. For **Password Reset**, enter the required fields in the **Enrollment Reminder** tab.

11. Save your changes on the **Password Reset Process** form.

12. From the **Password Reset Process Groups** related list, select the user groups that use the process.

    The **Password Reset Process Groups** related list appears only if the **Apply to all users** check box is not selected.

13. Select the **Active** check box to enable the Password Reset process.

14. Right-click on the form header, and select **Save**.

    For more information on password reset process, see [Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md).


**Parent Topic:**[Setting up Service Desk assisted Password Reset in Service Operations Workspace](../concept/setup-password-reset-sow.md)

