---
title: Classify service and CI AI agent
description: This AI agent assigns the appropriate service and offering to an incident. It can also assign the appropriate configuration item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-classify-service-and-ci-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Classify service and CI AI agent

This AI agent assigns the appropriate service and offering to an incident. It can also assign the appropriate configuration item.

## Workflow

The agent helps users complete tasks related to classify service and ci.

1.  Find candidates.
2.  Choose recommendations.
3.  Present recommendations to the user.
4.  Update the incident if meaningful recommendations were found.

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

Find candidates

Update incident


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

itil, sn\_service\_desk\_agent

</td></tr><tr><td>

Data access roles

</td><td>

itsm.aia.worker, access\_analyzer\_ai\_user, actsub\_user, agent\_role\_config\_viewer, agent\_workspace\_user, app\_service\_user, canvas\_user, certification, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, contact\_user, data\_manager\_user, dependency\_views, email\_client\_template\_read, email\_composer, interaction\_agent, itil, knowledge, notify\_view, now\_assist\_panel\_user, one\_extend\_viewer, pa\_viewer, platform\_ml\_read, prompt\_library\_user, role\_viewer, service\_status\_subscriber, service\_viewer, snc\_internal, snc\_platform\_rest\_api\_access, snc\_required\_script\_writer\_permission, sn\_ace.ace\_user, sn\_aia.viewer, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_bm\_client.benchmark\_data\_viewer, sn\_change\_read, sn\_change\_write, sn\_cimaf.sn\_cimaf\_read, sn\_cmdb\_user, sn\_comm\_management.comm\_plan\_viewer, sn\_data\_kit.analyst, sn\_dex\_desktop.notification\_template\_admin, sn\_diagram\_builder.db\_read, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_gd\_guidance.guidance\_user, sn\_incident\_read, sn\_incident\_write, sn\_itam\_recomm.recommendations\_read, sn\_itsm\_aia.sn\_aia\_chg\_conflict, sn\_itsm\_aia.sn\_aia\_chg\_quality, sn\_itsm\_aia.sn\_aia\_chg\_schedule, sn\_itsm\_contact\_query, sn\_mcp\_client.viewer, sn\_nb\_action.next\_best\_action\_user, sn\_nowassist\_admin.user, sn\_now\_canvas\_ai.interactive\_view\_user, sn\_pren.experience\_issue\_read, sn\_problem\_read, sn\_problem\_write, sn\_prompt\_assist.prompt\_developer, sn\_publications\_recipients\_list\_user, sn\_publications\_recipients\_user, sn\_query\_gen.user, sn\_reacf.sn\_remedial\_action\_read, sn\_request\_approver\_read, sn\_request\_read, sn\_request\_write, sn\_skill\_builder.viewer, sn\_sla\_definition\_query, sn\_sow.it\_agent\_dashboard\_user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sttrm\_condition\_read, sn\_uib\_collab.user, sn\_uxc\_gen\_ai.sn\_aia\_sla\_explain, survey\_reader, task\_editor, template\_editor, template\_read\_global, tracked\_file\_reader, view\_changer, viz\_creator, workspace\_user

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

-   Triage and categorize ITSM incident
-   ITSM Agent Zero

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

