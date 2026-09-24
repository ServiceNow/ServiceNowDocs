---
title: OIDC Provider Configuration and OAuth Protected Resource fields
description: Reference for the fields on the OIDC Provider Configuration and OAuth Protected Resource records used to register an external authorization server for the ServiceNow MCP Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/mcp-3p-auth-reference.html
release: brazil
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [OIDC provider configuration, OAuth protected resource, MCP Server, reference]
breadcrumb: [External authorization servers for the ServiceNow MCP Server, Authentication, Access Management]
---

# OIDC Provider Configuration and OAuth Protected Resource fields

Reference for the fields on the OIDC Provider Configuration and OAuth Protected Resource records used to register an external authorization server for the ServiceNow MCP Server.

## OIDC Provider Configuration fields

|Field|Description|
|-----|-----------|
|OIDC Provider|The name of the external authorization server configuration.|
|Active|When selected, the configuration is in effect and the provider is a trusted token issuer.|
|Issuer URI|The issuer identifier of the external authorization server. The instance matches the issuer claim on an incoming token against this value.|
|OIDC Metadata URL|The provider's OIDC metadata discovery endpoint, used to retrieve the provider's signing keys and configuration.|
|Enable JTI claim verification|When selected, the instance verifies the JTI claim on incoming tokens.|
|JTI Claim|The name of the token claim that carries the JTI value.|
|OIDC Configuration Cache Life Span|How long the instance caches the provider's OIDC metadata.|
|SSO Only||
|User Claim|The token claim used to identify the user.|
|User Field|The ServiceNow user field that the User Claim value is matched against. In the demo, this was set to email.|

## OAuth Protected Resource fields

|Field|Description|
|-----|-----------|
|Resource Name|A display name for the protected resource.|
|Resource Identifier|The identifier of the protected resource, advertised in the Protected Resource Metadata.|
|Active|When selected, the resource is active.|
|Application|The application scope the resource belongs to.|
|Allowed Glide APIs|The Glide APIs an authenticated client is allowed to call for this resource.|
|Allow Glide as Authorization Server|When selected, the ServiceNow authorization server can also issue tokens for this resource, and any registered external authorization servers.|
|Allowed Services||
|Bearer Methods Supported|How the bearer token is presented on a request. In the demo, this was set to header.|
|Scopes Supported|The scopes advertised for the resource in the Protected Resource Metadata.|
|Domain|The domain the resource record belongs to.|

