---
title: Session management
description: This category looks at the security of the application state for a user. Sessions should be unique to each individual, unable to be guessed or shared, and invalidated after periods of inactivity or when not required. This includes factors such as cookie attributes for cookie-based sessions, session token generation, and storage and requirements for federated re-authentication.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Hardening settings, Platform Security]
---

# Session management

This category looks at the security of the application state for a user. Sessions should be unique to each individual, unable to be guessed or shared, and invalidated after periods of inactivity or when not required. This includes factors such as cookie attributes for cookie-based sessions, session token generation, and storage and requirements for federated re-authentication.

-   **[Apply continuous authentication policies to mobile sessions](sc-apply-continuous-authentication-policies-to-mobile-sessions.md)**  
Reduce the risk of session hijacking by applying continuous authentication policies to mobile sessions.
-   **[Minimize absolute session timeout duration \[Updated in Security Center 1.3\]](sc-absolute-session-timeout.md)**  
Use the **glide.ui.user\_cookie.max\_life\_span\_in\_days** property to set a maximum life span for user cookies created when users log in with the **Remember Me** checkbox selected. When the cookie expires, users who have selected the **Remember Me** checkbox are forced to reauthenticate into the instance.
-   **[Define active session timeout exception roles \[New in Security Center 1.3\]](sc-define-active-session-timeout-exception-roles.md)**  
Use a system property to exempt roles from active session timeout limits.
-   **[Enable UserCookie version 3.1 \[Updated in Security Center 2.0\]](sc-enable-usercookie-version-3-1.md)**  
Manage the version of UserCookie that is enabled on your instance to secure the storage of the secret key in the source code.
-   **[Enforce password reset on api requests \[Updated in Security Center 1.5\]](sc-enforce-password-reset-on-api-requests.md)**  
Manage how the password reset functionality operates on your instance.
-   **[Enable HTTP Only Cookie Flag \[Updated in Security Center 1.3\]](sc-http-only-cookie-flag.md)**  
Use the **glide.cookies.http\_only** property to enable the HTTPOnly attribute for sensitive cookies.
-   **[Invalidate Session After OAuth Token Expiration \[New in Security Center 2.0\]](sc-invalidate-session-after-oauth-token-expiration.md)**  
Configure the **glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled** property to the secure value to prevent users from continuing to use a session via cookies after the OAuth token used to create the session expires.
-   **[Minimize concurrent interactive session quantity \[Updated in Security Center 1.3\]](sc-glide-authenticate-max-concurrent-interactive-sessions.md)**  
Use this property with the Limit Concurrent Sessions plugin to control the number of active sessions that can be opened by a user.
-   **[Limit concurrent sessions across all nodes \[Updated in Security Center 1.3\]](sc-limit-concurrent-sessions-across-all-nodes.md)**  
Use the **glide.authenticate.limit.concurrent.sessions.across.all.nodes** property with the Limit Concurrent Sessions plugin to manage the number of sessions tracked across all nodes.
-   **[Limit concurrent sessions plugin](sc-limit-concurrent-sessions-plugin.md)**  
Configure the com.glide.limit.concurrent.sessions plugin to reduce the chance of session hijacking on your instance.
-   **[Limit guest's active session life span \[New in Security Center 1.3\]](sc-limit-guests-active-session-life-span.md)**  
Use the **glide.guest.active.session.life\_span** property to control the duration of an active guest’s HTTP sessions.
-   **[Limit concurrent interactive sessions \[Updated in Security Center 1.3\]](sc-glide-authenticate-limit-concurrent-interactive-sessions.md)**  
Manage the number of interactive sessions on your instance.
-   **[Limit integrations' active session life span \[New in Security Center 1.3\]](sc-limit-integrations-active-session-life-span.md)**  
The **glide.integrations.active.session.life\_span** property enforces max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions.
-   **[Limit policy based session access mobile refresh token interval \[New in Security Center 1.5\]](sc-limit-policy-based-session-access-mobile-refresh.md)**  
Use the **glide.authenticate.session\_access.mobile.refresh\_token\_interval** property to govern the length of time that must elapse before a mobile device user will be forced to re-authenticate.
-   **[Limit UI active session life span \[New in Security Center 1.3\]](sc-limit-ui-active-session-life-span.md)**  
The **glide.ui.active.session.life\_span** property enforces max lifespan on active authenticated HTTP sessions irrespective of inactive timeout.
-   **[Limit session length for high assurance sessions](sc-limit-session-length-for-high-assurance-sessions.md)**  
Reduce the risk of account takeover in high assurance sessions by limiting session length
-   **[Proactively invalidate inactive sessions \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](sc-proactively-invalidate-inactive-sessions.md)**  
The **glide.active.session.timeout.invalidate.session** property controls if a timeout session is proactively invalidated before the Tomcat server.
-   **[Rotate HTTP session identifiers](sc-rotate-http-session-identifiers.md)**  
Use the **glide.ui.rotate\_sessions** property to enable rotation of the HTTP session identifiers to reduce security vulnerabilities.
-   **[Minimize concurrent interactive session quantity \[Updated in Security Center 1.3\]](sc-minimize-concurrent-interactive-session-quantity.md)**  
Use this property with the Limit Concurrent Sessions plugin to control the number of active sessions that can be opened by a user.
-   **[Minimize session activity timeout duration \[Updated in Security Center 1.3\]](sc-session-activity-timeout.md)**  
Use the **glide.ui.session\_timeout** property to designate, in minutes, activity timeout value.
-   **[Minimize session window timeout duration \[Updated in Security Center 1.3\]](sc-session-window-timeout.md)**  
Use the **glide.ui.user\_cookie.life\_span\_in\_days** property to set the expiration time period for the Remember Me cookie. The default value is 15 days and the maximum cap is at 30 days.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

