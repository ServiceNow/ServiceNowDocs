---
title: Configure a credential store type to support third-party password auto-generation
description: Enable the subflows in credential store type to support third-party password auto-generation.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing Password Reset processes, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a credential store type to support third-party password auto-generation

Enable the subflows in credential store type to support third-party password auto-generation.

## Before you begin

Role required: password\_reset\_credential\_manager, password\_reset\_admin, or admin

## About this task

Users can easily reset their passwords for the credential stores that don't have REST APIs to reset the password. For example, the password reset subflows support Robotic Process Automation. The Password Reset process can be automated with a Robotic Process Automation robot to reset the password of an application that does not have an API to reset the password.

For more information about Robotic Process Automation, see Robotic Process Automation \(RPA\) Hub.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Credential Store Types**.

2.  Open the credential store type.

3.  To use password reset subflows in the Integration Hub, leave the **Use Flow** check box selected.

4.  In the **Password reset flow** field, enter a required value for the password reset subflow.

5.  From the **Password Delivery Mechanism** list, select **Reset flow doesn’t accept password as input**.

6.  If you want your users to change the password immediately after signing in post password reset, select the **Supports Force Password Change On First Log In** check box.

    **Note:** Ensure that the **User must reset password** check box is selected on the Password Reset Process form of the associated process. But these settings of changing passwords after first sign-in post reset work only if the credential store you are configuring supports the settings.

7.  Click **Update** or save the changes.


**Parent Topic:**[Customizing Password Reset processes](../concept/customizing-password-reset.md)

