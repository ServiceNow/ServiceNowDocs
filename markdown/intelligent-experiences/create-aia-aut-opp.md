---
title: Create an AI agent from an automation opportunity
description: Use automation opportunities identified on your instance to create AI agents in AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-aia-aut-opp.html
release: australia
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 4
breadcrumb: [Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Create an AI agent from an automation opportunity

Use automation opportunities identified on your instance to create AI agents in AI Agent Studio.

## Before you begin

Role required: sn\_aia.admin

## About this task

Automation opportunities are determined by data available on your instance. Analysis of common task types with possible agentic AI solutions yields recommendations with estimated time and cost savings based on the records analyzed. Each opportunity shows a list of steps needed to resolve the task, demonstrating possible automation instructions. Each identified opportunity also provides an estimated number of tools necessary for the AI agent to complete those steps.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Home**.

2.  Select **View all automation opportunities**.

3.  Check the list of automation opportunities, then select the one you'd like to create an AI agent to solve.

    The list can be filtered and sorted by column. By default, the list is sorted by estimated annual savings time.

    You can choose between the **List** or **Gallery** view to display the opportunities. Sorting is not available in the **Gallery** view.

    You can select **AI Agent Advisor** to be directed to the AI Admin Hub where you can review what tables are being monitored for automation opportunities. You can also add tables

4.  Review the automation opportunity preview.

    For more information about the source of the automation opportunity, select **View sample issues**. You can see a list of records, including their number, short description, description, and the analysis of the root cause. You can select a record number to open that record in a new browser tab. When you're done, select **Back** to return to the automation opportunity preview.

    The steps listed in the **Resolution steps** section describe the process that can be automated. The actual prompt for the AI agent will be different than the text shown there.

    The number of tools identified is an estimation. The necessary tools may or may not already exist on your instance.

5.  Select a modality for your AI agent, either **Chat** or **Voice**.

6.  Select **Build AI Agent** to be redirected to the full setup process with the opportunity context applied.

7.  Review the generated content for the AI agent and make modifications to suit your specific needs.

    AI generates the name, description, how-to instructions, and AI agent expertise. It also adds relevant tools if they're available. You may need to create more tools for your AI agent to fulfill all of the steps in the how-to instructions. Steps missing tools are identified in the **Tools** section under the list of currently applied tools.

8.  [Define the security controls for your AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-aia-new.md).

    Specify which users can invoke the AI agent with the **Allowed users** dropdown. If you choose **Users with specific roles**, you can choose which roles are required to use the AI agent.

    Determine the data that your AI agent can access. AI agents that act as a **Dynamic user** have the same data access settings as the user who invoked the AI agent. If you set the user identity as an **AI user**, then the AI agent will have the same data access permissions as the chosen user record. AI users must have the type set to **AI**. Once you select an AI user, you can see which roles it has.

9.  Review the test scenarios.

    Test scenarios are generated automatically as part of the applied opportunity context. They may take a few minutes to generate, so they won't appear right away. Once they're generated, they are added to the AI agent automatically. You can still edit test scenarios after they're generated.

    You can [add your own scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-scenarios-aia.md) or remove unwanted generated ones.

10. [Add a trigger to your AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia-new.md).

    If you only want your AI agent to be used in chats, you don't need to add a trigger.

11. [Select which channels users can access your AI agent from](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/channels-access-aia.md).

    ServiceNow Otto is recommended.

12. Map long-term memory categories.

    For more information about long-term memory, see [Set up long-term memory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/long-term-memory-aia-new.md).

13. Select **Save** to save all changes made to the AI agent.


## Result

A new AI agent is built based on an identified automation opportunity.

Before activating your new AI agent, [manually test your AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) on sample records to confirm it behaves as expected. Select **Run test** to start. You can also [evaluate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md) using your test scenarios to identify behavior patterns and possible optimizations. You can't run both a manual test and an evaluation at the same time.

When you're satisfied with the AI agent's performance, you can select **Activate** to make it available to users.

