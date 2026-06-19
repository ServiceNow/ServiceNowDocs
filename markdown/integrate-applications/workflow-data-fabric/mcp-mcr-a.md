---
title: Manual client registration
description: Connect to an MCP connector in Connect Hub by providing OAuth 2.1 credentials from the third-party provider, for connectors such as GitHub and Figma that require a registered OAuth application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/mcp-mcr-a.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
breadcrumb: [Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Manual client registration

Connect to an MCP connector in Connect Hub by providing OAuth 2.1 credentials from the third-party provider, for connectors such as GitHub and Figma that require a registered OAuth application.

## Before you begin

-   Note the **Client ID** and **Client secret** generated for your OAuth application. You must provide these values during the connection setup.
-   Some connectors may require additional configurations. See [Additional connector configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/additional-configs-mcr.md) for the list of supported connectors that require additional configurations. If your connector is listed, perform the required configurations before registering the client manually.
-   Role required: wdf\_builder or admin.

## About this task

Some MCP connectors require you to manually supply OAuth 2.1 credentials instead of using an automatic authorization redirect. Connect Hub displays the label **Manual setup may be required** next to connectors that use this method.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Click **Create** and select **Model Context Protocol**.

    The list of all available MCP connectors is displayed.

    \[Omitted image "list-mcp-reg.jpg"\] Alt text:

3.  Locate the connector you want to use.

    -   To search for a connector by name, enter the connector or system name in the **Search system or connector** field.
    -   To filter by system, select **System**, select one or more systems from the list, and then select **Apply**.
    -   To change the sort order, select **Sort by** and choose the preferred option.
4.  Select the connector card for the system you want to connect.

    A details panel opens showing the connector description, system, type, endpoint URL, and the label **Manual setup may be required**.

    \[Omitted image "dcr-github.jpg"\] Alt text:

5.  Select **Connect**.

    The Authentication dialog opens for the selected connector. The dialog shows the authentication method as **OAuth 2.1** and includes fields for authentication..

6.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID from your OAuth application in the third-party system.|
    |Client secret|Client secret from your OAuth application in the third-party system.|
    |Authorization scopes|Optional OAuth scopes as a comma-separated list.|

    **Note:** Refer to the third-party system's OAuth documentation for the list of supported scopes. For example, the Figma connector uses the scope `mcp:connect`. If no scopes are required, leave the field empty.

7.  Select **Connect**.

    \[Omitted image "dcr-connect.jpg"\] Alt text:

    Connect Hub processes the OAuth credentials and creates the connection record. The Edit MCP Connector page is displayed with the connection record details. A **Connected** label is displayed next to the connection name when the connector is ready for use.


## Result

The MCP connector is connected to Connect Hub using the OAuth 2.1 credentials you provided. The connector is available for use in AI agent configurations and automation flows.

