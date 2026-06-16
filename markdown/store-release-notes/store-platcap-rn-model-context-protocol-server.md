---
title: Model Context Protocol Server release notes
description: Version history for the ServiceNow Model Context Protocol Server application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-model-context-protocol-server.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Model Context Protocol Server release notes

Version history for the ServiceNow® Model Context Protocol Server application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 1.1.0 - December 2025**
    -   The Model Context Protocol defines a standard method of communication between large language models \(LLMs\) and external systems, such as a ServiceNow instance. AI applications connect to an external system from an MCP client, such as an AI agent, using an MCP server. The server tells the client which external resources it can access and how to access them. Then, from an MCP client, users can request information from the server and automate functionality using the available tools and data that the server returns. For general information about the Model Context Protocol and MCP servers, see the Model Context Protocol documentationon the Model Context Protocol website.
    -   With MCP Server Console, you can create MCP servers on an instance and configure the tools that they expose or use a preconfigured Quickstart Server. You can create tools from Now Assist skills or use the tools installed with our Quickstart Model Context Protocol Server. Then any LLM or AI agent \(such as ChatGPT, Microsoft Copilot, or Claude\) can call an MCP server from its MCP client using OAuth 2.0 authentication and get a list of available tools. With these tools, users can prompt the server for information from the instance, such as a list of recently closed incidents or case summaries. You can also use the ServiceNow Model Context Protocol Client application as an MCP client.

**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

