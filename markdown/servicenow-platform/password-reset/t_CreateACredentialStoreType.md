---
title: Create a credential store type for Password Reset
description: Create a custom credential store type when the base-system types do not meet your needs.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Customizing Password Reset processes, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a credential store type for Password Reset

Create a custom credential store type when the base-system types do not meet your needs.

## Before you begin

Role required: password\_reset\_credential\_manager

## About this task

You can also configure a credential store type to work independently with the password reset, password change, and unlock password actions.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Credential Store Types**.

2.  Click **New**.

3.  In the **Name** field, enter the name for the credential store type.

4.  In the **Description** field, enter the description for the credential store type.

5.  To use password reset subflows in Integration Hub, leave the **Use Flow** check box selected.

    **Note:** See [Customize password reset processes and integrate third-party credential services](setup-pwd-reset-ihub.md) for information on creating provider-specific subflows.

6.  Select the **Supports history check** check box to determine whether the credential store supports the history policy capability.

    If selected, only then the password\_reser\_admin can disable or enable this feature through a credential store record.

7.  Select the subflows created for the third-party application.

    **Note:** See [Customize password reset processes and integrate third-party credential services](setup-pwd-reset-ihub.md) for information on creating provider-specific subflows.

<table id="table_mpv_f3s_f5b"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base Alias

</td><td>

A connection and credential alias that is used in the subflows of this credential store type.

 This is the default alias used by the subflows while making an external call.

**Note:** If you want to override the default alias, use the child alias property of the credential store.

</td></tr><tr><td>

Password change flow

</td><td>

Changes the password of an authenticated and unlocked user account to the provided new password. Verifies that the new password conforms to the password format and history policies. Displays an error if the user is not authenticated or is locked out.

 Use the Password Reset flow to unlock a locked user account and require a password change.

</td></tr><tr><td>

Unlock user flow

</td><td>

Defines the process to unlock a user.

 If a credential store supports the unlock user flow, the **Get user lock state flow** field becomes a required field. But when a credential store doesn’t support the unlock user flow, you can still set up the user lock state flow.

</td></tr><tr><td>

Get user lock state flow

</td><td>

Retrieves the lock status of an account specific to the credential store.

</td></tr><tr><td>

Connection test flow

</td><td>

Defines how to test the connection.

</td></tr><tr><td>

Password reset flow

</td><td>

Unlocks the specified user account. Expires the current password and changes the password to the provided new password if it conforms to the password format and history policies. If it doesn't conform, a warning is displayed.

**Note:** In the case of an Robotic Process Automation setup, the subflow doesn’t reset the password immediately but only pushes the request into the Robotic Process Automation queue and the status is displayed as **Pending**.

</td></tr><tr><td>

Password Delivery Mechanism

</td><td>

Sets the mechanism such as whether to accept the password as input or not. For example, in the case of the credential store for which Robotic Process Automation functionality is required, Robotic Process Automation can’t accept the password from the Password Reset application for security purposes. So, for Robotic Process Automation subflows, the **Reset flow doesn't accept password as input** value must be selected. That means, while users create a reset password request, they are not asked to enter passwords of their choice.

 **Note:** This feature is applicable only to the password reset action. If for a credential store, the reset flow doesn’t accept a password, which is configured through the password delivery mechanism, then all the fields for password policy and password generation are hidden on the related credential store form. For example, **Enable password policy**, **Password policy**, **Enable Password Strength**, **Strength rule**, and **Auto-generate password**.

</td></tr><tr><td>

Supports Force Password Change On First Log In

</td><td>

When selected, notifies the user to change the password when the user signs in for the first time with the new password that the user receives after the password reset action is completed.

 **Note:** Based on this setting, the fields on the Password Reset Process form change. For example, when a password reset administrator selects the **Auto-generate password** check box on the Password Reset Process form, the form displays the **User must reset password** field. So, it depends on the password reset administrator whether to prompt users to change their auto-generated password or not even if the **Supports Force Password Change On First Log In** check box is selected.

</td></tr></tbody>
</table>8.  If you want to use workflows, clear the **Use Flow** check box to use the password reset workflows in Orchestration.

    **Note:**

    -   The workflows have been deprecated. Use the subflows by leaving the **Use Flow** check box selected.
    -   The workflows are available only if you have upgraded from the previous releases.
    |Field|Description|
    |-----|-----------|
    |Password Reset workflow|Defines the credential store processing. Password Reset workflows are available to use as a model. Provide scripts for each of the activities defined for the subflow. For more information about how to create a workflow, see [Create a workflow](../../workflow-administration/task/t_CreateAWorkflow.md). For installed workflows, see [Installed with Password Reset](../reference/r_InstalledWithPasswordReset.md).|
    |Connection test workflow|Defines how to test the connection. Connection test workflows are available to use as a model. If you create a connection test subflow, provide scripts for each of the activities defined for the subflow. For installed workflows, see [Installed with Password Reset](../reference/r_InstalledWithPasswordReset.md).|
    |Get user lock state workflow|Defines how to get the user lock state. Get user lock state workflows are available to use as a model. Provide scripts for each of the activities defined for the subflow. For more on how to create a workflow, see [Create a workflow](../../workflow-administration/task/t_CreateAWorkflow.md). For installed workflows, see [Installed with Password Reset](../reference/r_InstalledWithPasswordReset.md).|
    |Unlock user workflow|Defines how to unlock a user. Unlock user workflows are available to use as a model. If you create a connection test subflow, provide scripts for each of the activities defined for the subflow. For installed workflows, see [Installed with Password Reset](../reference/r_InstalledWithPasswordReset.md).|

9.  Click **Submit**.


**Parent Topic:**[Customizing Password Reset processes](../concept/customizing-password-reset.md)

