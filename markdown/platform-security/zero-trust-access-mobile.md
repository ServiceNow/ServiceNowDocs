---
title: Zero Trust Access for Mobile
description: Zero Trust Access \(ZTA\) is a security model that assumes that no user or device is trusted by default.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zero Trust Access, Access Management]
---

# Zero Trust Access for Mobile

Zero Trust Access \(ZTA\) is a security model that assumes that no user or device is trusted by default.

You can use the Zero Trust Access - Session Access policy within the Adaptive Authentication policy to reduce the roles or privileges of the particular session in mobile for users.

To enable Zero Trust Access on mobile, you must perform the following tasks:

-   Session Access configurations can only be performed with `security_admin` role. You must elevate your role to `security_admin`.
-   Activate the **Zero Trust - Policy Based Session Access** `com.snc.zero_trust_session_access` policy.
-   Enable the **glide.authenticate.session\_access.mobile.enabled** from the system properties table.![Zero Trust Access Mobile Enabled](../images/enable-zero-trust-access-mobile.png)
-   Configure the **glide.authenticate.session\_access.mobile.refresh\_token\_interval** field to control session access on mobile based on the refresh token.![Refresh token configuration](../images/idp-setup-zero-trust-access-mobile.png)

    **Note:** You must configure the refresh token seconds when using an IDP for Mobile App logins. By default, users are logged out from the mobile apps after 1800 seconds \(30 minutes\).

-   Enable Zero Trust Access is enabled under **Application Registries** for the mobile client application \(OAuth client\). In this case, **ServiceNow Agent** \(Now Agent\) and **ServiceNow Request** \(Now Mobile\).![Application Regisrty](../images/application-registry-trust-access-mobile.png)
-   Configure Session Access role to either reduce or remove roles for the users logging based on the policy inputs and conditions. To learn more about the configuration, see [Configuring Session Access role](../task/configure-session-access-role.md).

The configuration evaluates the login to reduce or remove the roles of the users who access your ServiceNow® instance based on the policy filters and conditions. For more information, see [Configure Zero Trust Access for mobile](https://www.servicenow.com/docs/access?context=configure-zero-trust-access-mobile&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

