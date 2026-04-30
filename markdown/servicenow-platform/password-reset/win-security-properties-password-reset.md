---
title: Configure security settings for the Password Reset Windows Application
description: Configuring security settings for the Password Reset Windows Application.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure security settings for the Password Reset Windows Application

Configuring security settings for the Password Reset Windows Application.

## Security settings

-   The **glide.security.use\_csrf\_token** property setting allows the Password Reset Windows Application to retrieve a token for a secure communication with the datacenter instance.
-   The **CheckCertificateRevocationList** registry key default setting of **true** causes the Password Reset Windows Application to validate the server certificate before every communication. See [Customize the Password Reset Windows Application](../task/win-customize-password-reset.md) for details.
-   The **ServiceNowCertPublicKey** registry key contains the public key for the app. See [Customize the Password Reset Windows Application](../task/win-customize-password-reset.md) for details.

## Configure the glide.security.use\_csrf\_token property

To configure the **glide.security.use\_csrf\_token** property, a security\_admin elevated privilege is required.

Set the **glide.security.use\_csrf\_token** property to true \(Yes\). See the topic titled "High Security Settings" in [https://servicenow.com/docs](https://servicenow.com/docs).

The Windows local administrator performs the remainder of the installation procedure.

**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

