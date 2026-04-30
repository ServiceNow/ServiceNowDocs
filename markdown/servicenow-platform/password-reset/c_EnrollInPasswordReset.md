---
title: Enrolling in the Password Reset application to reset your password
description: The self-service process is a typical process that you might follow to reset your password. Your experience might differ.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enrolling in the Password Reset application to reset your password

The self-service process is a typical process that you might follow to reset your password. Your experience might differ.

## Example experience of the self-service process

1.  On the Login page, click the **Forgot Password** link to start the process.

    ![Login page](../image/forgot-password.png "Login page")

2.  On the Identify page, enter your identifying information \(generally your user name or email address\). The example includes the CAPTCHA security feature.

    ![Identify page](../image/identify-enduser-page.png "Identify page")

3.  On the Verify page, verify your identity by providing your verification information. The admin configured the method of verification and can require multiple verifications. In the following example, the admin has configured the Security Questions verification. You must answer questions to prove your identity. \(Earlier, while enrolling for the password reset process, you selected these questions and provided secure, private answers.\) Other possible verifications require you to enter a code that was sent to a mobile device by SMS text, through the authenticator app, or by email.

    ![Verify page](../image/verify-enduser-page.png "Verify page")

4.  The system checks the credential store to verify your identity and then displays the new password on the Reset page.

    ![Reset page](../image/reset-enduser-page.png "Reset page")


## Enroll in the Password Reset program

Some organizations auto-enroll users in a Password Reset program. Your organization could offer end users the option to enroll for one or more methods of verifying your identity when resetting the password. End users can enroll for most Password Reset programs on a mobile device.

**Note:** By default, the dark theme doesn't apply to the Password Reset Enrollment form. Users can change the theme to the dark theme. For more information about the dark theme, see [Exploring themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

End users might enroll for any combination of the following methods:

-   **Verify your identity using an authenticator app**
    -   You enroll on a computer that you normally use to access the instance \(you use an authenticator app to reset your password, but can’t use an authenticator to enroll for Password Reset Windows Application.\). After you’ve enrolled, you install an authenticator app on one or more devices and then authorize the devices for authenticator verification.
    -   Later, when you want to reset your password, read the authenticator code on your device and then enter the code on the web page to verify your identity.
-   **Verify your identity using an SMS code \(SMS verification\)**
    -   To enroll, you authorize a mobile device for SMS verification.
    -   Later, when you want to reset your password, you get a code on the device and enter the code on the web page to verify your identity.
-   **Verify your identity using an emailed code**
    -   To enroll, you authorize one or more email addresses.
    -   Later, when you want to reset your password, the system sends a code to the email address. You then enter the code on the web page to verify your identity.
-   **Verify your identity using security questions verification**
    -   To enroll, you choose multiple questions that only you can answer \(like the name of your first pet\) and then supply answers. The system stores your answers securely.
    -   Later, when you want to reset your password, the system presents one or more of the questions. You answer the questions to verify your identity.

-   **[Enroll for the Password Reset program using an authenticator](../task/authenticator-app-verification.md)**  
Verify your identity while resetting your password by enrolling for the Password Reset program using a third-party authenticator app.
-   **[Enroll for the Password Reset program using SMS codes](../task/t_EnrollUsingSMS.md)**  
To verify your identity while resetting your password, you can use a code \(the SMS code\) that was delivered to your mobile phone or device. You can enroll on a mobile device.
-   **[Enroll for the Password Reset program using emailed codes](../task/enroll-email-verification.md)**  
To verify your identity while resetting your password, you enter a code that was sent to your email address. You can enroll for this program on a mobile device.
-   **[Enroll for the Password Reset program using questions and answers](../task/t_EnrollUsingASecurityQuestion.md)**  
Your organization might ask you to select the questions to use when resetting your password. You select the questions and provide answers that only you know. At another time, when you reset your password, your answers verify your identity. You can enroll on a mobile device.
-   **[Enroll for the Password Reset program using Soft PIN](../task/enroll-pwr-program-soft-pin.md)**  
Verify your identity while resetting your password by using a Soft PIN. To use it, you must enroll for the verification using a Soft PIN.
-   **[Reset your password on Windows systems](../task/t_RsttPassDeskRst.md)**  
If your organization uses the Password Reset Windows Application, you can reset your password directly from your Windows login screen.

**Parent Topic:**[Configuring Password Reset](password-reset-admin-guide.md)

