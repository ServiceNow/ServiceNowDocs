---
title: Actions in Password Reset for Virtual Agent
description: The actions in the Virtual Agent use plugins.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Actions in Password Reset for Virtual Agent

The actions in the Virtual Agent use plugins.

-   Password Reset \(com.glideapp.password\_reset\): This plugin is active by default.
-   Password Reset for Virtual Agent \(com.snc.password\_reset.virtual\_agent\): You must install this plugin to use Password Reset for Virtual Agent.

For more information about creating your password reset process, see [Password Reset](../reference/password-reset-landing-page.md).

End users can initiate a password reset conversation with Virtual Agent by entering specific keywords. For example, when a user enters the keyword `Reset`, the Virtual Agent shows the **Reset Password** action. The users can select the action to initiate the password reset.

![Keyword in the Virtual Agent](../image/virtual-agent-password-reset-first.png "Keyword in the Virtual Agent")

![Virtual Agent displaying topics](../image/virtual-agent-password-reset.png "Virtual Agent displaying topics")

## Enrollment in Password Reset for Virtual Agent

You can let end users enroll for Password Reset verifications using the Virtual Agent. The Virtual Agent includes an enrollment topic and its topic blocks for each verification, such as SMS, email, security question, Soft PIN, or a third-party authenticator app. Users can select any of the topic blocks to enroll for verification.

You can modify the enrollment topic, but you must duplicate the default enrollment topic and then modify the duplicated topic.

Here's the enrollment flow in Virtual Agent:

1.  Users select the enrollment topic in Virtual Agent.
2.  Users select any one of these verification types:
    -   **Security questions**
        -   If users aren't enrolled, Virtual Agent displays the questions, and users need to select questions and give answers to them.
        -   If users are already enrolled, Virtual Agent shows options to the users to:
            -   Change answers to the existing questions
            -   Re-enroll
    -   **Soft PIN**
        -   If the user isn't enrolled, Virtual Agent displays rules that are followed by a Soft PIN question. Users enter a valid Soft PIN and complete the enrollment.
        -   If users are already enrolled, they get a message asking whether to update existing Soft PIN enrollment.

            If users select **Yes**, Virtual Agent displays rules that are followed by a Soft PIN question.

            Users must enter a valid Soft PIN to complete the enrollment.

            **Note:** When users change the existing Soft PIN, they must use a new Soft PIN that must differ from the previously existing Soft PIN.

    -   **Third-party authenticator app**

        -   If users aren't enrolled, they get a QR code and an alphanumeric code. Users can scan the QR code or enter the alphanumeric code in the authenticator app.
        -   If users are already enrolled, they get two options:

            -   Generate a new QR code and an alphanumeric code
            -   Disable multi-factor authentication
            If users select an option to generate a new QR, the new enrollment flow starts. If users select the other option, the multi-factor authentication gets disabled. If the multi-factor authentication is disabled, to re-enroll, users must enable it again.

        Password Reset supports the following third-party authenticator apps:

        -   Google Authenticator
        -   Microsoft Authenticator
        -   Cisco Duo
    -   **Email and SMS**
        -   If users aren’t enrolled, they can add new mobile devices for SMS verification or can add an email address for email verification.
        -   If users are already enrolled, they can view the list of enrolled mobile devices for SMS verification, or they can view an email address. For SMS, the users can verify, remove, or authorize mobile devices. For email, the users can verify or authorize the email address.
3.  Users complete the enrollment.

## Verification options for Password Reset for Virtual Agent conversations

The following verification options are supported in Virtual Agent conversations. Custom verifications are not supported in Virtual Agent.

-   Personal data: The user provides specific pieces of personal data.
-   Authenticator app: The user enters the generated code from the an authenticator app on a mobile device.
-   SMS:The user enters the code received on a mobile phone.
-   Email:The user enters the code received in an email.
-   Security question verification: The user enters the answers for the security question.

## Soft PIN expiration framework for Password Reset

Virtual Agent supports expiration framework to account for Soft PIN verification during Password reset. As an end-user, you can use the existing Virtual Agent topic to enroll for Soft PIN enrollment to:

-   Re-enroll when your Soft PIN has expires.
-   Inform you of the number of days from the time you setup a new Soft PIN after which your token expires.
-   Reset Soft PIN to account for history policies.
-   Configure the topic to ask for password before proceeding to reset your Soft PIN.

## Reset password conversation flow for Virtual Agent

1.  Virtual Agent sends identity verification information to the end users based on the password reset process configuration.
2.  Virtual Agent provides the reset steps if users successfully verify themselves with the given inputs.
3.  Virtual Agent displays the password rules.
4.  The user enters a new password, adhering to the password rules.
5.  Virtual Agent prompts the user to reenter the password if the password does not meet the criteria.
6.  Once the password meets the criteria, the Virtual Agent resets the password.
7.  Users then log in using the new password.

## Password reset flow using interactive voice response \(IVR\)

A user can reset a password using interactive voice response \(IVR\). For example, by using a phone call. A user gets the instructions for verification on a phone call. Once the verification is complete, the user receives an auto-generated password or an email containing a URL, which the user can use to reset the password based on the configuration of the process.

After resetting your password, the newly auto-generated password is spoken over IVR. If the Password Reset process is configured with an email or SMS, the password is also sent to the registered email and SMS.

The following verification types are supported over IVR:

-   Authenticator app
-   SMS
-   Email

You can use the **sn\_pwdreset\_va.supported\_channels** system property to enable the IVR or Microsoft Teams or both.

**Note:** By default, the minimum character length is 8 characters. The maximum length in the password policy must be modified for a better experience over IVR.

## Change password conversation flow for Virtual Agent

1.  The user initiates the Change Password action. The user selects the password reset process, or if only one process is available, the process is selected automatically.
2.  Virtual Agent prompts the password guidelines or rules.
3.  The user enters the old password, enters the new password, confirms the new password, and submits the request.
4.  Virtual Agent shows the request status whether the password is changed or not.
5.  If the password is changed, the users can use the new password to log in.

## Unlock account conversation flow for Virtual Agent

When a user account is locked, the user can't log in to the account. But using the Virtual Agent, the user can unlock the account and log in.

1.  Virtual Agent sends identity verification information to the end user based on the password reset process configuration.
2.  Virtual Agent provides the verification information if the user successfully verifies their identity with the given inputs.
3.  Once the user has been identified and verified, the Virtual Agent unlocks the user's account.

**Note:** Users can also use the Microsoft Teams channel to unlock accounts and reset passwords.

