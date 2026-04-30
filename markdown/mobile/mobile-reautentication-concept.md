---
title: Configure mobile re-authentication system properties
description: Set mobile re-authentication system properties so users must re-authenticate their login credentials when performing specific actions.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile system property configurations, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile re-authentication system properties

Set mobile re-authentication system properties so users must re-authenticate their login credentials when performing specific actions.

To activate the re-authentication option, select `Re-authentication` in the **Preconditions** field within the Action functions table. See, [Configure an action function](../task/sg-studio-config-action-function.md).

-   **[Configure mobile re-authentication login method](mobile-reauthentication-login-method.md)**  
Define the re-authentication method to be either single sign-on \(SSO\) or local login, depending on your security requirements.
-   **[Configure mobile re-authentication SSO login](../task/mobile-reauthentication-login-sso.md)**  
Define which identity provider to use for the SSO login. If this property is not defined, the system reuses the default identity provider used for a regular login.
-   **[Configure mobile re-authentication logout option](../task/mobile-reauthentication-logout.md)**  
Configure this parameter to force your users to log out each time before they re-authenticate.
-   **[Configure mobile re-authentication for single or multiple use](../task/mobile-reauthentication-usage-token.md)**  
Define whether each mobile action requires re-authentication. Alternatively, define whether the user can perform multiple actions without the need to re-authenticate each time.
-   **[Configure mobile re-authentication login timespan](../task/mobile-reauthentication-token-lifespan.md)**  
Define a time period in seconds that a user is not required to re-authenticate themselves. This parameter only applies when a user has permission to re-authenticate multiple times.

**Parent Topic:**[Mobile system property configurations](additional-mobile-configuration.md)

