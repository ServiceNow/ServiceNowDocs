---
title: LogicMonitor API AI agent
description: This AI agent investigates alerts that originate with LogicMonitor, as well as operator-initiated entity checks. The agent parses the alert context, resolves the entity, samples the alerting datapoint, checks collector health, and synthesizes a plain-language assessment with a resource-category-aware handoff recommendation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-logicmonitor-api-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 3
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# LogicMonitor API AI agent

This AI agent investigates alerts that originate with LogicMonitor, as well as operator-initiated entity checks. The agent parses the alert context, resolves the entity, samples the alerting datapoint, checks collector health, and synthesizes a plain-language assessment with a resource-category-aware handoff recommendation.

## Workflow

The agent investigates a LogicMonitor alert or a specific LogicMonitor-monitored entity to assess its health and recommend next steps.

1.  Resolve the entity referenced by the alert or request, and classify its resource category, such as Linux, Windows, network, voice, virtualization, or SAP HANA.
2.  Sample the alerting datapoint and check the health of the collector responsible for monitoring that entity.
3.  Verify whether the condition has already cleared and remained stable, or whether it appears to be a false positive.
4.  Surface related LogicMonitor alerts and recent ServiceNow change records for the entity.
5.  Associate the entity with its corresponding CMDB service for additional context.
6.  Synthesize a plain-language assessment of the entity's health, along with a recommended next step appropriate to its resource category.

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

LogicMonitor Connection Lookup

LogicMonitor Get Alert Details

LogicMonitor Get CMDB Service Association

LogicMonitor Get Collector Health

LogicMonitor Get Device Details

LogicMonitor Get Metric

LogicMonitor Get Process Detail

LogicMonitor Get Recent Changes for CI

LogicMonitor Get Related Entities

LogicMonitor List Alerts

LogicMonitor List DataSource Instances

LogicMonitor List Device DataSources

LogicMonitor List Devices

LogicMonitor List SDTs


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

evt\_mgmt\_operator

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

svc\_logicmonitor\_ai\_agent

 Contains: actsub\_user, agent\_admin, agent\_security\_admin, agent\_workspace\_user, api\_analytics\_read, app\_service\_user, canvas\_user, certification, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, connection\_admin, contact\_user, cors\_rule\_admin, credential\_admin, data\_interface\_steward, data\_manager\_user, decision\_table\_reader, dependency\_views, df\_data\_steward, email\_client\_template\_read, email\_composer, evt\_mgmt\_operator, evt\_mgmt\_user, export\_rest\_api, external\_app\_install\_admin, fd\_read, fd\_read\_actions, fd\_read\_flows, fd\_read\_operations, fd\_read\_operations\_all, flow\_designer, flow\_operator, flow\_write\_enabled, graphql\_schema\_admin, interaction\_agent, itil, knowledge, metadata\_scope\_viewer, notify\_view, now.assist.creator, now.assist.creator.analytics, now\_assist\_panel\_user, openapi\_admin, pa\_viewer, platform\_ml\_read, portfolio\_viewer, prompt\_library\_user, rest\_api\_builder, rest\_api\_explorer, sam\_core\_user, service\_status\_subscriber, service\_viewer, snc\_platform\_rest\_api\_access, sn\_ace.ace\_user, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_bm\_client.benchmark\_data\_viewer, sn\_change\_read, sn\_change\_write, sn\_cimaf.sn\_cimaf\_read, sn\_cmdb\_user, sn\_comm\_management.comm\_plan\_viewer, sn\_conv\_fa.conv\_fa\_designer, sn\_dex\_desktop.notification\_template\_admin, sn\_diagram\_builder.db\_read, sn\_gaf.data\_report\_viewer, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_gd\_guidance.guidance\_user, sn\_incident\_read, sn\_incident\_write, sn\_itam\_recomm.recommendations\_read, sn\_itsm\_aia.sn\_aia\_chg\_conflict, sn\_itsm\_aia.sn\_aia\_chg\_quality, sn\_itsm\_aia.sn\_aia\_chg\_schedule, sn\_itsm\_contact\_query, sn\_mcp\_client.viewer, sn\_na\_analytics.ai\_engmt\_viewer, sn\_na\_analytics.viewer, sn\_nb\_action.next\_best\_action\_user, sn\_now\_canvas\_ai.interactive\_view\_user, sn\_pren.experience\_issue\_read, sn\_problem\_read, sn\_problem\_write, sn\_publications\_recipients\_list\_user, sn\_publications\_recipients\_user, sn\_query\_gen.user, sn\_reacf.sn\_remedial\_action\_read, sn\_request\_approver\_read, sn\_request\_read, sn\_request\_write, sn\_sla\_definition\_query, sn\_sow.it\_agent\_dashboard\_user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sttrm\_condition\_read, sn\_udc.basic\_read, sn\_uib\_collab.user, sn\_uxc\_gen\_ai.sn\_aia\_sla\_explain, sn\_workflow\_studio.workflow\_studio\_read, survey\_reader, task\_editor, template\_editor, template\_read\_global, tracked\_file\_reader, trigger\_designer, trigger\_designer\_read, view\_changer, viz\_creator, wdf\_consumer, wdf\_operator, web\_service\_admin, workflow\_ai\_author, workspace\_user

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

Not applicable.

</td></tr></tbody>
</table>For more information, see [ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

