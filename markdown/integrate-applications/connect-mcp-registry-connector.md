---
title: Connect to an MCP server from the registry
description: Connect to a certified Model Context Protocol \(MCP\) server from the MCP registry in Connect Hub to enable AI agents to access external systems through OAuth 2.0 authentication.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-22"
reading_time_minutes: 2
breadcrumb: [Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Connect to an MCP server from the registry

Connect to a certified Model Context Protocol \(MCP\) server from the MCP registry in Connect Hub to enable AI agents to access external systems through OAuth 2.0 authentication.

## Before you begin

Role required: admin or a role with access to Workflow Data Fabric Connect Hub.

## About this task

The MCP registry in Connect Hub provides a curated list of pre-built connectors for external systems that are certified by ServiceNow and approved for use. Each connector in the registry specifies the transport type, endpoint URL, authentication method, and approval status, so you can evaluate a connector before connecting to it.

When you connect to an MCP server, Connect Hub automatically creates a connection alias using OAuth 2.1 MCP configuration and opens the third-party authorization page so you can approve access. After authorization is complete, the connector is listed on the Connectors page under the Model Context Protocol Connector type with a status of Connected.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Click **Create**.

3.  Select **Model Context Protocol**.

    The available certified registries are displayed.

4.  Select the connector you want to use.

    Each connector card shows the following information to help you choose the right connector.

    |Field|Description|
    |-----|-----------|
    |System|Name of the external system the connector integrates with.|
    |Transport type|Communication protocol used by the MCP server.For example, **streamable-http**.|
    |Endpoint URL|URL of the MCP server endpoint that ServiceNow connects to.|
    |Connector status|Certification and approval status of the connector. Connectors that show **Certified by ServiceNow** and **Approved** have been verified for use.|

    **Tip:** If the connector you need is not listed, click **Create a custom connector** at the bottom of the dialog box.

    The connector detail page opens, showing the system name, description, type, authentication method, endpoint URL, and connector status. Other connectors for the same system are listed in a sidebar.

5.  Review the connector details and click **Connect**.

    An authorization page for the external system is opened in a new browser tab. The page shows the name of the auto-generated OAuth provider, the ServiceNow instance website, and the redirect URIs that will be used after authorization.

6.  On the authorization page, click **Approve**.

    **Note:** If you do not recognize the application requesting access or the redirect URIs do not match your ServiceNow instance URL, click **Cancel** and contact your administrator.

    The external system loads in the browser tab and authenticates the connection. After authentication is complete, the browser redirects back to your ServiceNow instance.


## Result

The Connectors page in Workflow Data Fabric opens and shows the new connector under **Model Context Protocol Connector**. The connection alias page displays the system name, connection name, protocol, and configuration template with a status of **Connected**.

## What to do next

Use the connected MCP connector in flows or AI agent configurations in Workflow Data Fabric to give AI agents access to the external system.

