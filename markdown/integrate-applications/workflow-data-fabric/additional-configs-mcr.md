---
title: Additional connector configurations
description: Some connectors may require additional configurations while registering client manually. These connectors and their required configurations are listed here.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/additional-configs-mcr.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Additional connector configurations

Some connectors may require additional configurations while registering client manually. These connectors and their required configurations are listed here.

## Zoom connector

User must create one app in Zoom account for each MCP server. For example, two separate apps must be created in Zoom account for Zoom Revenue Accelerator and Zoom Whiteboard. One Zoom app cannot be used for more than one MCP server.

## Figma connector

Ensure that you whitelist your account and then obtain the values of **Client ID** and **Client secret**. For the list of whitelisted MCP clients, see [Figma MCP Catalog](https://www.figma.com/mcp-catalog/).

## Miro connector

Obtain the values of **Client ID** and **Client secret**, and add the **Redirect URL** in Miro account. If you are unable to perform the required steps, run this curl command from your terminal. Replace `<ServiceNow-Instance-Name>` in **client\_uri** and **redirect\_uris** with your ServiceNow instance name:

```
curl --location 'https://mcp.miro.com/register' \
--header 'Content-Type: application/json' \
--data '{
    "client_uri": "https://<ServiceNow-Instance-Name>.service-now.com",
    "grant_types": [
        "authorization_code",
        "refresh_token"
    ],
    "redirect_uris": [
        "https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do",
        "https://<ServiceNow-Instance-Name>.service-now.com/mcp_redirect.do"
    ],
    "client_name": "AutoGen-1775150937195-OAuthProvider",
    "response_types": [
        "code"
    ]
}'
```

