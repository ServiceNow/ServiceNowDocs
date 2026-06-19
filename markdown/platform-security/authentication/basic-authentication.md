---
title: Basic authentication
description: Legacy API authentication method using username and password, with restricted usage and varying behaviour in zBoot and upgraded instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/basic-authentication.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API Authentication, Authentication, Access Management]
---

# Basic authentication

Legacy API authentication method using username and password, with restricted usage and varying behaviour in zBoot and upgraded instances.

Basic authentication is a legacy method for authenticating API requests using a username and password combination. While it remains available for compatibility in certain scenarios, its use is strongly discouraged over token-based authentication methods.

Basic authentication should only be used in limited scenarios where alternative methods aren't viable.

## Behaviour across instance scenarios

The behaviour of basic authentication varies depending on how an instance is provisioned or upgraded.

-   **zBoot instances \(newly provisioned instances\)**

    In zBoot scenarios, basic authentication is restricted by default to improve security.

    -   Basic authentication may be blocked unless specific conditions are met
    -   Access may be limited to users with required roles or permissions
    -   Enforcement is stricter compared to upgraded instances
    These restrictions minimises exposure to insecure authentication methods and encourage adoption of modern alternatives.

-   **Upgraded instances**

    In upgraded instances, basic authentication may continue to function under certain conditions to support backward compatibility.

    -   Existing integrations using basic authentication may continue to work
    -   Restrictions may be applied gradually depending on patch or upgrade level
    -   Behaviour may differ based on system configuration and applied changes
    This approach allows existing users to transition to more secure authentication mechanisms without immediate disruption.


## Restrictions and limitations

Basic authentication is subject to several restrictions that vary based on system context and applied updates.

<table id="table_mdv_zrl_njc"><thead><tr><th>

Restrictions

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Access restrictions

</td><td>

-   Basic authentication may be inactive by default in some scenarios.
-   Access may only be permitted for specific users or roles.
-   Certain environments may enforce stricter controls.

</td></tr><tr><td>

Behavioural restrictions

</td><td>

-   Behaviour differs between:
    -   zBoot instances \(stricter enforcement\)
    -   Upgraded instances \(transitional behaviour\)
-   Allowed usage may be time-bound or limited in scope depending on configuration.

</td></tr></tbody>
</table>