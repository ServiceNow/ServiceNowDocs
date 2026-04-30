---
title: Authentication Metrics
description: Analyze authentication metrics to see information related to authentication, such as infrequently used IP addresses, failed logins, and types of authentication schemes used by your users.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Monitor instance metrics, Instance Security Center, Platform Security]
---

# Authentication Metrics

Analyze authentication metrics to see information related to authentication, such as infrequently used IP addresses, failed logins, and types of authentication schemes used by your users.

Use the **Authentication Metrics** page to view reports relating to your authentication configuration. The following reports are displayed in this tab.

**Note:** The authentication metrics page requires the **REST API Access Policy plugin** \(com.glide.rest.policy\) plugin. For more details about this feature, see [REST API access policies](../../../integrate/authentication/concept/inbound-authentication-profile.md).

-   **APIs without authentication policies**

    Displays a real-time count of all API’s without an access policy

-   **Hardening: Account recovery flow**
-   **Hardening: Role-based MFA feature related setting**
-   **Web service access only accounts**

    Shows the count of all user records with web service access option enabled in **User** \[sys\_user\] table.

-   **X509 certificates expiring in 30 days**

    Displays a count of all X.509 certificates from **X.509 Certificates** \[sys\_certificate\] table which are due expire in 30 days.


**Parent Topic:**[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)

