---
title: Register your PIV/CAC card for Service Portal login
description: Register your Personal Identity Verification \(PIV\) or Common Access Card \(CAC\) card so that you can log in to your organization's portal without entering a password.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/piv-cac-login.html
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Register your PIV/CAC card for Service Portal login

Register your Personal Identity Verification \(PIV\) or Common Access Card \(CAC\) card so that you can log in to your organization's portal without entering a password.

## Before you begin

To register your PIV/CAC card, an administrator must activate certificate-based authentication and then set up PIV/CAC authentication. For more information on this setup process, see [Personal Identity Verification \(PIV\) card or Common Access Card \(CAC\) based authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/certificate-based-authentication.md).

The following task assumes that you have a card reader connected to your system.

Role required: none

## Procedure

1.  Log in to a portal using your user name and password.

2.  In the portal, open your user profile.

3.  Insert your PIV/CAC card into a card reader and then select **Register your client certificate**.

    \[Omitted image "piv-cac-certificate.png"\] Alt text: Certificate selection for PIV/CAC authentication

4.  In the dialog box that appears, review the PIV/CAC certificate and then select **Register**.

    \[Omitted image "piv-cac-certificate-found.png"\] Alt text: Dialog box to register your PIV/CAC certificate

    If the registration is successful, the system provides the following alert message: `The PIV/CAC certificate has been successfully registered and linked to the user account.`

    Close the dialog box to finish.


## Result

The next time you log in to your portal, you can log in using your PIV/CAC card. To log in, insert your PIV/CAC card into a card reader and then select **Login with PIV/CAC card**.

\[Omitted image "piv-cac-login.png"\] Alt text: Login page with PIV/CAC option

To log out of the portal, select your avatar and then select **Logout**. Then, close the browser window.

**Parent Topic:**[Managing portal access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/portal-security.md)

**Related topics**  


[Login widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/login-widget.md)

