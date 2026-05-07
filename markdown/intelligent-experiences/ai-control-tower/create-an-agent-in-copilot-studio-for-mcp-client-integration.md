---
title: Connecting with Microsoft Copilot Studio Via AI Gateway
description: Connecting with a Microsoft Copilot Studio via AI Gateway.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect to MCP servers Via AI Gateway, AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# Connecting with Microsoft Copilot Studio Via AI Gateway

Connecting with a Microsoft Copilot Studio via AI Gateway.

## Before you begin

Role required: Workspace user

## Procedure

1.  Log in to MCP client \(https://copilotstudio.microsoft.com\).

2.  Creating an agent.

    1.  Navigate to **Agents**.

    2.  Select **+New agent**.

    3.  While creating an agent, navigate to the **Configure** tab.

    4.  Enter the Name.

    5.  Enter the description.

    6.  Select **Create**.

        An agent is created.

3.  Adding tools to the agent in Microsoft Copilot Studio

    1.  Open the Agent and navigate to **Tools** tab.

    2.  Select **+Add a tool**.

    3.  Select **Model Context Protocol** icon.

    4.  Select **+New tool**.

    5.  Select **Model Context Protocol**.

        Displays Add a model Context Protocol server \(preview\) window.

    6.  Enter the Server name, Server description, and Server URL.

        The MCP server URL is the Server URL and the details are available in the AI Gateway setup tab.

    7.  Select Authentication: OAuth 2.0.

    8.  Select type: Manual.

    9.  Enter the Client ID and Client secret.

        The Client ID and Client secret details are available in the MCP server record created for Microsoft Copilot Studio.

    10. Enter the Authorization URL and Token URL template.

        The Authorization endpoint URL and Token URL template are available on the AI Gateway setup tab.

    11. Enter the Refresh URL.

        The Refresh URL is same as the Token URL.

    12. Select **Create**.

        Your tool gets created successfully and generates a Redirect URL.

4.  Copy the Redirect URL and paste in the Redirect URL field in the MCP server record.

5.  Select **Save** to save the MCP server record.

6.  Navigate to **ALL** &gt; **Application registry** and look for the Copilot MCP server record.

7.  Verify to change the values of **Always use PKCE** and **Public Client** from **True** to **False** of the server record.

    This step is only applicable for Microsoft Copilot Studio.

8.  Save the Copilot MCP server record.

9.  Navigate back to the Copilot Studio.

10. Select **Next**.

11. Select **Create new connection**.

12. Select **Approve**.

13. After getting connected, select **Add to agent**.

14. Open the connection manager and provide authentication to Copilot.

    This step is only applicable for Microsoft Copilot Studio.

15. Select **Connect**.

16. Select **Submit**.


