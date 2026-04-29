---
title: Client credentials grant
description: Use the OAuth client credentials grant type for back-end services or automated integrations that access ServiceNow APIs without user interaction. The client application authenticates directly using its client ID and secret, and receives an access token that represents the application itself, and not the user.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Client credentials grant

Use the OAuth client credentials grant type for back-end services or automated integrations that access ServiceNow® APIs without user interaction. The client application authenticates directly using its client ID and secret, and receives an access token that represents the application itself, and not the user.

-   **Ideal for:**

    Client applications such as back-end services or automated system integrations that need to access ServiceNow APIs without user involvement.

-   **How it works:**

    The client application authenticates directly with the ServiceNow instance using its own credentials \(client ID and secret\). Once authenticated, it receives an access token to access ServiceNow APIs. Because no user is involved, the access token represents the client application itself, not a user's identity.


**Related topics**  


[Client credentials grant workflow](client-credentials-grant-workflow.md)

[Configure an OAuth Client credential grant](../../machine-identity/task/configure-an-oauth-client-credential-grant.md)

