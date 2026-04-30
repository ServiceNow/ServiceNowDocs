---
title: Test an agentic workflow
description: Test your agentic workflow in AI Agent Studio to analyze its performance while it executes the instructions that you defined.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create an agentic workflow, Now Assist AI agents, Enable AI experiences]
---

# Test an agentic workflow

Test your agentic workflow in AI Agent Studio to analyze its performance while it executes the instructions that you defined.

## Before you begin

Role required: sn\_aia\_admin and either admin or at least one role required by the ACL of the agentic workflow being testing and each of the ACLs of its downstream components

## About this task

After you create an agentic workflow, test the agentic workflow to confirm that it functions the way that you defined it. You must select the **Agentic workflow** radio button to test your agentic workflow. Select the agentic workflow that you want to test and provide a task with a concise summary and a reference number in the **Task** field to begin testing the agentic workflow.

During the agentic workflow testing, you see a simulated chat experience in the AI Agent Studio chat on the **Output** tab. The chat experience is a result of the agentic workflow execution done by the fulfiller and AI agent.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.

2.  On the **Test scenario** tab, in the What to test section, select the **Agentic workflow** radio button.

3.  In the Select one drop-down list, select an agentic workflow that you want to test.

4.  In the Task drop-down list, provide a concise summary of the task to be achieved.

    **Note:** In the task summary, include a reference number for a specific record for better results during your testing.

5.  Select **Start test**.

    ![Select the agentic workflow radio button and provide details for testing.](../image/ais-testing-new.png)

    You're directed to the **Output** tab, where you see Now Assist executing the operations to test your agentic workflow.


## Result

When testing an agentic workflow, you can see the AI Agent Orchestrator and AI Agent Communicator working together to organize and manage the AI agents like a team. The AI agent Orchestrator assigns the individual, specialized agents to complete the subtasks. The AI Agent Communicator lets the AI Agent Orchestrator know the status of each agent.

Your AI agent starts to execute the test autonomously to resolve the agentic workflow by taking the input from the live agent as required.

![Output from a tested agentic workflow with the task given to it.](../image/agentic-workflow-output.png "Testing an agentic workflow")

-   A simulated chat experience begins on the Now Assist panel between your fulfiller agent and AI agent.
-   A diagram shows the tasks and communication of the AI agents that are working together to solve the case.
-   A decision log records the thought process of each AI agent that is involved in solving the agentic workflow.

    **Note:** You can view the entire decision log by selecting **Download logs**.


You can restart the entire testing process at any time by selecting **Restart**.

