---
title: Exploring limit concurrent sessions
description: You can limit the number of concurrent interactive sessions for a user or role on an instance across all nodes.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Limit concurrent sessions, Authentication, Access Management]
---

# Exploring limit concurrent sessions

You can limit the number of concurrent interactive sessions for a user or role on an instance across all nodes.

Concurrent interactive sessions refer to the number of sessions a user can have active per ServiceNow instance. An active instance session occurs with every new login to a specific ServiceNow instance. By default, there are no limitations on the number of active instance sessions a user can have.

With the Jakarta release, you can limit the number of active concurrent sessions per user. When the user logs in after hitting the maximum number of sessions active, the oldest active session terminates and a new interactive session becomes active. If a user tries to access a closed session through a browser, the user is redirected to the login page.

**Note:** The **Limit concurrent sessions** plugin must be active to enable a maximum session limit. Limits are set through the glide.authenticate.max.concurrent.interactive.sessions property. A maximum limit value applies to any user or role that has the limit property active. A user or a role connected to the user must have the limit\_concurrent\_sessions value set to true for the limit on sessions to initiate. For the Jakarta release, this feature does not support sessions created through the native mobile app or non-interactive mechanisms.

A typical use case if a maximum concurrent session of 1 is set:

1.  The user accesses the initial ServiceNow instance through Chrome.
2.  After the user successfully logs in, ServiceNow creates session 1 \(S1\) for the user.
3.  The user decides to initiate another access to the ServiceNow instance through Firefox.
4.  After the user successfully logs in, ServiceNow creates session 2 \(S2\) for the user.
5.  Since the user has a maximum concurrent session limit of 1, the S1 session invalidates when S2 is created.
6.  When the user goes back through Chrome to access the S1 ServiceNow instance, the user is redirected to the login page as S1 is invalid.

Concurrent session limits work with all the ServiceNow authentication mechanisms: SAML, LDAP, and local database authentication. It also works with Multi-factor authentication and all interactive ServiceNow authentication mechanisms. The source of the session is viewable through the **sys\_user\_session** table, under the column **Type**. The values can be:

-   Web Browser
-   Mobile Browser
-   ServiceNow Mobile App
-   Non-interactive \(SOAP, WSDL, OAuth\)

