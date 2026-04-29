---
title: Sensitive data redaction
description: Redact sensitive data such as Social Security number, credit card details, email address, phone number, and other personal information from inbound emails to help protect data and privacy.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Sensitive data redaction

Redact sensitive data such as Social Security number, credit card details, email address, phone number, and other personal information from inbound emails to help protect data and privacy.

When an inbound email is received, the sensitive data is masked. The sensitive data is redacted from the body, body\_text, subject in the \[sys\_email\] table after flows and inbound actions are executed.

**Note:** Data that has been redacted can’t be recovered.

Redact sensitive data option is available in inbound email actions once the following is activated:

-   [Sensitive Data Redaction for Inbound Emails plugin](../task/activate-data-redaction-emails-plugin.md)
-   [Data Discovery application](https://www.servicenow.com/docs/access?context=activate-data-discovery&version=australia&pubname=australia-platform-security&ft:locale=en-US)

    **Note:** Data Discovery application does not require a paid subscription when used along with sensitive data redaction for inbound emails plugin.


To create inbound email actions, see [Create an inbound email action](../task/t_CreatingAnInboundEmailAction.md).

Redaction time for the record can be viewed by checking the **Email Log**. For more information, see [System email log and mailboxes](https://www.servicenow.com/docs/access?context=r_EmailLogs&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **[Activate sensitive data redaction for inbound emails plugin](../task/activate-data-redaction-emails-plugin.md)**  
You can activate the Sensitive Data Redaction for Inbound Emails plugin \(com.glide.email\_inbound.redaction\) for Notifications if you have the admin role. The application installs related plugins if they are not already installed.
-   **[Customize behavior for sensitive data redaction](../task/customize-data-redaction.md)**  
Customize sensitive data redaction behavior by creating system properties for flows that are triggered by inbound emails, sys\_email record, and inbound actions.

**Parent Topic:**[Use Inbound email actions](use-inbound-email-action.md)

