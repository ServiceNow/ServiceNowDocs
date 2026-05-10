---
title: Manually test the execution of an agentic workflow
description: Test your agentic workflow in AI Agent Studio to analyze how it functions while it executes the instructions that you defined.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Create an agentic workflow, Now Assist AI agents, Enable AI experiences]
---

# Manually test the execution of an agentic workflow

Test your agentic workflow in AI Agent Studio to analyze how it functions while it executes the instructions that you defined.

## Before you begin

Role required: sn\_aia\_admin and either admin or at least one role required by the ACL of the agentic workflow being testing and each of the ACLs of its downstream components

## About this task

After you create an agentic workflow, test it to see that it functions the way that you defined it. You can choose to run a manual test with a single instruction to test its basic functioning, or you can evaluate the AI agent's performance across multiple executions.

If you want to test multiple executions using execution logs, you can run an automated test. If you select **Start automated evaluation**, the agentic evaluation guided setup opens in a new browser tab. See [Evaluate an agentic workflow](execute-aia-eval.md) for more details about running a new automated evaluation.

When manually testing performance, you can see how the agentic workflow and its AI agents interact with the AI Agent Orchestrator and the Communicator AI agent. The Orchestration is an agent that directs different AI agents, and the Communicator AI agent facilitates the communication between the user and other AI agents.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.

2.  Select **Start manual test**.

    If you want to start an automated test, see [Evaluate an agentic workflow](execute-aia-eval.md) for more details on that process.

3.  In the **Choose a test type** drop-down menu, select **AI agent or workflow**.

    If you want to test user access security controls, see [Test AI agent user access](test-aia-access.md).

4.  Select an agentic workflow that you want to test by entering the name of a workflow or choosing from the drop-down menu.

5.  Under **Choose a testing mode**, select the testing mode either as **Premium Chat** or **Standard**.

    **Note:** The Premium Chat testing mode is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

6.  In the Version drop-down list, select the version of the AI agent you want to test.

    See [Version control for AI agents and agentic workflows](../concept/version-control.md) for more information about creating and changing versions.

7.  In the Task drop-down list, provide a concise summary of the task to be achieved.

    **Note:** In the task summary, include a reference number for a specific record for better results during your testing.

    ![Complete the testing form.](../image/test-aw-manually-new.png)

8.  Select **Continue to Test Chat Response**.


## Result

When testing an agentic workflow, you can see the AI Agent Orchestrator and AI Agent Communicator working together to organize and manage the AI agents like a team. The AI agent Orchestrator assigns the individual, specialized agents to complete the subtasks. The AI Agent Communicator lets the AI Agent Orchestrator know the status of each agent.

**Note:** If you don't have the roles necessary to pass the ACLs of the agentic workflow and all of its AI agents and tools, you're notified that you don't have the necessary access and the test won't execute.

Your AI agents start to execute the test autonomously to resolve the agentic workflow by taking the input from the live agent as required.

![Output from a tested agentic workflow with the task given to it.](../image/aia-test-playground.png "Testing an agentic workflow")

-   A simulated chat experience begins on the Now Assist panel between your invoking user and AI agent.
-   At the top of the canvas, you can see information about the agentic workflow you're testing, including its name, version, and description.
-   A diagram shows the tasks and communication of the AI agents that are working together to solve the case.
-   A decision log records the thought process of each AI agent that is involved in solving the agentic workflow.

    **Note:** You can view the entire decision log by selecting **Download logs**.


You can restart the entire testing process at any time by selecting **Restart**.

