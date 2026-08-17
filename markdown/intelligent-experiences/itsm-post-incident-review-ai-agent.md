---
title: Post incident review AI agent
description: This AI agent generates a post-incident review report for the user to review and revise after a major incident report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-post-incident-review-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Post incident review AI agent

This AI agent generates a post-incident review report for the user to review and revise after a major incident report.

## Workflow

A post-incident review \(PIR\) report is a comprehensive document created after a major incident or disruption has been resolved. Its purpose is to analyze what happened, understand the root causes, and assess the impact of the incident, while also providing actionable recommendations for preventing future occurrences. The report should contain 4 sections: Executive Summary section, Customer / Service Impact section, Detailed Technical Summary section, and Action items &amp; Prevention section.

1.  Collect the details about the major incident, including short description, description, assignment group, assigned to, category, subcategory, service, configuration item, resolution notes, business impact, and activities.
2.  Collect child incidents and related records.
3.  Generate a post-incident review report with four sections.
4.  Collect feedback on the report from the user.
5.  Update the incident record.
6.  Acknowledge the result and conclude the conversation.

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

Fetch incident details

Get child incident details

Get related records

Update post incident summary to major incident


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

itil

</td></tr><tr><td>

Data access roles

</td><td>

itil, major\_incident\_manager, snc\_required\_script\_writer\_permission

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

Post incident review report

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

