---
title: Connecting with Copilot Studio Via AI Gateway
description: Connecting with a Copilot Studio via AI Gateway.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Connect to MCP servers Via AI Gateway, Explore AI Gateway, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Connecting with Copilot Studio Via AI Gateway

Connecting with a Copilot Studio via AI Gateway.

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

    6.  Click **Create**.

        An agent is created.

3.  Adding tools to the agent in Copilot Studio

    1.  Open the Agent and navigate to **Tools** tab.

    2.  Click **+Add a tool**.

    3.  Select **Model Context Protocol** icon.

    4.  Select **+New tool**.

    5.  Select **Model Context Protocol**.

        Displays Add a model Context Protocol server \(preview\) window.

    6.  Enter the Server name, Server description, and Server URL.

        The MCP server URL is the Server URL and the details are available in the AI Gateway setup tab.

    7.  Select Authentication: OAuth 2.0.

    8.  Select type: Manual.

    9.  Enter the Client ID and Client secret.

        The Client ID and Client secret details are available in the MCP server record created for Copilot Studio.

    10. Enter the Authorization URL and Token URL template.

        The Authorization endpoint URL and Token URL template are available on the AI Gateway setup tab.

    11. Enter the Refresh URL.

        The Refresh URL is the same as the Token URL.

    12. Click **Create**.

        Your tool gets created successfully and generates a Redirect URL.

4.  Copy the Redirect URL and paste in the Redirect URL field in the MCP server record.

5.  Click **Save** to save the MCP server record.

6.  Navigate to **ALL** &gt; **Application registry** and look for the Copilot MCP server record.

7.  Ensure to change the values of **Always use PKCE** and **Public Client** from **True** to **False** of the server record.

    This step is only applicable for Copilot Studio.

8.  Save the Copilot MCP server record.

9.  Navigate back to the Copilot Studio.

10. Select **Next**.

11. Select **Create new connection**.

12. Select **Approve**.

13. After getting connected, select **Add to agent**.

14. Open the connection manager and provide authentication to Copilot.

    This step is only applicable for Copilot Studio.

15. Click **Connect**.

16. Click **Submit**.


