---
title: JSON Web token bearer grant
description: Configuring an OAuth JSON Web Token \(JWT\) bearer grant secures token-based authentication without user interaction. Use this flow when a client application needs secure, unattended access to ServiceNow resources, either as itself or on behalf of a user.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# JSON Web token bearer grant

Configuring an OAuth JSON Web Token \(JWT\) bearer grant secures token-based authentication without user interaction. Use this flow when a client application needs secure, unattended access to ServiceNow resources, either as itself or on behalf of a user.

The client application generates a signed JWT that includes identity-related claims, such as the user or system it represents. It sends it to the ServiceNow instance to request an access token.

-   **Ideal for:**

    Client applications that need secure access to ServiceNow resources—either on behalf of a user or as themselves—without requiring user interaction or storing a shared secret.

-   **How it works:**

    The client application creates a signed JWT \(JSON Web Token\) that includes identity-related claims—such as the user or system it represents—and presents it to the ServiceNow instance to request an access token.


## JWT Structure

The JWT must be signed using the client’s private key. It must include the following standard claims:

-   iss – Issuer \(client ID\)
-   sub – Subject \(user or system identity\)
-   aud – Audience \(ServiceNow token endpoint\)
-   exp – Expiration time
-   iat – Issued at

**Note:** ServiceNow uses the public key \(uploaded in the OAuth JWT profile\) to validate the signature and maps the sub claim to a user record.

**Related topics**  


[JSON Web token grant workflow](using-json-web-token-grant.md)

[Configure an OAuth JSON web token bearer grant](configure-an-oauth-jwt-bearer-grant.md)

