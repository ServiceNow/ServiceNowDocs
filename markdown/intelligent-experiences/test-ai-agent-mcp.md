---
title: Test an AI agent
description: Analyze the performance of an AI agent with a Model Context Protocol tool added to it to verify that it functions the way that you defined it.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Configuring Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Test an AI agent

Analyze the performance of an AI agent with a Model Context Protocol tool added to it to verify that it functions the way that you defined it.

## Before you begin

Role required: sn\_aia.admin

## About this task

After you create an AI agent and a Model Context Protocol to it as a tool, test it to see that it functions the way that you defined it. Search for the AI agent that you want to test and select the version from the Version drop-down and provide a task with a concise summary and a reference number in the **Task** field to begin testing the AI agent.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.

2.  In the **Test AI reasoning** tab, use the Search bar to search and select the AI agent that you want to test.

3.  In the Version drop-down list, select the version of the AI agent.

4.  In the **Task** field, provide a concise summary of the task to be achieved.

    **Note:** In the task summary, include a reference number or specific record for better results during your testing.

5.  Select **Start test**.

    ![Selecting an AI agent for testing in the AI Agent Studio.](../image/test-aia-mcp.png)

    You’re directed to the **Chat responses** tab, where you can see Now Assist executing operations to test the AI agent.

    ![Initial chat response from testing an AI agent that has an MCP tool indicating that it requires authentication.](../image/chat-response-mcp-test.png)

6.  Select **Log in** and authenticate the MCP server to complete the testing.

    **Note:**

    -   Log in will be visible only if the server isn’t authenticated.
    -   Enabling access to the MCP Server refreshes the whole Testing page and resumes testing in the Chat responses tab. The OAuth token used for the authentication is saved in the OAuth Credentials table \[oauth\_credential\].
    ![The AI agent with an MCP tool has been successfully tested.](../image/mcp-test-complete.png)


