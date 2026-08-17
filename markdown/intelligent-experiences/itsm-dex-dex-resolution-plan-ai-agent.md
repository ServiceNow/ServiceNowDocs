---
title: DEX resolution plan AI agent
description: This AI agent generates a resolution plan for the given issue based strictly on the root cause provided. The agent ensures all suggested steps are evidence-based, actionable, and aligned with the diagnosed root cause. No resolution is proposed outside these defined sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-dex-dex-resolution-plan-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# DEX resolution plan AI agent

This AI agent generates a resolution plan for the given issue based strictly on the root cause provided. The agent ensures all suggested steps are evidence-based, actionable, and aligned with the diagnosed root cause. No resolution is proposed outside these defined sources.

## Workflow

The agent follows a prioritized sequence of approved sources: DEX resolutions \(including remedial actions, self-help instructions\), past incident resolutions, and knowledge base articles.

1.  Retrieve the root cause of the issue and supporting data \(incident number, device OS, failing component/metric\). If both the root cause and device OS are missing, ask the user for input.
2.  Use the Fetch remedial actions and self-help instructions tool to retrieve DEX resolutions.
3.  Use the Similar incidents and knowledge articles retriever tool to search for relevant records.
4.  Analyze the collected data and construct a resolution plan using DEX resolutions, past incidents, and knowledge articles.
5.  From the remaining data, show up to three of the most relevant resolutions, prioritized in this order: remedial actions, self-help instructions, past incidents, and knowledge articles.
6.  Display the resolution plan to the user.

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

Fetch remedial actions and self-help instructions

Similar incidents and knowledge articles retriever

Stamp resolution plan to incident worknotes


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_incident\_write

</td></tr><tr><td>

Data access roles

</td><td>

dex.incident.ai.worker

access\_analyzer\_ai\_user, action\_designer, action\_write\_enabled, actsub\_user, agent\_client\_collector\_user, agent\_role\_config\_viewer, agent\_workspace\_user, app\_service\_user, canvas\_user, certification, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, contact\_user, data\_manager\_user, data\_mapping\_user, decision\_table\_admin, decision\_table\_reader, dependency\_views, email\_client\_template\_read, email\_composer, fd\_read\_actions, fd\_read\_operations, fd\_read\_operations\_all, flow\_designer, flow\_operator, flow\_write\_enabled, interaction\_agent, itil, knowledge, mbplus\_reader, notify\_view, now\_assist\_panel\_user, one\_extend\_viewer, openapi\_admin, pa\_viewer, personalize\_decision\_table\_input, platform\_ml\_di.admin, platform\_ml\_read, prompt\_library\_user, report\_user, role\_viewer, sam\_user, scan\_user, service\_status\_subscriber, snc\_platform\_rest\_api\_access, sn\_ace.ace\_user, sn\_aia.viewer, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_bm\_client.benchmark\_data\_viewer, sn\_change\_read, sn\_change\_write, sn\_cimaf.sn\_cimaf\_read, sn\_cmdb\_user, sn\_comm\_management.comm\_plan\_viewer, sn\_conv\_fa.conv\_fa\_designer, sn\_data\_kit.analyst, sn\_dex.ai\_user, sn\_dex.engineer, sn\_dex.service\_desk\_user, sn\_dex.user, sn\_dex\_content.user, sn\_dex\_desktop.notification\_template\_admin, sn\_dex\_ms365.user, sn\_dex\_score.dashboard\_user, sn\_dex\_zoom.user, sn\_diagram\_builder.db\_read, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_gd\_guidance.guidance\_user, sn\_incident\_read, sn\_incident\_write, sn\_itam\_recomm.recommendations\_read, sn\_itsm\_aia.sn\_aia\_chg\_conflict, sn\_itsm\_aia.sn\_aia\_chg\_quality, sn\_itsm\_aia.sn\_aia\_chg\_schedule, sn\_itsm\_contact\_query, sn\_mcp\_client.viewer, sn\_nb\_action.next\_best\_action\_user, sn\_nowassist\_admin.user, sn\_now\_canvas\_ai.interactive\_view\_user, sn\_pren.experience\_issue\_read, sn\_problem\_read, sn\_problem\_write, sn\_prompt\_assist.prompt\_developer, sn\_publications\_recipients\_list\_user, sn\_publications\_recipients\_user, sn\_query\_gen.user, sn\_reacf.sn\_remedial\_action\_read, sn\_request\_approver\_read, sn\_request\_read, sn\_request\_write, sn\_skill\_builder.viewer, sn\_sla\_definition\_query, sn\_sow.it\_agent\_dashboard\_user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sttrm\_condition\_read, sn\_sub\_man.admin, sn\_udc.basic\_read, sn\_uib\_collab.user, sn\_uxc\_gen\_ai.sn\_aia\_sla\_explain, sn\_workflow\_studio.workflow\_studio\_read, survey\_reader, task\_editor, template\_editor, template\_read\_global, tracked\_file\_reader, trigger\_designer, trigger\_designer\_read, usage\_admin, view\_changer, viz\_creator, workflow\_ai\_author, workspace\_user

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

DEX issue diagnosis and resolution workflow

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

