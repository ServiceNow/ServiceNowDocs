---
title: Test an AI agent
description: Analyze the performance of an AI agent when it provides a resolution plan for your AI agentso you can see that it functions the way that you defined it.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Test an AI agent

Analyze the performance of an AI agent when it provides a resolution plan for your AI agentso you can see that it functions the way that you defined it.

## Before you begin

Role required: sn\_aia\_admin and either admin or at least one role required by the ACL of the AI agent being testing and each of the ACLs of its downstream components

## About this task

After you create an AI agent, test it to see that it functions the way that you defined it. You must select the **AI agent** radio button to test an AI agent. Select the AI agent that you want to test and provide a task with a concise summary and a reference number in the **Task** field to begin testing the AI agent.

When testing, you can see how the AI agent interacts with the AI Agent Orchestrator, an agent that directs different AI agents, and the Communicator, an agent that focuses on facilitating communication between agents and the Orchestrator.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.

2.  In the **Test scenario** tab, under the What to test section, select the **AI agent** button.

3.  In the Select one drop-down list, select an AI agent that you want to test.

4.  In the **Task** field, provide a concise summary of the task to be achieved.

    **Note:** In the task summary, include a reference number or specific record for better results during your testing.

5.  Select **Start test**.

    ![Selecting an AI agent for testing in AI Agent Studio.](../image/select-ai-agent-test-new.png)

    You’re directed to the **Output** tab, where you can see Now Assist executing operations to test the AI agent.


## Result

When testing an AI agent, you can see the AI agent Orchestrator and Communicator working together to organize and manage the AI agents like a team. The AI agent Orchestrator assigns the individual, specialized agents to complete the subtasks. The AI agent Communicator lets the AI agent Orchestrator know the status of each agent.

**Note:** If you don't have the roles necessary to pass the ACLs of the AI agent or all of its tools, you will be notified that you don't have the necessary access and the test won't execute.

![Output from a tested AI agent with the task given to it.](../image/ai-agent-test-output.png "Testing an AI agent")

-   A simulated chat experience begins on the Now Assist panel between your fulfiller agent and AI agent.
-   A diagram shows the tasks and communication of the AI agents that are working together to solve the case.
-   A decision log records the thought process of each AI agent that is involved.

    **Note:** You can view the entire decision log by selecting **Download logs**.


You can restart the entire testing process at any time by selecting **Restart**.

