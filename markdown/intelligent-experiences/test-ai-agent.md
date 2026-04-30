---
title: Manually test the execution of an AI agent
description: Analyze the execution of an AI agent so you can see that it functions the way that you defined it.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Manually test the execution of an AI agent

Analyze the execution of an AI agent so you can see that it functions the way that you defined it.

## Before you begin

Role required: sn\_aia\_admin and either admin or at least one role required by the ACL of the AI agent being testing and each of the ACLs of its downstream components

## About this task

After you create an AI agent, test it to see that it functions the way that you defined it. You can choose to run a manual test with a single instruction to test its basic functioning, or you can evaluate the AI agent's performance across multiple executions.

If you want to test multiple executions using execution logs, you can run an automated test. If you select **Start automated evaluation**, the agentic evaluation guided setup opens in a new browser tab. See [Evaluate an AI agent](execute-aia-eval.md) for more details about running a new automated evaluation.

When manually testing performance, you can see how the AI agent interacts with the AI Agent Orchestrator and the Communicator AI agent. The Orchestration is an agent that directs different AI agents, and the Communicator AI agent facilitates the communication between the user and other AI agents.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.

2.  Select **Start manual test**.

    If you want to start an automated test, see [Evaluate an AI agent](execute-aia-eval.md) for more details on that process.

3.  In the **Test type** drop-down meny, select **AI agent or workflow**.

    If you want to test user access security controls, see [Test AI agent user access](test-aia-access.md).

4.  Select an agentic workflow or AI agent that you want to test by searching the name of a workflow or choosing from the drop-down menu.

5.  In the Version drop-down list, select the version of the AI agent you want to test.

    See [Version control for AI agents and agentic workflows](../concept/version-control.md) for more information about creating and changing versions.

6.  In the **Task** field, provide a concise summary of the task to be achieved.

    **Note:** In the task summary, include a reference number or specific record for better results during your testing.

    ![Complete testing form](../image/test-aia-perf-form.png)

7.  Select **Continue to Test Chat Response**.


## Result

When testing an AI agent, you can see the AI agent Orchestrator and Communicator working together to organize and manage the AI agents like a team. The AI agent Orchestrator assigns the individual, specialized agents to complete the subtasks. The AI agent Communicator lets the AI agent Orchestrator know the status of each agent.

**Note:** If you don't have the roles necessary to pass the ACLs of the AI agent and all of its tools, you’ll be notified that you don't have the necessary access and the test won't execute.

Your AI agent starts to execute the test autonomously to resolve the task.

![Output from a tested AI agent with the task given to it.](../image/aia-test-playground.png "Testing an AI agent")

-   A simulated chat experience begins on the Now Assist panel between your invoking user and AI agent.
-   A diagram shows the tasks and communication of the AI agents that are working together to solve the case.
-   A decision log records the thought process of each AI agent that is involved in solving the agentic workflow.

    **Note:** You can view the entire decision log by selecting **Download logs**.


You can restart the entire testing process at any time by selecting **Restart**.

