---
title: Microsoft Teams application management AI agent
description: This Microsoft Teams integration agent automates tasks related to Microsoft Teams and ServiceNow Integration Hub. The agent manages user application installations by performing actions such as looking up app installations and installing applications for users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spoke-msteams-microsoft-teams-application-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Integration Hub AI agents, Integration Hub, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Microsoft Teams application management AI agent

This Microsoft Teams integration agent automates tasks related to Microsoft Teams and ServiceNow Integration Hub. The agent manages user application installations by performing actions such as looking up app installations and installing applications for users.

## Workflow

1.  Identify whether the user wants to look up installed apps for a user or install an app.
2.  Gather the necessary parameters and perform the operation. For installations, user consent is required before proceeding.

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

-   **Flow Action**

Install Application to User

Look up User App Installation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Integration Hub at [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub.md).

**Parent Topic:**[Integration Hub AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrationhub-ai-agents-overview.md)

