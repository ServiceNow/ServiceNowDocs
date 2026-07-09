---
title: Configure a CIMD client
description: Register a Client ID Metadata Document \(CIMD\) client so that the instance accepts inbound OAuth requests from a client identified by a metadata document URL. You can fetch the client's configuration from its metadata URL or enter the details manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-cimd-client.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 4
keywords: [configure CIMD client, register CIMD client, Client ID Metadata Document, CIMD metadata URL, metadata sync mode, oauth\_entity\_cimd]
breadcrumb: [CIMD client integration, Inbound Integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Configure a CIMD client

Register a Client ID Metadata Document \(CIMD\) client so that the instance accepts inbound OAuth requests from a client identified by a metadata document URL. You can fetch the client's configuration from its metadata URL or enter the details manually.

## Before you begin

Role required: `oauth_admin`

To fetch the configuration automatically, you need the client's CIMD metadata document URL.

## About this task

You can register a CIMD client in two ways:

-   **Fetch the configuration from the metadata URL**

    The instance retrieves the client's metadata document and populates the client fields for you. Use this method when the client publishes a CIMD metadata document.

-   **Enter the configuration details manually**

    Provide the client fields yourself. Use this method when you want to enter or adjust the details by hand.


Each CIMD client also has a metadata sync mode that controls how the instance keeps the client's configuration current:

-   **Live \(Dynamic\)**

    For fully trusted clients. The ServiceNow AI Platform refreshes the client configuration dynamically from the Client ID metadata. The metadata is cached and re-fetched when the cache expires \(default 1 hour\), not on every use.

-   **Static \(Manual\)**

    For pre-approved clients. The ServiceNow AI Platform uses the initial configuration captured during onboarding. No automatic updates are made afterward.


## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **CIMD Clients**.

2.  Select **New**.

3.  On the **What kind of OAuth application?** page, select **Configure a Client ID Metadata Document \(CIMD\) client**.

    The **Add a CIMD OAuth Client** dialog opens.

    \[Omitted image "cimd-client-1.png"\] Alt text: Add a CIMD OAuth Client

4.  Provide the client configuration using one of the following methods:

    -   Fetch from the metadata URL \(recommended\): In **CIMD Metadata URL**, enter the client's metadata document URL — for example, `https://vscode.dev/oauth/client-metadata.json` and select **Fetch Metadata**. The instance retrieves the document and populates the **Client Name**, **Redirect URIs**, **Response Types**, **Client URI**, and **Logo URL** fields.
    -   Enter the details manually: Select **Enter the details instead**, and enter the client's **Name**, **Client ID** \(the CIMD metadata document URL\), and the remaining fields.
5.  Select the **Metadata Sync Mode**:

    -   Live: The instance fetches the latest configuration from the Client ID metadata each time the client is used. You don't maintain the **Client Name**, **Redirect URIs**, **Response Types**, **Client URI**, or **Logo URI** values manually.
    -   Static: The instance stores the configuration captured during onboarding and makes no automatic updates. Provide the **Client Name**, **Redirect URIs**, **Response Types**, **Client URI**, or **Logo URI** values, because the instance doesn't refresh them automatically.
    **Note:** The registration dialog uses spec-style labels for some of these fields — **Client ID \(CIMD URL\)**, **Client Name**, **Redirect URIs**, and **Logo URI** — while the saved record uses the labels in this table \(**Client ID**, **Name**, **Redirect URL**, and **Logo URL**\). These are the same fields.

    \[Omitted image "cimd-client-2.png"\] Alt text: Add a CIMD OAuth Client

6.  If the client uses localhost redirect URIs, select **Localhost redirection allowed**.

7.  Review and complete the remaining fields, using the following descriptions.

    **Note:**

    -   The **Mode** column in the following table indicates whether a field applies to both metadata sync modes or only to a specific mode.
    -   Fields marked **Static** are entered manually; in **Live** mode, the instance fetches those values from the CIMD endpoint during the authorization code flow.
<table><thead><tr><th>

Field

</th><th>

Required

</th><th>

Mode

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Yes

</td><td>

Both

</td><td>

Display name for the client.

</td></tr><tr><td>

**Client ID**

</td><td>

Yes

</td><td>

Both

</td><td>

The HTTPS CIMD metadata URL, set automatically from the URL entered at registration. This URL is the client identifier used in the OAuth flow.

</td></tr><tr><td>

**Client URI**

</td><td>

No

</td><td>

Static

</td><td>

Client home page.

</td></tr><tr><td>

**Redirect URL**

</td><td>

Yes

</td><td>

Static

</td><td>

Where the authorization code is returned. In Live mode, it's fetched from the CIMD endpoint during the authorization code flow. Multiple redirect URLs are supported.

</td></tr><tr><td>

**Logo URL**

</td><td>

No

</td><td>

Both

</td><td>

Logo shown on the consent screen.

</td></tr><tr><td>

**Metadata Sync Mode**

</td><td>

No

</td><td>

Both

</td><td>

Live \(default\) fetches from the CIMD endpoint. Static pins the manually entered values.

</td></tr><tr><td>

**Localhost redirection allowed**

</td><td>

No

</td><td>

Both

</td><td>

Turn on to allow localhost redirection when the redirect URL is localhost or a loopback address.

</td></tr><tr><td>

**Active**

</td><td>

—

</td><td>

Both

</td><td>

On by default.

</td></tr><tr><td>

**Refresh Token Lifespan**

</td><td>

Yes

</td><td>

Both

</td><td>

Seconds; default `8,640,000`.

</td></tr><tr><td>

**Access Token Lifespan**

</td><td>

Yes

</td><td>

Both

</td><td>

Seconds; default `1,800`.

</td></tr><tr><td>

**Response Types**

</td><td>

No

</td><td>

Static

</td><td>

Supports code only; authorization code with PKCE only.

</td></tr><tr><td>

**Public Client**

</td><td>

—

</td><td>

Both

</td><td>

Always on for CIMD clients \(PKCE\); read-only.

</td></tr><tr><td>

**Token Format**

</td><td>

Yes

</td><td>

Both

</td><td>

-   Opaque \(default\)
-   JWT


</td></tr><tr><td>

**Scope Restriction**

</td><td>

Yes

</td><td>

Both

</td><td>

-   Securely scoped \(default\)
-   Broadly scoped
 **Note:** For ServiceNow MCP server use cases, use Broadly Scoped.

</td></tr><tr><td>

**Cache lifespan**

</td><td>

No

</td><td>

Both

</td><td>

Metadata cache in seconds; default `3,600`.

</td></tr><tr><td>

**Auth Scopes** \(related list\)

</td><td>

—

</td><td>

Both

</td><td>

Scopes granted to the client. To know more about Auth Scopes, see [REST API Auth Scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/rest-api-auth-scope.md).

</td></tr><tr><td colspan="4">

**Generic fields**

</td></tr><tr><td>

**Login URL**

</td><td>

No

</td><td>

Both

</td><td>

Optional login URL.

</td></tr><tr><td>

**Application**

</td><td>

—

</td><td>

Both

</td><td>

Global \(read-only\).

</td></tr><tr><td>

**Accessible from**

</td><td>

—

</td><td>

Both

</td><td>

All application scopes \(default\).

</td></tr><tr><td>

**Comments**

</td><td>

No

</td><td>

Both

</td><td>

Free text.

</td></tr></tbody>
</table>    \[Omitted image "cimd-client-3.png"\] Alt text: CIMD Registration

8.  Register the client:

    -   If you fetched the metadata in the dialog, select **Create**.
    -   If you entered the details on the form, select **Submit** or **Update** to complete the registration.

## Result

The CIMD client is registered and appears in the **CIMD Registered Clients** list. The instance accepts inbound OAuth requests from the client, validating the request against the client's metadata each time the client initiates a flow.

