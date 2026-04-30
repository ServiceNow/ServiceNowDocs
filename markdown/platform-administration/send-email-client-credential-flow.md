---
title: Sending email using client credential flow
description: Use the client credential flow to send emails from Microsoft Exchange Online.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Sending email using client credential flow

Use the client credential flow to send emails from Microsoft Exchange Online.

Email account administrators, who are users that have the email\_account\_admin role, can configure ServiceNow AI Platform to send emails from an Microsoft Exchange Online tenant. The email account administrators can use SMTP by authenticating with a client ID and client secret or with certificates.

-   **[Activate OAuth support](../task/activate-oauth-plugin.md)**  
You can activate the Email:OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP plugin \(com.glide.email.oauth\) for Notifications if you have the admin role.
-   **[Configure client credential flow for SMTP OAuth2 using a client id and secret](../task/configure-client-id-secret-email-auth.md)**  
Configure outbound email accounts in a ServiceNow instance using a client id and secret.
-   **[Register an OAuth provider](../task/register-oauth-cred-flow.md)**  
Use the information generated during the Microsoft Azure account configuration to register an application as an OAuth provider.
-   **[Configure client credential flow for SMTP OAuth2 using certificate-based authentication](../task/config-credential-flow-certificate.md)**  
Configure an OAuth application profile to authenticate using certificates for outbound email.
-   **[Create an email account with SMTP OAuth2.0](../task/create-email-account-smtp.md)**  
Create an email account from Microsoft Exchange Online with SMTP OAuth2.0.

**Parent Topic:**[Advanced email setup](../../reference-pages/concept/c_AlternateEmailConfigurations.md)

