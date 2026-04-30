---
title: Data protection
description: The data protection category addresses the elements of confidentiality, integrity and availability \(CIA\) of data.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Hardening settings, Platform Security]
---

# Data protection

The data protection category addresses the elements of confidentiality, integrity and availability \(CIA\) of data.

The CIA components are:

-   Confidentiality: Data is protected from unauthorized access in transit and at rest.
-   Integrity: Data is protected from unauthorized creation, deletion or change.
-   Availability: Data is accessible when required.

-   **[Remove remember me](sc-remove-remember-me.md)**  
Use the **glide.ui.forgetme** property to remove the **Remember Me** check box from the login page to prevent login information from being cached.
-   **[Require clearing pasteboard when backgrounding mobile application \[New in Security Center 1.3 and updated in 1.5\]](sc-require-clearing-pasteboard-when-backgrounding-mobile-application.md)**  
The **glide.sg.clear\_pasteboard\_when\_backgrounded** property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode. If it is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.
-   **[Restrict HR case updates from personal emails \[New in Security Center 1.3 and updated in 1.5\]](sc-restrict-hr-case-updates-from-personal-emails-plugin-applicability-human-resources-scoped-app.md)**  
Use the**sn\_hr\_core.restrict\_guest\_email** property to control whether a user can respond back to a HR case with their personal email.
-   **[Restrict oauth parameters to POST body \[New in Security Center 1.3\]](sc-restrict-oauth-parameters-to-post-body.md)**  
Use the **glide.oauth.allow.parameters.in.post.body.only** property to control the inbound OAuth authentication's acceptance of access tokens. Access tokens are sensitive and should only be accepted when located within a POST request body.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

