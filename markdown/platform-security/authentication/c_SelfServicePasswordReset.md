---
title: Password Reset
description: The default self-service Password Reset process enables a user to reset the password without assistance from service desk agents.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Local authentication, Authentication, Access Management]
---

# Password Reset

The default self-service Password Reset process enables a user to reset the password without assistance from service desk agents.

## The default self-service password reset flow

1.  If a user does not remember the password, the user can click the **Forgot Password?** link on the login screen.
2.  The Password Reset application starts. On the **Identity** page, the user identifies himself or herself by entering a **Username**.
3.  On the **Verify** page, the user proves that they are the person who is associated with the username. In this example, the user enters the email address that is associated with the user profile. The admin can configure a different verification method or can require additional verifications, for example, a personal question that only the user can answer.
4.  The **Reset** page tells the user to check email for instructions.
5.  The user opens the email and clicks the **here** link to reset the password. The link is valid for a period that you specify \(use the **password\_reset.request.expiry** property\).
6.  The **Reset Password** page guides the user to reset the password.

The default self-service Password Reset process \(`com.glideapp.password_reset`\) defines:

-   The URI that specifies where users are redirected when they click **Forgot Password?**. By default this value is **/$pwd\_reset.do?sysparm\_url=ss\_default**, which is the same value used in the **glide.security.password\_reset.uri** property. In previous releases, this value was set to **/reset\_password.do**.
-   The **Enable Password Reset URL** option, which specifies that the user should receive an email with a link to reset their password after they click **Forgot Password?**.
-   The Personal Data - Enter Email Address verification flow that specifies the three-step password reset flow.

See Configure your Password Reset process for instructions on accessing this form and configuring the fields.

**Note:**

-   This feature works for locally authenticated users who enter the username and password specified in their user record. Users logging in to the instance via an SSO solution or an LDAP integration cannot reset passwords using the example self-service Password Reset process.
-   The end user must enable and configure notification preferences. See Subscription-based notifications. Administrators can x[modify the email that is sent to the end user](../task/t_ModifyPasswordResetNotification.md).

