---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection service test and repair agentic workflow
description: Use the service test and repair agentic workflow to run the test groups that are mapped to a task.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection service test and repair agentic workflow

Use the service test and repair agentic workflow to run the test groups that are mapped to a task.

## Service test and repair overview

Resolve the customer issues using a team of agents in the service test and repair agentic workflow. This agentic workflow processes task requests that require to run the test groups that are mapped to a task and create repair tasks for the failed test runs. This workflow also updates the consolidated summary in work notes and runs autonomously in the background without any user interaction.

The service test and repair agentic workflow supports these tables:

-   Incident
-   Change request
-   Domain order
-   Order task
-   Service problem case

Role required: sn\_tmt\_agentic\_ai.test\_and\_repair\_telecom\_service\_ai\_agent

To modify the service test and repair agentic workflow [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Role masking

Required role: sn\_tmt\_agentic\_ai.test\_and\_repair\_telecom\_service\_ai\_agent

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

## Service test and repair agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Service test and repair**.

To create an agentic workflow, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Start manual test**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

## AI agents used in the Service test and repair agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

To create an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).

|AI agent|AI agent role|
|--------|-------------|
|Task information collector AI Agent V2|Collects task information and validates the given task.|
|On demand service tester AI Agent V2|Creates a diagnostic task based on the inventory specifications for a service problem case and execute a test groups.|
|Service repair AI agent V2|Creates the repair task for the test runs.|

