---
title: Remediation compliance analysis AI agent
description: This Unified Security Exposure Management agent provides insights around remediation target compliance. It provides SLA or compliance statistics about remediation targets. The agent can break down these numbers by attributes such as severity, assignment group, or configuration class item class.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/usem-remediation-compliance-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Unified Security Exposure Management AI agents, Unified Security Exposure Management AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Remediation compliance analysis AI agent

This Unified Security Exposure Management agent provides insights around remediation target compliance. It provides SLA or compliance statistics about remediation targets. The agent can break down these numbers by attributes such as severity, assignment group, or configuration class item class.

## Workflow

1.  Extract the target year, month \(defaults to previous month\), and grouping attribute \(defaults to assignment group\) for the user query.
2.  Retrieve compliance statistics for the specified time period and grouping.
3.  After presenting results, offer three additional options:
    -   **Break down by CI class**

        Re-run the statistics grouped by CI class instead of assignment group.

    -   **Compare against another month**

        Generate a side-by-side comparison of statistics between two months.

    -   **Identify highs/lows**

        Retrieve the full summary and extract which specific assignment groups or CI classes have the highest or lowest missed SLAs for a given severity.

4.  Continue the follow-up loop until the user is finished or asks something outside this agent's scope \(in which case, route to another agent\).

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Generate comparison summary

Get full summary

Get remediation compliance statistics


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_vul\_ai.read\_rem\_insights, sn\_vul\_ai.write\_rem\_insights

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Analyze vulnerability remediation status

</td></tr></tbody>
</table>Learn more about Unified Security Exposure Management at [Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/unified-security-exposure-management-landing-page.md).

**Parent Topic:**[Unified Security Exposure Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/usem-ai-agents-overview.md)

