---
title: Jamf application targets removal AI agent
description: This AI agent removes static groups as targets from computer or mobile device applications in Jamf. It identifies the group and application, checks that the group is a target, confirms the request with the user, and reports the result.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-csdv2-jamf-application-targets-removal-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Client Software Distribution 2.0 AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Jamf application targets removal AI agent

This AI agent removes static groups as targets from computer or mobile device applications in Jamf. It identifies the group and application, checks that the group is a target, confirms the request with the user, and reports the result.

## Workflow

The agent helps the user remove a static group as a target of a computer or mobile device application in Jamf.

1.  Ask the user for the group type and, if it can't be inferred, whether the application is a computer or mobile device application.
2.  Ask for the group name or ID.
3.  Look up the group by name and, if several match, ask the user to choose the correct one.
4.  Ask for the application name or ID.
5.  Look up the application by name and, if several match, ask the user to choose the correct one.
6.  Check whether the group is a target of the application and, if it isn't, tell the user that no change is needed.
7.  Ask the user to confirm the request.
8.  Remove the group as a target of the application and report the result, or explain any error that occurred.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Look up Computer Application by Name

Look up Mobile Device Application by Name

Look up Static Computer Group by Name

Look up Static Mobile Device Group by Name

Look up Static User Group by Name

-   **Subflows**

Look up Application Scope

Remove Target Group from Application


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_csd.CSD Admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_csd.CSD Admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Jamf Group Management Agentic Team

</td></tr></tbody>
</table>**Parent Topic:**[Client Software Distribution 2.0 AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-csdv2-ai-agents-overview.md)

**Related topics**  


[Client Software Distribution 2.0 application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/csd-app-2.md)

[Integration Hub solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/solutions.md)

