---
title: Business Logic
description: This category looks at the logic and flow unique to each application with general secure principles. Specifically ensure that the intended sequence of business logic flow cannot by bypassed, that limits exist to detect and prevent automated attacks, and that protections against spoofing, tampering, information disclosure and elevation of privilege attacks exist.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Hardening settings, Platform Security]
---

# Business Logic

This category looks at the logic and flow unique to each application with general secure principles. Specifically ensure that the intended sequence of business logic flow cannot by bypassed, that limits exist to detect and prevent automated attacks, and that protections against spoofing, tampering, information disclosure and elevation of privilege attacks exist.

The following are some security controls that an administrator can configure to restrict unauthorized access to sensitive entities within the ServiceNow AI Platform.

-   **[Limit max comments per user per day](sc-limit-max-comments-per-user-per-day.md)**  
Configure the **sn\_kb\_social\_qa.max\_comments\_per\_user\_daily** property to restrict the number of QA comments per day.
-   **[Limit max subscriptions per user per day](sc-limit-max-subscriptions-per-user-per-day.md)**  
Configure the **sn\_kb\_social\_qa.max\_subscriptions\_per\_user\_daily** property to limit the max number subscriptions a user can subscribe to in a day.
-   **[Minimize SMTP Recipient Quantity \[Updated in Security Center 1.3\]](sc-max-smtp-recipients.md)**  
The **glide.email.smtp.max\_recipients** specifies the maximum number of recipients the instance can list in the **To:** line for a single email notification.
-   **[Timeout Guest Sessions](sc-timeout-guest-sessions.md)**  
Use a system property to control the inactive session timeout for unauthenticated users.
-   **[Validate remote host](sc-validate-remote-host.md)**  
Set the property to true to prevent bad actors from using internal port scanning in your network.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

