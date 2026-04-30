---
title: Multi-Provider SSO \(SAML\) IdP authentication flow
description: Describes the different entities that can authenticate a user through the SAML multi-SSO.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Multi-Provider SSO \(SAML\) IdP authentication flow

Describes the different entities that can authenticate a user through the SAML multi-SSO.

You can follow the authentication flow to understand when an entity authenticates a user using Multi-SSO.

![](../images/Idp_auth_flow.png)

-   **Local DB**

    If Multi-SSO is not enabled, authentication directs to a local DB.

-   **SAML SSO Cookie IdP**

    If a SAML SSO cookie exists, the IdP which is specified with this cookie authenticates the user.

-   **Auto-redirect IdP**

    If the auto-redirect IdP is enabled, this IdP authenticates the user.

-   **Federated IdP**

    If the user browser is redirected to the external authorization \(login\_locate\_sso.do\) login screen, and the user exists in the user table with the IdP set in the **SSO Source** field as federation: xxx, then the federated IdP authenticates the user.

-   **Associated IdP**

    If the user browser is redirected to the external authorization \(login\_locate\_sso.do\) login screen, and the user exists in the user table with the IdP set in the **SSO Source** field as sso: xxx, then the associated IdP authenticates the user.

-   **Auto-provisioning IdP**

    If the user browser is redirected to the external authorization \(login\_locate\_sso.do\) login screen, and the user does not exist in the user table, but auto-provisioning is enabled, then the auto-provisioning IdP authenticates the user.

    **Note:** If there is more than one auto-provisioning IdP enabled, the user can choose the auto-provisioning IdP they can use.

-   **Default IdP**

    If the user browser is redirected to the external authorization \(login\_locate\_sso.do\) login screen, and the user either:

    -   Does not exist in the user table, auto-provisioning is not enabled, and there is an active default IdP
    -   Exists in the user table, an IdP is not specified on the SSO source user or company record, and there is an active default IdP
    then the default IdP authenticates the user.


