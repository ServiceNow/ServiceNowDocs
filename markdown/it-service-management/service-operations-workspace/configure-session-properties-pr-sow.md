---
title: Configure the session properties
description: Configure the password reset properties based on the requirement.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up Service Desk assisted Password Reset in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the session properties

Configure the password reset properties based on the requirement.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Overview**.

2.  On the **Admin Center** page, do one of the following:

    -   In the **Overview** tab, select the **Configure** button in the **Service Desk Assisted Password Reset** card.
    -   In the **Configurations** tab, select **Service Desk Assisted Password Reset** card.
3.  On the **Session properties** card, select **Configure**.

4.  On the form, fill in the fields.

<table id="table_mwh_kln_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Password Reset Global Properties

</td></tr><tr><td>

Email template for enrollment reminder emails. The instance can send email reminders to users who are not yet enrolled in the Password Reset process.

</td><td>

Template to use for the email messages that remind users to enroll for the password reset process.

</td></tr><tr><td>

Workflow polling frequency \(frequency, in milliseconds, that the application polls the password reset/change workflow for completion\)

</td><td>

Time period in milliseconds between checks on status of the Password Reset workflow.

 -   Type: integer
-   Default value: 500


</td></tr><tr><td>

Workflow expiration \(time, in milliseconds, before the password reset/change workflow expires\)

</td><td>

Maximum wait time in milliseconds for the workflow to complete. The workflow is triggered during the password reset request when the user clicks **Submit**.

 -   Type: integer
-   Default value: 90000


</td></tr><tr><td colspan="2">

Password Reset Request Properties

</td></tr><tr><td>

Number of unsuccessful attempts allowed for resetting/changing password

</td><td>

Number of password reset attempts a user is allowed before they are locked out for a period determined by the value in max\_attempt\_window.

 -   Type: integer
-   Default value: 3 \(attempts\)


</td></tr><tr><td>

Number of minutes a user needs to wait to reset/change password after the last successful reset/change

</td><td>

Time period that users are blocked or prevented from changing their passwords after trying the maximum number of times.

 -   Type: integer
-   Default value: 1440 \(minutes\)


</td></tr><tr><td>

Number of minutes a user needs to wait to start a reset request after the last successful unlock account.

</td><td>

Time period that a user must wait after successfully resetting the password to reset the password again.

 -   Type: integer
-   Default value: 1440 \(minutes\)


</td></tr><tr><td>

Number of minutes before a password reset request expires

</td><td>

Time period during which a user must perform the Password Reset process.

 -   Type: integer
-   Default value: 10 \(minutes\)


</td></tr><tr><td>

Maximum number of times that a user can receive "Reset Password" link via email, in a span of 24 hours. The upper limit is 5.

</td><td>

Maximum number of times a user can receive emails containing a link for resetting a password in a duration of 24 hours.

</td></tr><tr><td colspan="2">

Password Reset Security Question Properties

</td></tr><tr><td>

Number of security questions required during the password reset request

</td><td>

Number of security questions that are displayed on the Verify page while a user is attempting to reset the password. The user must answer all questions correctly to verify identity.

</td></tr><tr><td>

Number of security questions required during enrollment

</td><td>

Number of questions that a user must provide answers to while enrolling for the Password Reset process.

</td></tr><tr><td>

Minimum length requirement for security answers

</td><td>

Minimum number of alphanumeric characters that the user must enter in the answer text box for any security question.

</td></tr><tr><td colspan="2">

Password Reset SMS Code Properties

</td></tr><tr><td>

Maximum number of SMS codes sent for verification per day

</td><td>

Maximum number of SMS codes that are sent to a user within one 24-hour period. The 24-hour period begins when a user clicks **Send Code**.

</td></tr><tr><td>

Number of minutes before the user can attempt to send another SMS code for verification

</td><td>

Time that must pass before another SMS code can be sent to a user.

</td></tr><tr><td>

Number of digits in the SMS code sent to the user

</td><td>

Number of characters required for a user to reset their password.

</td></tr><tr><td>

Number of minutes before the SMS code expires

</td><td>

Time, in minutes, until the SMS code sent to the user expires.

</td></tr><tr><td>

Use Notify for SMS code notification for enrollment and verification

</td><td>

Support for SMS channel used for notifying users for password reset enrollment and verification.

</td></tr></tbody>
</table>5.  Select **Save**.


**Parent Topic:**[Setting up Service Desk assisted Password Reset in Service Operations Workspace](../concept/setup-password-reset-sow.md)

