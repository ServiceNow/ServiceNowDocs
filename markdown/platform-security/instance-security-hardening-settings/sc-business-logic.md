---
title: Business Logic
description: This category looks at the logic and flow unique to each application with general secure principles. Specifically ensure that the intended sequence of business logic flow cannot by bypassed, that limits exist to detect and prevent automated attacks, and that protections against spoofing, tampering, information disclosure and elevation of privilege attacks exist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-business-logic.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Hardening settings, Platform Security]
---

# Business Logic

This category looks at the logic and flow unique to each application with general secure principles. Specifically ensure that the intended sequence of business logic flow cannot by bypassed, that limits exist to detect and prevent automated attacks, and that protections against spoofing, tampering, information disclosure and elevation of privilege attacks exist.

The following are some security controls that an administrator can configure to restrict unauthorized access to sensitive entities within the ServiceNow AI Platform.

-   **[Limit max comments per user per day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-limit-max-comments-per-user-per-day.md)**  
Configure the **sn\_kb\_social\_qa.max\_comments\_per\_user\_daily** property to restrict the number of QA comments per day.
-   **[Limit max subscriptions per user per day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-limit-max-subscriptions-per-user-per-day.md)**  
Configure the **sn\_kb\_social\_qa.max\_subscriptions\_per\_user\_daily** property to limit the max number subscriptions a user can subscribe to in a day.
-   **[Minimize SMTP Recipient Quantity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-max-smtp-recipients.md)**  
The **glide.email.smtp.max\_recipients** specifies the maximum number of recipients the instance can list in the **To:** line for a single email notification.
-   **[Timeout Guest Sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-timeout-guest-sessions.md)**  
Use a system property to control the inactive session timeout for unauthenticated users.
-   **[Validate remote host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-validate-remote-host.md)**  
Set the property to true to prevent bad actors from using internal port scanning in your network.

**Parent Topic:**[Hardening settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/security-hardening-settings.md)

