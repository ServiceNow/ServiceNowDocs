---
title: Securing your ServiceNow mobile instance with Zero Trust Access
description: Limit end-user access to your ServiceNow instance by opting in to Zero Trust Access. This adjusts user roles and permissions according to security policies defined by the admin based on factors such as IP address, location, and identity provider attributes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/zero-trust-access-for-mobile.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Securing your ServiceNow mobile instance with Zero Trust Access

Limit end-user access to your ServiceNow® instance by opting in to Zero Trust Access. This adjusts user roles and permissions according to security policies defined by the admin based on factors such as IP address, location, and identity provider attributes.

Session states can either be relegated with limited user access or restored with full user access. If a user’s mobile session when logging in to their mobile app meets the security policy conditions set by Zero Trust Access, a banner appears that explains that the user’s access may be limited. This can help protect against unauthorized access and data breaches, even when high-privileged users access applications from untrusted devices or locations.

For more information, see [Zero Trust Access \(ZTA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/servicenow-ai-platform-security/session-access.md).

\[Omitted image "mobile-zero-trust-access.png"\] Alt text: Banner notifying the user that their access may be limited because they are not on a trusted network.

-   **[Configure Zero Trust Access for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/configure-zero-trust-access-mobile.md)**  
Configure Zero Trust Access \(ZTA\) on mobile to reduce end-user access based on factors such as IP address, location, and identity provider attributes.

**Parent Topic:**[Mobile authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-authentication.md)

