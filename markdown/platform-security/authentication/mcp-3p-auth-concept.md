---
title: External authorization servers for the ServiceNow MCP Server
description: Register an external authorization server, such as Microsoft Entra ID or Okta, as a trusted token issuer for the ServiceNow MCP Server, so that MCP clients can authenticate using tokens issued by your enterprise identity provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/mcp-3p-auth-concept.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [MCP Server, Model Context Protocol, external authorization server, OIDC provider, JWT, Protected Resource Metadata, Entra ID, Okta]
breadcrumb: [Authentication, Access Management]
---

# External authorization servers for the ServiceNow MCP Server

Register an external authorization server, such as Microsoft Entra ID or Okta, as a trusted token issuer for the ServiceNow MCP Server, so that MCP clients can authenticate using tokens issued by your enterprise identity provider.

By default, an MCP client authenticates to the ServiceNow MCP Server using the ServiceNow authorization server. If your organization centralizes identity through an external provider — for example, Microsoft Entra ID or Okta — you can register that provider as a trusted external authorization server. MCP clients can then obtain a token from your provider and use it to call the ServiceNow MCP Server, without depending on the ServiceNow authorization server to issue the token.

Configuring this involves two record types:

-   **OIDC Provider Configuration**

    Registers an external authorization server as a trusted token issuer. The configuration identifies the provider's issuer URI and metadata endpoint, and defines how the ServiceNow MCP Server validates tokens the provider issues.

-   **OAuth Protected Resource**

    Defines a resource that the ServiceNow MCP Server protects and advertises through its Protected Resource Metadata endpoint. The resource record identifies the resource and the Glide APIs an authenticated client is allowed to call.


## How authentication works

When an MCP client calls the ServiceNow MCP Server with an external authorization server configured, the following sequence occurs:

1.  The MCP client calls the MCP Server without a token. The MCP Server returns HTTP 401 with a `WWW-Authenticate` header that includes the `resource_metadata` URL.
2.  The MCP client requests the Protected Resource Metadata from the `.well-known/oauth-protected-resource` endpoint. The response identifies the resource, the authorization servers that can issue tokens for it, and the supported scopes.
3.  The MCP client obtains a token from the external authorization server using the OAuth 2.1 authorization code flow with PKCE.
4.  The MCP client calls the MCP Server again, presenting the token as a bearer token.
5.  The ServiceNow MCP Server validates the token locally: it confirms the issuer is a trusted issuer, verifies the token signature, confirms the audience matches, and confirms the token has not expired. If validation succeeds, the MCP Server processes the request.

## Security considerations

-   The ServiceNow MCP Server accepts tokens only from authorization servers you register as trusted. A token from an unregistered issuer is rejected.
-   Register only the external authorization servers your organization uses, and keep the list current.
-   Fetching provider metadata and signing keys occurs over HTTPS.

