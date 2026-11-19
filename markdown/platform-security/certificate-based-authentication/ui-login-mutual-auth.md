---
title: Log in using Certificate-based authentication
description: After your administrator sets up Certificate-based authentication, you can register the client certificate and log in using your PIV \(Personal Identity Verification\) or CAC \(Common Access Card\) card.Before you log in to ServiceNow AI Platform using your PIV or CAC card, you must register the client certificate of your PIV or CAC card. If you are not able to register the client certificate, contact your administrator. Your administrator can also register the client certificate of your PIV or CAC card.You can log in with your PIV or CAC card instead of user name and password when Certificate-based authentication is enabled on ServiceNow AI Platform.View and delete client certificates associated with your account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/certificate-based-authentication/ui-login-mutual-auth.html
release: zurich
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Certificate-based authentication, Authentication, Access Management]
---

# Log in using Certificate-based authentication

After your administrator sets up Certificate-based authentication, you can register the client certificate and log in using your PIV \(Personal Identity Verification\) or CAC \(Common Access Card\) card.

## Register client certificate for your PIV or CAC card

Before you log in to ServiceNow AI Platform using your PIV or CAC card, you must register the client certificate of your PIV or CAC card. If you are not able to register the client certificate, contact your administrator. Your administrator can also register the client certificate of your PIV or CAC card.

### Before you begin

-   Make sure that Certificate-based authentication is enabled.
-   Make sure that a card reader is connected to your computer and your PIV or CAC card is inserted.
-   Role required: none

### About this task

If you need an admin to register your client certificate, see [Map PEM certificate to user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/certificate-based-authentication/set-up-mutual-auth.md).

### Procedure

1.  Log in to ServiceNow AI Platform using your user name and password.

2.  Click your name from the **User Menu** and select **Profile**.

3.  From the **Related Links**, click **Register client certificate**.

    If a valid is certificate is available, the following message displays:

    \[Omitted image "register-piv-cac-card-cert.png"\] Alt text: register a client certificate for PIV or CAC card

4.  Click **Register**.

    After the registration is successful, the following message displays:

    `The PIV/CAC certificate has been successfully registered and linked to the user account.`

    \[Omitted image "piv-cac-card-register-success.png"\] Alt text: certificate registered successfully for a PIV or CAC card

    The next time you log in to your ServiceNow AI Platform, you can log in using your PIV or CAC card. For more information, see [Log in to ServiceNow AI Platform using PIV or CAC card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/certificate-based-authentication/ui-login-mutual-auth.md).


## Log in to ServiceNow AI Platform using PIV or CAC card

You can log in with your PIV or CAC card instead of user name and password when Certificate-based authentication is enabled on ServiceNow AI Platform.

### Before you begin

-   Role required: none
-   Make sure that Certificate-based authentication is enabled.
-   Make sure that a PIV or CAC card reader is connected to your computer.
-   Make sure that a client certificate of your PIV or CAC card is mapped to you. For more information, see [Register CA certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/certificate-based-authentication/set-up-mutual-auth.md).

### Procedure

1.  Insert your PIV or CAC card into the card reader.

2.  Navigate to your instance in a browser.

    Browser prompts for a PIN for your PIV or CAC card.

3.  Enter the PIN of your PIV or CAC card in the browser prompt.

    **Note:** If you forget your PIN, contact your administrator.

4.  If you enter a correct PIN, the browser displays a prompt to select a certificate.

    \[Omitted image "client\_certificate\_prompt.png"\] Alt text: Browser prompt to select a client certificate.

5.  Select a certificate from the browser prompt.

    If the certificate is valid and mapped to you, you are redirected to the login page.\[Omitted image "piv\_cac\_card\_login.png"\] Alt text: Login page with PIV or CAC card option

6.  Click **Log in with PIV/CAC card** button.

    To log out of the ServiceNow AI Platform, you must remove the PIV or CAC from the card reader and then close the browser.


## Manage your client certificates

View and delete client certificates associated with your account.

### Before you begin

-   Make sure that Certificate-based authentication is enabled.
-   Role required: none

### Procedure

1.  Log in to ServiceNow AI Platform using your user name and password.

2.  Click your name from the **User Menu** and select **Profile**.

    \[Omitted image "user\_menu\_profile.png"\] Alt text: Options in the user menu

3.  From the **Related Links**, click **Manage your client certificates**.

    The User Client Certificates \[sys\_user\_certificate\] table opens and displays certificates that are associated with your account.

4.  View or delete certificates associated with your account.


