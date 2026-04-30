---
title: Resource owner password credential grant
description: Configuring an OAuth Resource Owner Password Credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Resource owner password credential grant

Configuring an OAuth Resource Owner Password Credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token.

## Security Considerations

The ROPC flow exposes user credentials directly to the client application, making it inherently less secure than modern alternatives. It should only be used in scenarios where the client is fully trusted, tightly controlled, and securely managed.

Avoid using this grant in modern applications unless absolutely necessary. For secure user-based access, it is strongly recommended to use the Authorization Code Flow with PKCE, which keeps credentials out of the client and leverages secure redirection and token handling practices.

**Related topics**  


[Resource owner password credential grant workflow](resource-owner-password-credential-workflow.md)

[Configure an OAuth resource owner password credential grant](configure-an-oauth-resource-owner-password-credential-grant.md)

