---
title: CMDB health metrics manager AI agent
description: Performs actions related to the CMDB health metrics
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cmdb-cmdb-health-metrics-manager-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [CMDB AI agents, CMDB, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# CMDB health metrics manager AI agent

Performs actions related to the CMDB health metrics

## Workflow

The agent helps users complete tasks related to CMDB health metrics manager.

1.  If you have done it before, skip to step 2.
2.  Check the CMDB health dashboard jobs and health metrics.
3.  If there are no health metrics calculated, skip to step 5.
4.  If there are metric scores retrieved, ask the user if they want to retrieve the health scores for all principal classes, and if not, which specific class or classes instead.
5.  Retrieve the health scores for the selected CI classes.
6.  Inform the user that they have completed the step of going through the CMDB health metrics.

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

-   **Script**

Check CMDB health dashboard jobs and health metrics

Get CMDB health scores

Get similar CI Classes


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal, sn\_cmdb\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

CMDB Data Governance

</td></tr></tbody>
</table>Learn more about Configuration Management Database \(CMDB\) at [Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_ITILConfigurationManagement.md).

**Parent Topic:**[CMDB AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cmdb-ai-agents-overview.md)

