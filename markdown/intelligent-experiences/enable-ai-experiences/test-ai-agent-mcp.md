---
title: Test an AI agent
description: Analyze the performance of an AI agent that has a Model Context Protocol \(MCP\) tool added to it to verify that it functions the way you defined it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/test-ai-agent-mcp.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Configure Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Test an AI agent

Analyze the performance of an AI agent that has a Model Context Protocol \(MCP\) tool added to it to verify that it functions the way you defined it.

## Before you begin

Role required: sn\_aia.admin

## About this task

After you create an AI agent and add an MCP tool to it, test the AI agent to confirm that it functions the way you defined it. Search for the AI agent, select the version, and provide a task with a concise summary and a reference number to begin testing.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.

2.  In the **Test AI reasoning** tab, search for and select the AI agent that you want to test.

3.  In the Version drop-down list, select a version of the AI agent.

4.  In the **Task** field, provide a concise summary of the task you want to achieve.

    **Note:** In the task summary, include a reference number or specific record to achieve results pertaining to a task your AI agent can perform.

5.  Select **Start test**.

    \[Omitted image "test-aia-mcp.png"\] Alt text: The Test AI reasoning tab, which includes the search field, the Version drop-down list, and the Task field.

    You’re directed to the **Chat responses** tab, where you can see Now Assist executing operations to test the AI agent.

6.  Complete the testing by selecting **Log in** and authenticating the MCP server.

    \[Omitted image "chat-response-mcp-test.png"\] Alt text: The Chat responses tab that shows the operations for testing an AI agent. A message indicates that the operation requires authentication.

    **Note:**

    -   The **Log in** button is visible only if the server isn’t authenticated.
    -   Enabling access to the MCP server refreshes the Testing page and resumes testing in the **Chat responses** tab.
    -   The OAuth token used for the authentication is saved in the OAuth Credentials table \[oauth\_credential\].

