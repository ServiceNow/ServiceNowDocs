---
title: Client ID Metadata Document \(CIMD\) workflow
description: Configuring Client ID Metadata Document \(CIMD\) inbound support lets an instance accept an external OAuth client that's identified by a metadata document URL, without storing a client secret for that client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/cimd-inbound-integration-workflow.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 2
keywords: [CIMD, Client ID Metadata Document, OAuth inbound, public client, oauth\_entity\_cimd, metadata sync mode]
breadcrumb: [CIMD client integration, Inbound Integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Client ID Metadata Document \(CIMD\) workflow

Configuring Client ID Metadata Document \(CIMD\) inbound support lets an instance accept an external OAuth client that's identified by a metadata document URL, without storing a client secret for that client.

## Before you begin

Role required: `oauth_admin`

## About this task

CIMD gives you a faster, lower-friction way to bring an external OAuth client onto an instance. Instead of entering every client detail manually, you point the instance at the client's metadata URL, and the platform fetches the configuration.

You stay in control of which clients connect. An instance doesn't accept clients on its own — you register each CIMD client before it can connect. CIMD makes registration easier and, in Live mode, keeps the client's configuration current. It doesn't remove the registration step.

When you register a CIMD client, you select how the instance keeps the client's configuration up to date:

-   **Live \(Dynamic\)**

    For fully trusted clients. The ServiceNow AI Platform refreshes the client configuration dynamically from the Client ID metadata. The metadata is cached and re-fetched when the cache expires \(default 1 hour\), not on every use.

-   **Static \(Manual\)**

    For pre-approved clients. The ServiceNow AI Platform uses the initial configuration captured during onboarding. No automatic updates are made afterward.


## About this task

\[Omitted image "cimd-inbound-workflow.png"\] Alt text: Client ID Metadata Document \(CIMD\) workflow

## Procedure

1.  **Authorization**
2.  The client redirects the user to the instance's authorization endpoint, using the client's metadata document URL as the client ID and including a PKCE code challenge.

    **Note:** Proof Key for Code Exchange \(PKCE\) is required for CIMD clients.

3.  The instance identifies the client ID as a registered CIMD client and retrieves the client's configuration, either from cache or by fetching the metadata document from the client's URL.

4.  The instance validates the request against the metadata.

    The instance confirms that the redirect URI is an exact match of a redirect URI in the metadata, that the client uses a supported grant type, and that the client is registered as a public client.

5.  If user consent is required, the instance displays the consent screen, showing the client name from the metadata.

    Whether the consent screen appears depends on the consent configuration. An administrator can configure CIMD clients to bypass the consent screen, in which case the flow continues without prompting the user.

6.  **The user approves access**

    **Note:** This step is skipped when the consent screen is configured to be bypassed.

7.  The instance redirects the user back to the client with an authorization code.

8.  **Token exchange**
9.  The client exchanges the authorization code for an access token at the instance's token endpoint, sending the PKCE code verifier.

    Because a CIMD client is a public client, the token request does not include a client secret.

10. The instance verifies the PKCE code verifier, validates the authorization code, and issues an access token to the client.

11. **API access**
12. The client includes the access token in the API requests to the instance.

13. The instance validates the access token, and returns the appropriate API response.


## What to do next

For details on configuring a client, see [Configure a CIMD client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configure-cimd-client.md).

