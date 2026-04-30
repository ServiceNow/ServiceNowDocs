---
title: Limitations of the Password Reset Windows Application
description: The Password Reset Windows Application has a few limitations.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Limitations of the Password Reset Windows Application

The Password Reset Windows Application has a few limitations.

-   The Password Reset Windows Application doesn't support custom verifications.
-   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface.
-   The Password strength indicator is not supported.
-   For some verification types, you can use only one verification. Custom verifications are not supported. For more information, see [Password Reset verifications](../concept/c_PWRVerifications.md).
-   Custom UI macros configured on the **Process** &gt; **Advanced** page are not supported \(for example, entry, success, or failure macros\). The system displays only the default success and failure messages.
-   The Password Reset Windows Application supports newline characters in the **Password rule hint** text. Other formatting is not supported \(bold, underline, and hyperlink\). For more information, see [Configure the connection to a credential store for the Password Reset processes](../task/t_CreateACredentialStore.md).

**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

