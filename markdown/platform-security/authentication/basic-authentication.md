---
title: Basic authentication
description: Legacy API authentication method using username and password, with restricted usage and varying behavior in zBoot and upgraded instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/basic-authentication.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [API authentication, Authentication, Access Management]
---

# Basic authentication

Legacy API authentication method using username and password, with restricted usage and varying behavior in zBoot and upgraded instances.

**Important:** Basic authentication is being prepared for future deprecation. Starting with the Brazil release, migrate your integrations to OAuth 2.0, mutual TLS \(mTLS\), or federated token-based authentication. Basic authentication remains supported until a future release, subject to the restrictions described in this topic. For guidance on identifying and migrating these integrations, see the [KB3220405](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220405) article.

Basic authentication is a legacy method for authenticating API requests using a username and password combination. While it remains available for compatibility in certain scenarios, its use is strongly discouraged over token-based authentication methods.

Basic authentication should only be used in limited scenarios where alternative methods aren't viable. To learn more about the basic authentication restrictions, review this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3025707).

## Behavior across instance scenarios

The behavior of basic authentication varies depending on how an instance is provisioned or upgraded.

-   **zBoot instances \(newly provisioned instances\)**

    In zBoot scenarios, basic authentication is restricted by default to improve security.

    -   Basic authentication may be blocked unless specific conditions are met
    -   Access may be limited to users with required roles or permissions
    -   Enforcement is stricter compared to upgraded instances
    These restrictions minimizes exposure to insecure authentication methods and encourage adoption of alternative authentication methods.

-   **Upgraded instances**

    In upgraded instances, basic authentication may continue to function under certain conditions to support backward compatibility.

    -   Existing integrations using basic authentication may continue to work
    -   Restrictions may be applied gradually depending on patch or upgrade level
    -   Behavior may differ based on system configuration and applied changes
    This approach enables existing users to transition to more secure authentication mechanisms without immediate disruption.


