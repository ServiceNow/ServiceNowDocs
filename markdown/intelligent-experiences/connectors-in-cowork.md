---
title: Connectors in ServiceNow Cowork
description: Connectors link ServiceNow Cowork to the platforms you work in, so Cowork can read and update your real data, not just answer questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/connectors-in-cowork.html
release: brazil
topic_type: concept
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [connectors, MCP]
breadcrumb: [Use, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Connectors in ServiceNow Cowork

Connectors link ServiceNow Cowork to the platforms you work in, so Cowork can read and update your real data, not just answer questions.

With connector, Cowork works across your platforms as part of any task you assign. For example, it can update incidents, schedule meetings, send email, and review GitHub pull requests, and it can combine these actions to complete larger pieces of work from start to finish.

Cowork includes connectors for ServiceNow, Microsoft 365, and GitHub. Each connector uses the authentication method that its platform supports. For example, the Microsoft 365 connector uses your Microsoft account sign in and covers mail, calendar, OneDrive files, Teams chats and channels, and directory users and groups. Cowork stores the connector tokens locally and refreshes them automatically, about every 90 days.

## Connectors and MCP servers

Connectors and Model Context Protocol \(MCP\) servers both extend what Cowork can do, but they serve different purposes. Connectors are integrations with deep capabilities for ServiceNow, Microsoft 365, and GitHub. MCP servers add tools from other services, such as Sentry, SerpApi, or Postman, and you can choose which MCP servers each subagent can use. Use a connector when one is available for your platform, and add an MCP server for services that connectors don't cover. A remote MCP server connects through a server URL, while a local MCP server runs on your device outside the agent sandbox.

You can view and add connectors from **Settings** &gt; **Connectors**.

-   **[Connect ServiceNow Cowork to Microsoft 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/connect-cowork-microsoft.md)**  
Connect your Microsoft account so ServiceNow Cowork can work with your mail, calendar, Microsoft OneDrive files, and Teams chats and channels. After you connect, you can ask Cowork to draft and send email, schedule meetings, find files, and post to Microsoft Teams.
-   **[Connect ServiceNow Cowork to GitHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/connect-cowork-github.md)**  
Connect ServiceNow Cowork to GitHub or GitHub Enterprise to enable pull request review, CI checks, read code, and manage issues.

**Parent Topic:**[Using ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-cowork-using.md)

