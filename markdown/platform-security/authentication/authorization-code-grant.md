---
title: Authorization code grant
description: The OAuth authorization code grant is a secure and widely used flow for web, mobile, or desktop apps that access user data with user consent. It supports both private clients \(using a client secret\), and public clients \(using PKCE\).
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Authorization code grant

The OAuth authorization code grant is a secure and widely used flow for web, mobile, or desktop apps that access user data with user consent. It supports both private clients \(using a client secret\), and public clients \(using PKCE\).

In this flow, ServiceNow functions as both the authorization server \(handling user authentication and token issuance\) and the resource server \(hosting the APIs\). If SSO is enabled, ServiceNow redirects the user to the configured Identity Provider \(IdP\) for authentication. After the IdP successfully authenticates the user, control returns to ServiceNow, which then issues the authorization code. This process ensures that even with external authentication, ServiceNow remains the authority for issuing tokens and managing API access.

-   **Ideal for:**

    Applications that need to access user data on behalf of user with the user’s consent.

-   **How it works:**

    The user initiates the login process from the client application, which redirects them to a ServiceNow login page. After the user logs in and grants consent, the client application receives an authorization code, which it exchanges with the ServiceNow instance for an access token. This is the most secure and widely used flow for user-facing integrations. It supports both confidential clients \(with a client secret\) and public clients \(using PKCE\).


**Note:** If you want to use your own identity provider \(such as Azure AD or Okta\) as the authorization server, consider using the  flow.

**Related topics**  


[Authorization code grant workflow](authorization-workflow.md)

[Configure an OAuth authorization code grant](../../machine-identity/task/configure-an-oauth-authorization-code-grant.md)

