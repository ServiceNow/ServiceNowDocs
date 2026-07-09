---
title: Client ID Metadata Document \(CIMD\) client integration
description: CIMD lets the ServiceNow AI Platform accept an external OAuth client that identifies itself with an HTTPS metadata-document URL instead of a pre-issued client ID and secret.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/cimd-inbound.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-06-19"
reading_time_minutes: 4
keywords: [CIMD, Client ID Metadata Document, OAuth inbound, oauth\_entity\_cimd, public client, client registration, authentication]
breadcrumb: [Inbound Integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Client ID Metadata Document \(CIMD\) client integration

CIMD lets the ServiceNow AI Platform accept an external OAuth client that identifies itself with an HTTPS metadata-document URL instead of a pre-issued client ID and secret.

CIMD is a JSON file an OAuth client hosts at an HTTPS URL; that URL serves as the client's `client_id`, and when the client initiates an OAuth flow, the ServiceNow AI Platform fetches the metadata document from the URL and uses it to complete the flow. This removes the pre-registeration of client secret for every client.

CIMD gives you a faster, lower-friction way to bring an external OAuth client onto an instance. Instead of entering every client detail manually, you point the instance at the client's metadata URL, and the ServiceNow AI Platform fetches the configuration.

You stay in control of which clients connect. An instance doesn't accept clients on its own — you register each CIMD client before it can connect. CIMD makes registration easier and, in Live mode, keeps the client's configuration current. It doesn't remove the registration step.

**Note:**

-   CIMD clients are public clients. Because there is no way to establish a shared client secret with a client identified only by a metadata URL, the metadata document can't use client secret authentication methods.
-   CIMD replaces Dynamic Client Registration \(DCR\) as the supported approach for clients that connect without prior registration. Instead of each client registering through DCR and creating a registration record that the instance must store and maintain, a CIMD client is identified by its metadata document URL, and the instance fetches the registration details from that URL when they are needed.

## How CIMD works

At the protocol level the flow is:

1.  The client hosts its metadata as a JSON document at a stable HTTPS URL on a domain it controls.
2.  The client sends that URL as the client\_id in the authorization request.
3.  If the instance supports CIMD, it fetches the document over HTTPS, validates the JSON and required fields, and confirms that the client\_id inside the document exactly matches the URL it was fetched from.
4.  The instance applies its policy—on ServiceNow AI Platform, this means the client must already be registered.
5.  The standard authorization code flow continues, including consent.
6.  Metadata is fetched when a client starts a new authorization flow, not on token refreshes or ordinary API calls, so the effect on day-to-day performance is minimal.

## Availability

CIMD is available from **Zurich Patch 7** onward and from **Australia Patch 1** onward.

## CIMD metadata document

The metadata values follow the OAuth client metadata vocabulary \(RFC 7591\). ServiceNow AI Platform supports public clients only, so the client uses PKCE rather than a client secret.

|Field|Required|Purpose|
|-----|--------|-------|
|client\_id|Required|Must equal the HTTPS URL where the document is hosted, compared as a simple string.|
|redirect\_uris|Required|Allowed redirect targets; the instance exact-matches the request against these.|
|client\_name|Recommended|Human-readable name shown on the consent screen.|
|client\_uri|Recommended|The client's home page; supports trust checks.|
|logo\_uri|Optional|Logo shown on the consent screen.|

## URL and hosting requirements

The metadata URL must use HTTPS and include a path, and it must not contain dot or double-dot path segments. A short, stable URL is recommended because it may appear to people on authorization screens. The endpoint must return valid JSON with a JSON content type; if the document is malformed, the instance stops the request and does not cache the error.

## Metadata sync modes

Each CIMD client is configured with a metadata sync mode that determines how the obtains and refreshes the client's configuration:

-   **Live \(Dynamic\)**

    For fully trusted clients. The ServiceNow AI Platform refreshes the client configuration dynamically from the Client ID metadata. The metadata is cached and re-fetched when the cache expires \(default 1 hour\), not on every use.

-   **Static \(Manual\)**

    For pre-approved clients. The ServiceNow AI Platform uses the initial configuration captured during onboarding. No automatic updates are made afterward.


## Supported use cases

-   **ServiceNow MCP Server—MCP clients**: An MCP client can identify with a CIMD URL rather than a manually created OAuth inbound integration. There is no dedicated onboarding UI for MCP clients yet; they use the same CIMD registration flow as any other client.
-   **Regular OAuth clients**: CIMD is a general OAuth client-identification mechanism on the instance, not limited to MCP.

## Public clients, PKCE, and token format

Characteristics of CIMD clients CIMD clients:

-   Public clients and use PKCE; the Public Client setting is fixed
-   The supported response type is code only
-   The only supported flow is authorization code with PKCE
-   Token Format defaults to Opaque, with JWT also available. Scope Restriction defaults to Securely scoped.

## Caching and performance

The instance caches the metadata it fetches and does not cache errors or invalid documents. The default cache lifespan is **3,600 seconds \(one hour\)** and is configurable per client through the Cache lifespan field. Because metadata is fetched only at the start of a new authorization flow, the performance impact is small.

