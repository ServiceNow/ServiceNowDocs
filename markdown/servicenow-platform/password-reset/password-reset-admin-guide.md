---
title: Configuring Password Reset
description: The Password Reset application enables an end user to reset or change a password using a self-service process. Alternatively, your organization can implement a process that requires a service desk agent to reset passwords for end users.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring Password Reset

The Password Reset application enables an end user to reset or change a password using a self-service process. Alternatively, your organization can implement a process that requires a service desk agent to reset passwords for end users.

Watch the video: [Introducing Password Reset \(video\)](https://www.youtube.com/watch?v=6VbPR7CWF0M)

## Elements of the Password Reset process

You configure the following elements of the process for your organization:

-   A connection to the credential store for your organization where user credentials, like user name and password, are securely stored.
-   One or more user groups on the ServiceNow instance that can use the password reset process.
-   The type of identification that users must enter to identify themselves \(generally user name or email address\).
-   One or more verifications — Methods to verify the identity of the user. Here are some examples of the verifications:
    -   Question and answer: Answer a question that only the user knows \(based on the **Security Question verification** type\).
    -   Email: Enter a code number that was emailed to the user.
    -   SMS: Enter a code number that was texted to a mobile device.
    -   Authenticator app: Enter a code that is displayed on your Authenticator app on a mobile device.

        **Note:** Password Reset supports the following authenticator apps:

        -   Google Authenticator
        -   Microsoft Authenticator
        -   Cisco Duo

## Implementing a Password Reset process

1.  Plan your implementation: Consider all applicable organizational guidelines, security policies, and areas of the organization.
2.  Set up the elements of the password reset and password change processes according to the plan:
    -   Connection to the credential store.
    -   User groups that use the password reset process.
    -   Identification type to use.
    -   Verifications to use.
3.  In the service desk-assisted model, assign service desk agents to monitor and reset passwords as needed.
4.  Monitor password reset activity to identify security threats and to ensure compliance with the password policy requirements of your organization.

## Password Reset Windows Application

If a user forgets the password or gets locked out of a Windows computer, the user can reset the password directly from the Windows login screen. The user clicks the **Forgot Password?** link and is then guided through the process of resetting the password. To learn more, see [Password Reset Windows Application](win-password-reset-overview.md).

## Password Change application

The Password Change application extends the Password Reset application by letting admins define how users change their passwords. Users can change their passwords by using a self-service process.

1.  The user logs in to the instance and then selects the **All** &gt; **Password Reset** &gt; **Change Password** module or link from the user profile record. The user can also use the Password Change application on mobile devices.

    **Note:** By default, the dark theme doesn't apply to the Change Password form. Users can change the theme to the dark theme. For more information about the dark theme, see [Exploring themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

2.  On the Change Password form, the user selects a Password Reset process related to a credential store for which the user wants to change the password.
3.  The user enters the old password and the new password.

    **Note:**

    As the user enters a password, the **New Password** field shows a message indicating whether the characters entered in the field are correct or not. For example, if a user enters a character that doesn't fit the password policy, the **New Password** field shows an error message. The strength bar also shows the strength of the new password that the user has entered.

    The password policy \(granular password complexity\) helps create a correct, strong password on the Change Password form in the Next Experience and the Core UI.

4.  After all the password rules are met, the workflows validate the old password, and then implement the new one.
5.  The user types the new password again in the **Retype password** field, and selects **Change Password**.
6.  The system notifies the user that the password was changed.

-   **[Plan your Password Reset processes](../task/t_PlanPasswordReset.md)**  
To ensure security and efficiency, take the time to plan your Password Reset implementation.
-   **[Calculating the security score for password reset process](../reference/pwd-reset-process-recommend.md)**  
The security score of the password reset process is a critical metric for the password reset administrators to assess the strength and configuration of the password reset process.
-   **[Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md)**  
To implement the process, you configure credentials, verification methods and settings, and enrollment settings. You also specify to which users the process applies.
-   **[Customizing Password Reset processes](customizing-password-reset.md)**  
Password Reset scripts enable you to customize Password Reset by creating your own credential store, verification, and identification types, and extend them by defining extension scripts. You can also create a custom credential store type, custom verification type, or verification.
-   **[Reset a password or unlock a user account with service desk assistance](../task/reset-password-for-user.md)**  
Reset a password or unlock a user account by requesting the assistance of a service desk agent.
-   **[Integrate Password Reset with a Service Portal widget](../task/use-pwd-reset-in-service-portal.md)**  
You can enable a Password Reset process in a Service Portal page by adding a widget that opens the password reset pages inside the portal.
-   **[Integrate Password Reset with a CMS integration](../../security/task/t_PasswordResetCMSIntegration.md)**  
You can configure a site in the ServiceNow content management \(CMS\) application to define a single-site access point that includes the Password Reset service. For example, you can create an employee self-service site that provides Password Reset service.
-   **[Installing and configuring Password Reset Windows Application](install-configure-password-reset-windows-app.md)**  
Request the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin that enables connections to the Active Directory \(AD\) credential store types.
-   **[Enrolling in the Password Reset application to reset your password](c_EnrollInPasswordReset.md)**  
The self-service process is a typical process that you might follow to reset your password. Your experience might differ.

**Parent Topic:**[Password Reset](../reference/password-reset-landing-page.md)

