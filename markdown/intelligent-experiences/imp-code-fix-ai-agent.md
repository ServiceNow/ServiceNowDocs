---
title: Code fix AI agent
description: This AI Agent automates the process of analyzing, suggesting, and implementing fixes for code violations or issues detected within code repositories or running scripts. It leverages LLM-driven suggestions while keeping the user in control of approval and refinement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/imp-code-fix-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Impact AI agents, Impact, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Code fix AI agent

This AI Agent automates the process of analyzing, suggesting, and implementing fixes for code violations or issues detected within code repositories or running scripts. It leverages LLM-driven suggestions while keeping the user in control of approval and refinement.

## Workflow

The agent helps users complete tasks related to fixing code.

1.  Receive the user's code request.
2.  Execute the appropriate tools to detect and handle code violations.
3.  Allow user-driven approval, rejection, or refinement.

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

Code Violation Handler

Fetch Codefix Issues

Make Additional Changes Handler

Solution Accepted Handler

Solution Rejected Handler


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_impact\_gen\_ai.ai\_fix\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_impact\_gen\_ai.ai\_fix\_user, sn\_se.scan\_engine\_read\_user

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

Code Fix Workflow

</td></tr></tbody>
</table>Learn more about Impact at [Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-landing-page.md).

**Parent Topic:**[Impact AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/impact-ai-agents-overview.md)

