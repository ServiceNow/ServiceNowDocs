---
title: Password management topics for ITSM Virtual Agent
description: End users can perform password reset, password change, and account unlock actions using Virtual Agent conversations.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Password management topics for ITSM Virtual Agent

End users can perform password reset, password change, and account unlock actions using Virtual Agent conversations.

End users can initiate a password management conversation with Virtual Agent by entering the keywords `Reset`, `Change`, `Unlock`, or `Password`.

Users who are not logged in can perform the Reset Password and Unlock Account actions. Users who are logged in can perform the Change Password, Reset Password, and Unlock Password actions.

Requirements:

-   Password Reset \(com.glideapp.password\_reset\) plugin
-   Password Reset Virtual Agent Conversations \(com.snc.password\_reset.virtual\_agent\) plugin

**Note:** In order for the password reset process to be available in Virtual Agent, ensure that you selected the **Enabled on Virtual Agent** check box in the Password Reset process configuration page.

For more information about the password reset process, see [Password Reset for Virtual Agent](https://www.servicenow.com/docs/access?context=password-reset-for-virtual-agent&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Verification options for password reset in Virtual Agent conversations

The following identity verification options are supported in Virtual Agent conversations. Custom verifications are not supported in Virtual Agent.

-   Personal data verification: User provides specific pieces of personal data.
-   Google Authenticator verification: User enters the generated code from the Google service Authenticator mobile app.
-   SMS code verification: User enters the code received via mobile text message.
-   Email code verification: User enters the code received via email.
-   Security question verification: User enters the configured security question answers.

For more information, see [Configure your Password Reset process](https://www.servicenow.com/docs/access?context=t_CreateAPasswordResetProcess&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Change Password

Users can request to change their user password.

This topic uses the Display Password Reset URLs [topic block](../reference/itsm-va-topic-blocks.md).

Basic flow:

1.  Virtual Agent asks the user to input their current password.
2.  If the current password matches, the user can enter a new password.
3.  Virtual Agent displays the password rules.
4.  If the user provides a password that meets the password requirements, Virtual Agent updates the password.
5.  If the user does not enter a valid password, the user must reenter the password.​

## Reset Password

Users can request to reset their user password.

This topic uses the Display Password Reset URLs [topic block](../reference/itsm-va-topic-blocks.md).

Basic flow:

1.  Virtual Agent sends identity verification information to the end user, based on the password reset process configuration.
2.  If the user successfully verifies their identity with the given inputs, Virtual Agent provides the reset steps.
3.  Virtual Agent displays the password rules.
4.  The user enters a new password, adhering to the password rules.​
5.  If the password does not meet the criteria, Virtual Agent prompts the user to reenter the password.
6.  Once the password meets the criteria, Virtual Agent resets the password.

## Unlock Account

Users can request to verify their locked user account.

This topic uses the Display Password Reset URLs [topic block](../reference/itsm-va-topic-blocks.md).

Basic flow:

1.  Virtual Agent sends identity verification information to the end user, based on the password reset process configuration.
2.  If the user successfully verifies their identity with the given inputs, Virtual Agent provides the verification information.
3.  Once the user has been identified and verified, Virtual Agent unlocks the user's account.

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](using-itsm-va.md)

