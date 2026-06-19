---
title: Dynamic client registration
description: Connect an MCP connector in Connect Hub to enable AI agents in to interact with an external system using automatic OAuth authorization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/mcp-dcr-a.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
breadcrumb: [Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Dynamic client registration

Connect an MCP connector in Connect Hub to enable AI agents in  to interact with an external system using automatic OAuth authorization.

## Before you begin

-   An account with the third-party system you want to connect to. Ensure that your account has the permissions required to authorize OAuth applications.
-   Role required: wdf\_builder or admin.

## About this task

Dynamic client registration enables you to connect an MCP connector that supports automatic OAuth authorization, such as Linear. In this, Connect Hub redirects you to the third-party provider's authorization page, where you approve the connection. No Client ID or Client secret is required. If the connector you want to use requires manual setup with a Client ID and Client secret, see [Manual client registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/mcp-mcr-a.md).

For the list of MCP connectors for which dynamic client registration is supported, see [Available Enterprise MCP Registries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/mcp-reg-enterprise.md).

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Click **Create** and select **Model Context Protocol**.

    The list of all available MCP connectors is displayed.

    \[Omitted image "list-mcp-reg.jpg"\] Alt text:

3.  Locate the connector you want to use.

    -   To search for a connector by name, enter the connector or system name in the **Search system or connector** field.
    -   To filter by system, select **System**, select one or more systems from the list, and then select **Apply**.
    -   To change the sort order, select **Sort by** and choose the preferred option.
4.  Select the connector card.

    A details panel opens on the right, displaying the connector's description, system, type, endpoint URL, and certification status. If multiple connectors are available for the same system, they are listed under **Other connectors** in the panel.

    \[Omitted image "mcp-dcr-linear.jpg"\] Alt text:

5.  Select **Connect**.

    Connect Hub initiates the OAuth authorization flow and redirects you to the third-party provider's authorization page in a new browser window or tab. The dialog in Connect Hub shows the status message.

6.  In the third-party provider's authorization page, review the requested permissions and select **Approve**.

    \[Omitted image "mcr-approve.jpg"\] Alt text:

7.  Provide the credentials when prompted.

    After authorization completes, the Edit MCP Connector page is displayed with the connection record details. A **Connected** label is displayed next to the connection name when the connector is ready for use.


## Result

The MCP connector is connected to Connect Hub and available for use in AI agent configurations and automation flows.

