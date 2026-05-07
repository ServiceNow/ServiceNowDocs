---
title: Exploring AI Agent Advisor
description: AI Agent Advisor automatically discovers automation opportunities in your instance and helps you to deploy AI agents to implement them.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-15"
reading_time_minutes: 2
keywords: [explore]
breadcrumb: [AI Agent Advisor, Enable AI experiences]
---

# Exploring AI Agent Advisor

AI Agent Advisor automatically discovers automation opportunities in your instance and helps you to deploy AI agents to implement them.

## AI Agent Advisor overview

AI Agent Advisor analyzes your instance data to identify the most frequent and impactful opportunities for efficiency gains in your workflows. For each identified opportunity, it proposes AI agents that can automate the solution, and generates new agents when no existing match is available.

This gives the Now Assist administrator a data-driven starting point for AI adoption, eliminating the guesswork of deciding where to apply automation.

## AI Agent Advisor users

The following table lists the primary users of AI Agent Advisor.

<table id="table_rzv_n21_k3c"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Now Assist Administrators

</td><td>

Now Assist administrators responsible for organization-wide AI deployment and management

</td></tr><tr><td>

Platform administrators

</td><td>

Platform administrators overseeing enterprise AI governance

</td></tr><tr><td>

AI builders and practitioners

</td><td>

AI practitioners building and deploying custom AI solutions across ServiceNow workflows

</td></tr></tbody>
</table>## AI Agent Advisor workflow

AI Agent Advisor operates through three sequential phases:

-   **Mine**

    The system analyzes the records in your instance \(for example, incident and case records\) on a scheduled basis to identify recurring problems that are candidates for automation.

    You can configure the data sources, filters, and schedule to target the most relevant records for your organization.

-   **Match**

    For each identified opportunity, the system maps the resolution steps to existing AI agents, tools, and agentic workflows already available on your platform.

-   **Make**

    When no existing agent is a strong match for a resolution step, the system generates a new AI agent tailored to that specific problem.


The result is a prioritized list of automation opportunities. Each opportunity displays the estimated time savings, estimated return on investment \(ROI\), number of related requests, number of matched AI assets, and proposed resolution steps. AI Agent Advisor generates the resolution steps using the data from existing records on your instance. You can use this list to decide which opportunities to act on first.

## AI Agent Advisor benefits

AI Agent Advisor provides the following benefits.

<table id="table_u3s_hpz_q3c"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

User

</th></tr></thead><tbody><tr><td>

Quickly discover automation opportunities for your instance. AI Agent Advisor analyzes actual instance data to identify and propose AI automations that provide the greatest efficiency gains.

</td><td>

[Automation discovery with AI Agent Advisor](now-assist-center-using-ai-agent-advisor.md)

</td><td>

Now Assist administrator

</td></tr><tr><td>

Matches identified automation opportunities to existing AI agents on the platform and supports automated creation and deployment of new agents, shortening the path from insight to action.

</td><td>

[AI agent matching and automated deployment](../task/activate-automation-opportunity-now-assist-center.md)

</td><td>

Now Assist administrator

 AI developer

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using AI Agent Advisor, see:

-   [Configuring AI Agent Advisor](configuring-ai-agent-advisor.md)
-   [Using AI Agent Advisor](using-ai-agent-advisor.md)
-   [AI Agent Advisor reference](ai-agent-advisor-reference.md)

