---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection preliminary troubleshooter agentic workflow
description: Use the preliminary troubleshooter agentic workflow to resolve broadband and internet issues.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection preliminary troubleshooter agentic workflow

Use the preliminary troubleshooter agentic workflow to resolve broadband and internet issues.

## Test and repair telecom service issues overview

Resolve the customer issues such as internet or broadband issues using a team of agents in the preliminary troubleshooter agentic workflow.This agentic workflow processes task requests that require payment status, contextual information from similar cases and Knowledge Base articles. This workflow runs autonomously in the background without any user interaction.

The Preliminary troubleshooter agentic workflow supports these tables:

-   Incident
-   Change request
-   Domain order
-   Order task
-   Service problem case

Role required: sn\_tmt\_agentic\_ai.test\_and\_repair\_telecom\_service\_ai\_agent

To modify the Preliminary troubleshooter agentic workflow [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Role masking

Required role: sn\_tmt\_agentic\_ai.test\_and\_repair\_telecom\_service\_ai\_agent

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

## Preliminary troubleshooter agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Preliminary troubleshooter**.

To create a new agentic workflow, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Start manual test**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

## AI agents used in the Service test and repair agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

To create an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).

<table id="table_gzg_pqh_l2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Task information collector AI Agent V2

</td><td>

Collects the task information and validates the task.

</td></tr><tr><td>

Customer payment status AI Agent V2

</td><td>

Checks for outstanding bill payments.

</td></tr><tr><td>

Preliminary troubleshooter AI Agent V2

</td><td>

-   AI agent designed to ask questions that are fetched from the structured question generator.
-   Activate the structured question generator skill to generate the questions from the skill.
-   Summarizes the resolution plan by checking the similar cases and Knowledge Base articles.

</td></tr></tbody>
</table>