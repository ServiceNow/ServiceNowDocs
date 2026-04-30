---
title: Password Reset in Service Operations Workspace reference
description: This reference topic provides additional information about the lists and forms that you use to configure and administer Password Reset.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Resetting password using Service-desk assisted Password Reset in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Password Reset in Service Operations Workspace reference

This reference topic provides additional information about the lists and forms that you use to configure and administer Password Reset.

## Identification methods

<table id="table_a4m_pqn_zbc"><thead><tr><th>

Error message

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User not enrolled

</td><td>

The user is not currently enrolled in the password reset process. The user must enroll to the password reset process to reset the password.

</td></tr><tr><td>

User not eligible for the process

</td><td>

The selected password reset process doesn’t apply to the user. You must select another password reset process to reset the password.

 Contact the system administrator for more assistance.

</td></tr><tr><td>

No password reset process found for the user

</td><td>

The user has not been assigned to any password reset processes. Contact the system administrator for more assistance.

</td></tr><tr><td>

Maximum verify attempts reached

</td><td>

The user has exhausted all the available password reset attempts. You can reset the password again after 8 hours.

</td></tr></tbody>
</table>## Verification methods

|Error message|Description|
|-------------|-----------|
|Email verification|
|Incorrect verification code entered|The verification code you have entered does not match the expected code.|
|Max resend attempts over|The error message indicates that you have exceeded the allowed number of attempts to resend a verification code.|
|SMS verification|
|Incorrect verification code entered|The verification code you have entered doesn’t match the expected code.|
|Max resend attempts over|You have exceeded the maximum number of attempts to resend a verification code.|
|Notify not enabled|Users are enrolled in the system to deliver notifications, however, the Notify feature responsible for sending the SMS messages isn’t enabled.|
|Security question|
|One or more answers incorrect|The user hasn’t provided the correct answers to the security questions or the agent might have entered the answers incorrectly.|
|Personal data verification|
|Incorrect answer entered|The user hasn’t provided the correct answers to the security questions or the agent might have entered the answers incorrectly.|
|Personal data confirmation|
|Incorrect answer|The user has not provided the email address as indicated.|
|Other errors|
|Multiple session error|Only one active session is allowed at a time to reset the password. Close the new session.|
|Technical error|You must logout and login to work on the password reset ticket.|
|Maximum verification attempts reached|You have exceeded the maximum number of attempts to verify the identity of the user.|

To reset a password for a user, refer [Reset password using service-desk assistance](../task/reset-password-sd-pr-sow.md).

**Parent Topic:**[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace](../concept/resetting-password-pr-sow.md)

