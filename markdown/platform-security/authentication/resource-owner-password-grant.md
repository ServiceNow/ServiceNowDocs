---
title: Resource owner password credential grant
description: Configuring an OAuth Resource Owner Password Credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Resource owner password credential grant

Configuring an OAuth Resource Owner Password Credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token.

-   **Ideal for:**

    Highly trusted internal client applications in controlled environments where the app collects the user’s credentials directly.

-   **How it works:**

    The client application collects the user’s username and password and sends them directly to the ServiceNow instance to obtain an access token. This flow bypasses redirection and consent screens but exposes user credentials to the client application, so it should only be used in legacy or tightly controlled environments where more secure alternatives are not feasible.


## Security Considerations

The ROPC flow exposes user credentials directly to the client application, making it inherently less secure than modern alternatives. It should only be used in scenarios where the client is fully trusted, tightly controlled, and securely managed.

Avoid using this grant in modern applications unless absolutely necessary. For secure user-based access, it is strongly recommended to use the Authorization Code Flow with PKCE, which keeps credentials out of the client and leverages secure redirection and token handling practices.

**Related topics**  


[Resource owner password credential grant workflow](resource-owner-password-credential-workflow.md)

[Configure an OAuth resource owner password credential grant](configure-an-oauth-resource-owner-password-credential-grant.md)

