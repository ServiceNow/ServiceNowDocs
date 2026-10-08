---
title: Create an agentic workflow
description: Create an agentic workflow in AI Agent Studio to coordinate multiple AI agents and solve complex problems that require collaboration across specialized agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-aw-new.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 3
breadcrumb: [AI Agent Studio, AI agents and agentic workflows, Enable AI Experiences]
---

# Create an agentic workflow

Create an agentic workflow in AI Agent Studio to coordinate multiple AI agents and solve complex problems that require collaboration across specialized agents.

## Before you begin

Role required: sn\_aia.admin

## About this task

In the ServiceNow agentic ecosystem, an agentic workflow is a coordinated set of AI agents that work together to solve complex problems. While individual AI agents solve discrete tasks, an agentic workflow orchestrates multiple specialized agents to tackle larger, more complex objectives.

An agentic workflow uses the AI Agent Orchestrator to coordinate agents, delegate subtasks, and manage communication between agents to resolve the overall problem.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Home**.

2.  Select **Create new agentic solution**, then select **New agentic workflow for a process**.

3.  In the New Agentic Workflow pop-up window, describe your agentic workflow and select **Next**.

    Alternatively, you can select **Skip** to open a new agentic workflow form.

4.  Select **Create a workflow from scratch** and select **Next**.

5.  Describe the purpose of the agentic workflow, then select **Check**.

    A large language model \(LLM\) uses your description to generate suggested content for the general prompt of the agentic workflow. The LLM also uses the description to generate AI agent suggestions that help the agentic workflow achieve its goal.

    If other agentic solutions accomplish a goal similar to the one you describe, the check identifies them so you can edit a matching solution instead.

    You can skip this step by selecting **Skip**.

6.  [Review or draft the content in the **Expected behavior** section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-aw-new.md).

    You can edit any content that the LLM generates.

    The Orchestrator uses the description and instructions when the agentic workflow is invoked. This content gives the Orchestrator the context it requires to coordinate agents for the workflow's purpose.

    After making any changes to the agentic workflow in this guided setup, you can select **Save** to save your progress.

7.  [Add AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-aia-aw-new.md) that work together within the agentic workflow.

    AI agents provide the specialized capabilities that the agentic workflow coordinates. The agentic workflow orchestrates these agents to solve complex problems collaboratively.

8.  [Define the agentic workflow access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-aw-new.md).

    The security controls configure user access and data access to the agentic workflow.

9.  [Add test scenarios for evaluations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-scenarios-aia.md).

    Automated evaluations of your agentic workflow require configured test scenarios to run against. You can add existing table records as scenarios or manually enter different test objectives to cover the full range of conditions your agentic workflow can encounter.

10. [Add a trigger to automatically invoke your agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aw-new.md) if a specified event occurs.

    A trigger isn't required if your agentic workflow is used only in chats.

11. [Determine how and where users can engage with your agentic workflow and set the processing messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/channels-access-aw-new.md).

    Agentic workflows can be invoked through Virtual Agent assistants, UI actions, or both. You can configure how the workflow communicates its progress to users.

12. Select **Save** to save your changes.


## Result

Your agentic workflow has the AI agents and context that it requires to coordinate work across multiple specialized agents.

## What to do next

To make your agentic workflow ready for use, select **Activate**.

You can [test your agentic workflow manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/test-ai-asset-new.md) to see an example execution. You can also [create an automated agentic evaluation to test the agentic workflow over repeated interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/launch-aia-eval.md). Automated evaluations can display optimization suggestions when LLM judges detect patterns behind low success rates.

