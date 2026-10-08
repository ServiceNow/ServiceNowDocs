---
title: Connect ServiceNow Cowork to MCP servers
description: Connect MCP servers so Cowork can use tools and data from other services, such as GitHub, Sentry, SerpApi, and Postman. Each server you connect adds capabilities to the agent, and you control which servers each sub-agent can use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/connect-mcp-servers.html
release: brazil
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [MCP servers, authentication]
breadcrumb: [Extend ServiceNow Cowork, Use, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Connect ServiceNow Cowork to MCP servers

Connect MCP servers so Cowork can use tools and data from other services, such as GitHub, Sentry, SerpApi, and Postman. Each server you connect adds capabilities to the agent, and you control which servers each sub-agent can use.

## Before you begin

Role required: sn\_app\_cowork.user

## About this task

**Important:** Local MCP servers run on your device outside the Cowork sandbox. After you connect one, it can take actions on your device without asking you to approve each action, and it stays configured when Cowork restarts. Your administrator can turn off local MCP servers. For more information, see [Turn off local MCP servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/turn-off-local-mcp-servers.md).

## Procedure

1.  Navigate to **Settings** &gt; **MCP Servers**.

2.  In the **Available** list, select the install icon for the server you want to add.

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

**Parent Topic:**[Extend ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/extending-cowork.md)

