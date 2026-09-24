---
title: Register an external authorization server for the ServiceNow MCP Server
description: Create an OIDC Provider Configuration to register an external authorization server, such as Microsoft Entra ID or Okta, as a trusted token issuer for the ServiceNow MCP Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/mcp-3p-auth-task.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [OIDC provider configuration, external authorization server, MCP Server, JWT]
breadcrumb: [External authorization servers for the ServiceNow MCP Server, Authentication, Access Management]
---

# Register an external authorization server for the ServiceNow MCP Server

Create an OIDC Provider Configuration to register an external authorization server, such as Microsoft Entra ID or Okta, as a trusted token issuer for the ServiceNow MCP Server.

## Before you begin

-   You have the details of the external authorization server: its issuer URI and its OIDC metadata URL.
-   You have the role required to manage OIDC Provider Configurations and OAuth Protected Resources.

Role required: oauth\_admin

## About this task

Registering an external authorization server involves creating an OIDC Provider Configuration that identifies the provider and defines how its tokens are validated. To advertise the protected resource to MCP clients, you also confirm an OAuth Protected Resource record for the resource the MCP Server exposes.

## Procedure

1.  Navigate to the **OIDC Provider Configurations** list.

2.  Select **New**.

3.  Complete the fields that identify the external authorization server:

    1.  In the **OIDC Provider** field, enter a name for the provider configuration.

    2.  In the **Issuer URI** field, enter the provider's issuer identifier.

    3.  In the **OIDC Metadata URL** field, enter the provider's metadata discovery endpoint.

4.  Set how tokens from the provider are validated and mapped:

    1.  To validate the JTI claim on incoming tokens, select **Enable JTI claim verification** and set the **JTI Claim** field.

    2.  In the **User Claim** and **User Field** fields, set the token claim used to identify the user and the ServiceNow user field it maps to.

    3.  Set the **OIDC Configuration Cache Life Span** to control how long the instance caches the provider's metadata.

5.  Select the **Active** check box, and then select **Submit**.

6.  Confirm that an **OAuth Protected Resource** record exists for the resource the MCP Server exposes.

    The OAuth Protected Resource record defines the resource that the Protected Resource Metadata endpoint advertises, including the resource identifier and the Glide APIs an authenticated client is allowed to call. See the reference topic for the field details.


## Result

The external authorization server is registered as a trusted token issuer. MCP clients can now obtain a token from the provider and use it to authenticate to the ServiceNow MCP Server. Tokens from issuers that are not registered and active are rejected.

