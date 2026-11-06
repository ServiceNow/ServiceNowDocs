---
title: Connect ServiceNow Arc to MCP servers
description: Connect MCP servers so Arc can use tools and data from other services, such as GitHub, Sentry, SerpApi, and Postman. Each server you connect adds capabilities to the agent, and you control which servers each sub-agent can use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/connect-mcp-servers.html
release: australia
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 2
keywords: [MCP servers, authentication]
breadcrumb: [Extend ServiceNow Arc, Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Connect ServiceNow Arc to MCP servers

Connect MCP servers so Arc can use tools and data from other services, such as GitHub, Sentry, SerpApi, and Postman. Each server you connect adds capabilities to the agent, and you control which servers each sub-agent can use.

## Before you begin

Role required: sn\_app\_arc.user

## About this task

**Important:** Local MCP servers run on your device outside the Arc sandbox. After you connect one, it can take actions on your device without asking you to approve each action, and it stays configured when Arc restarts. Your administrator can turn off local MCP servers. For more information, see [Turn off local MCP servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/turn-off-local-mcp-servers.md).

Servers that your administrator provides appear first in the **Available** list, ready to connect. You can't edit or delete them, and the card shows the server's status instead of its URL. To see the URL, hover over the info icon on the card.

**Note:** If your administrator deactivates a server, you can't connect to it unless your administrator activates it.

## Procedure

1.  Navigate to **Settings** &gt; **MCP Servers**.

2.  In the **Available** list, select the connect icon for the server you want to add.

    For a server your administrator provides, select the connect control on its card. You don't enter a name, URL, or credentials, and the remaining steps don't apply.

3.  In the **Server name** field, enter a name for the server.

4.  In the **Server URL** field, enter the server's URL.

    For servers from the Available list, the name and URL are filled in for you.

5.  Expand **Authentication \(optional\)** and enter the credentials if the server requires them.

6.  Select **Add &amp; Connect**.


## Result

The server appears under **Configured**. If the connection succeeds, the agent can use the server's tools, and you can grant access to it when you create a sub-agent.

## What to do next

To reconnect, edit, or remove a server, select the connect, edit, or delete icon on its card under **Configured**.

If a server card shows **Error**, read the message on the card. For example, a message about a missing Authorization header means the server requires credentials. Select the edit icon, add the credentials under **Authentication \(optional\)**, and then select the connect icon.

**Parent Topic:**[Extend ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/extending-cowork.md)

