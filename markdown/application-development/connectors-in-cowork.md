---
title: Connectors in ServiceNow Arc
description: Connectors link ServiceNow Arc to the platforms you work in, so Arc can read and update your real data, not only answer questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/connectors-in-cowork.html
release: australia
topic_type: concept
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [connectors, MCP]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Connectors in ServiceNow Arc

Connectors link ServiceNow Arc to the platforms you work in, so Arc can read and update your real data, not only answer questions.

With connectors, Arc works across your platforms as part of any task you assign. For example, it can update incidents, schedule meetings, send email, and review GitHub pull requests, and it can combine these actions to complete larger pieces of work from start to finish.

Arc includes connectors for ServiceNow, Microsoft 365, and GitHub. Each connector uses the authentication method that its platform supports. For example, the Microsoft 365 connector uses your Microsoft account sign in and covers mail, calendar, OneDrive files, Teams chats and channels, and directory users and groups. Arc stores the connector tokens locally and refreshes them automatically, about every 90 days.

## Connectors and MCP servers

Connectors and Model Context Protocol \(MCP\) servers both extend what Arc can do, but they serve different purposes. Connectors are integrations with deep capabilities for ServiceNow, Microsoft 365, and GitHub. MCP servers add tools from other services, such as Sentry, SerpApi, or Postman, and you can choose which MCP servers each subagent can use. Use a connector when one is available for your platform, and add an MCP server for services that connectors don't cover. A remote MCP server connects through a server URL, while a local MCP server runs on your device outside the agent sandbox.

You can view and add connectors from **Settings** &gt; **Connectors**.

-   **[Connect ServiceNow Arc to Microsoft 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/connect-cowork-microsoft.md)**  
Connect your Microsoft account so ServiceNow Arc can work with your mail, calendar, Microsoft OneDrive files, and Teams chats and channels. After you connect, you can ask Arc to draft and send email, schedule meetings, find files, and post to Microsoft Teams.
-   **[Manage Microsoft 365 action permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/set-m365-permissions.md)**  
For each Microsoft 365 action, such as reading Microsoft Teams messages or sending email, select whether Arc takes the action without asking, asks you every time, or never takes it.
-   **[Connect ServiceNow Arc to GitHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/connect-cowork-github.md)**  
Connect ServiceNow Arc to GitHub or GitHub Enterprise to enable pull request review, CI checks, read code, and manage issues.

**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)

