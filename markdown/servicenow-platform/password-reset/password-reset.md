---
title: Password Reset
description: The Password Reset application enforces strong and secure passwords by enabling end users to reset or change their passwords either by using the self-service process or by requesting the assistance of a service desk agent.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset

The Password Reset application enforces strong and secure passwords by enabling end users to reset or change their passwords either by using the self-service process or by requesting the assistance of a service desk agent.

## Password Reset application features

-   **Manage enrollment**

    Automatically enrolls end users or allows manual enrollment.

-   **Verification types**

    Validates user authenticity with the help various verifications.

-   **Integrated plugins**

    Resets passwords directly from the Windows application and Microsoft Azure active directory \(AD\).

-   **Enrollment types**

    Enables end users to enroll in different password reset programs at their convenience.

-   **Homepages with a dashboard view**

    Password Reset has a new, modernized look and feel. For more information, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).


## Password Reset processes

Users with the password\_reset\_admin role configure how the process of resetting a password works for an end user.

-   Self-service process:

    Users reset passwords over the internet using a browser on any supported interface, including mobile devices.

-   Service Desk assisted process:

    Users request the assistance of a service desk agent, over the phone or in person. In this process, users don't reset passwords.


For more information, see [Configuring Password Reset](password-reset-admin-guide.md) and [Plan your Password Reset processes](../task/t_PlanPasswordReset.md).

## Self-service and Service Desk - assisted processes

In addition to configuring the connections, user groups, and verifications, you can specify one of the following operational methods for the organization:

-   **Self-service process**

    End users reset passwords using a browser on any supported interface, including mobile devices. They can provide the identifying information and answer questions or submit a securely delivered code number. The following example shows the default self-service process Password Reset flow:

    1.  If a user doesn't remember their password, the user clicks **Forgot Password** on the Login page.

        ![Forgot Password](../image/forgot-password.png)

    2.  The Password Reset application starts. On the Identify page, the user enters their identifying information \(generally the user name or email address\). The example includes the default CAPTCHA security feature. The user provides identification by entering a user name and CAPTCHA, and clicks **Next**.

        **Note:** Users can hear characters displayed in CAPTCHA by clicking the Speak the CAPTCHA icon \(![Speak the CAPTCHA icon](../image/speak-the-captcha-icon.png)\) displayed in the pop-up window for the Identify step.

        ![Identify page](../image/identify-enduser-page.png)

    3.  On the **Verify** tab, the user provides personal data associated with their user name. For example, the user can either enter the email address associated with the user profile or answer the security question that an administrator has configured. This information is specified while enrolling in the Password Reset process. The administrator can configure a different verification method. For example, a personal question that only the user can answer.

        **Note:** Other possible verifications require the user to enter a code number that was sent to a mobile device by SMS text, through the Google Authenticator app, or by email.

    4.  The Reset page tells the user to check email for instructions.
    5.  The user opens the email and clicks the link in the email to reset the password. The link is valid for a period of time that an administrator specifies by using the **password\_reset.request.expiry** property.
    6.  The Reset Password page guides the user to reset the password.
    7.  The system checks the credential store to verify the identity and then displays the new password on the Reset page.
-   **Service desk-assisted process**

    An end user requests the assistance of a Service Desk agent, over the phone or in person. The agent processes the request. Each Service Desk agent has the Password Reset admin Service Desk role. The Reset request form that the agent contains a **Select user** field and a **Select process** field. On the form, the agent can view all processes in the end user’s domain.


## Next steps

Based on your role, do these steps:

-   If you're an administrator, start [configuring Password Reset for your users.](password-reset-admin-guide.md)
-   If you're an end user who wants to reset a password, [start enrolling to reset your password](c_EnrollInPasswordReset.md).

