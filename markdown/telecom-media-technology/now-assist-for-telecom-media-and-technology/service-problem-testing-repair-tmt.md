---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection test and repair telecom service issues agentic workflow
description: Use the Test and repair telecom service issues agentic workflow to resolve broadband and internet issues.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection test and repair telecom service issues agentic workflow

Use the Test and repair telecom service issues agentic workflow to resolve broadband and internet issues.

## Test and repair telecom service issues overview

Resolve the customer issues using a team of AI agents in the Test and repair telecom service issues agentic workflow. It can handle task requests that require troubleshooting, diagnostics, analysis, or resolution for a task \(case\), whether an identifier or description for the task is given.

The Test and repair telecom service issues agentic workflow supports these tables:

-   Incident
-   Change request
-   Domain order
-   Order task
-   Service problem case

Role required: sn\_tmt\_agentic\_ai.test\_and\_repair\_telecom\_service\_ai\_agent

To modify the Test and repair telecom service issues agentic workflow [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Role masking

Required role: sn\_tmt\_agentic\_ai.test\_and\_repair\_telecom\_service\_ai\_agent

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Test and repair telecom service issues agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Test and repair telecom service issues**.

To create a new agentic workflow, see [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test use cases**.

To test the use case, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## AI agents used in the Test and repair telecom service issues agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

To create an AI agent, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

<table id="table_gzg_pqh_l2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Service problem manager AI agent

</td><td>

An AI agent is responsible for planning, orchestrating, and delegating work to other agents.

 Checks the customer inventory status.

 Shows the Knowledge articles.

</td></tr><tr><td>

Payment status checker AI agent

</td><td>

Checks for outstanding bill payments.

</td></tr><tr><td>

Preliminary troubleshooter AI agent

</td><td>

AI agent designed to ask questions that are fetched from the structured question generator.

 Activate the structured question generator skill to generate the questions from the skill.

 Check for similar cases for the resolution plan and asks questions from Knowledge Base articles to determine the resolution.

</td></tr><tr><td>

On-demand service tester AI agent

</td><td>

Create a diagnostic task based on the inventory specifications for a Service problem case and execute a test definition.

</td></tr><tr><td>

Service repairer AI agent

</td><td>

Create the repair task for the test runs.

</td></tr></tbody>
</table>