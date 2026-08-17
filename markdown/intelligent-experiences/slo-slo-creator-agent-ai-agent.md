---
title: SLO Creator AI agent
description: This Supplier Lifecycle Operations agent analyzes a configuration item's reliability history \(alerts and outages\), identifies recurring issue patterns per CI. It then creates an SLO with targeted SLI filters to track each pattern.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/slo-slo-creator-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 3
breadcrumb: [Supplier Lifecycle Operations AI agents, Supplier Lifecycle Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# SLO Creator AI agent

This Supplier Lifecycle Operations agent analyzes a configuration item's reliability history \(alerts and outages\), identifies recurring issue patterns per CI. It then creates an SLO with targeted SLI filters to track each pattern.

## Workflow

1.  Fetch the configuration item's details \(including related child CIs\), then calculate risk scores, critical alert counts, outage counts, and incident counts across multiple compliance periods.
2.  Based on the risk analysis and business criticality, select the optimal compliance period, data source \(alerts or outages\), and goal targets.
3.  Retrieve alerts or outages associated with the CI and its related CIs, then classify events into SLI types \(Availability, Latency, Saturation, Errors\) using keyword matching.
4.  Select the SLO measurement approach \(Duration, Count by periods, or Count by occurrences\) and confirm the SLI type based on the source data analysis.
5.  Analyze events separately for each CI \(main and related\) to find recurring issue patterns. For each CI, select the most impactful pattern and build a validated encoded query filter to capture it. If no data or patterns exist, create a default SLI with an empty filter.
6.  Document all decisions in a structured format covering data analysis, metrics, SLO configuration choices, and SLI justifications.
7.  Submit all collected inputs \(CI details, SLO metadata, SLI filters, reasoning summary\) to create the SLO and its associated SLIs.

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

-   **Record Operation**

Alerts associated with configuration item

Outages associated with configuration item

-   **Scripts**

CI details

CI risk score

Create SLO and SLI

SLO metadata


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_sow\_slo.slo\_operator

</td></tr><tr><td>

Data access roles

</td><td>

access\_analyzer\_ai\_user, actsub\_user, agent\_role\_config\_viewer, agent\_workspace\_user, app\_service\_user, canvas\_user, certification, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, contact\_user, data\_manager\_user, dependency\_views, email\_client\_template\_read, email\_composer, evt\_mgmt\_user, interaction\_agent, itil, knowledge, notify\_view, now\_assist\_panel\_user, one\_extend\_viewer, pa\_viewer, platform\_ml\_read, portfolio\_viewer, prompt\_library\_user, role\_viewer, sam\_core\_user, service\_status\_subscriber, service\_viewer, snc\_internal, snc\_platform\_rest\_api\_access, snc\_required\_script\_writer\_permission, sn\_ace.ace\_user, sn\_aia.viewer, sn\_ai\_agents\_slo.creator\_agent\_executor, sn\_ai\_agents\_slo.creator\_agent\_queue\_processor, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_bm\_client.benchmark\_data\_viewer, sn\_change\_read, sn\_change\_write, sn\_cimaf.sn\_cimaf\_read, sn\_cmdb\_user, sn\_comm\_management.comm\_plan\_viewer, sn\_data\_kit.analyst, sn\_dex\_desktop.notification\_template\_admin, sn\_diagram\_builder.db\_read, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_gd\_guidance.guidance\_user, sn\_incident\_read, sn\_incident\_write, sn\_itam\_recomm.recommendations\_read, sn\_itsm\_aia.sn\_aia\_chg\_conflict, sn\_itsm\_aia.sn\_aia\_chg\_quality, sn\_itsm\_aia.sn\_aia\_chg\_schedule, sn\_itsm\_contact\_query, sn\_mcp\_client.viewer, sn\_nb\_action.next\_best\_action\_user, sn\_nowassist\_admin.user, sn\_now\_canvas\_ai.interactive\_view\_user, sn\_pren.experience\_issue\_read, sn\_problem\_read, sn\_problem\_write, sn\_prompt\_assist.prompt\_developer, sn\_publications\_recipients\_list\_user, sn\_publications\_recipients\_user, sn\_query\_gen.user, sn\_reacf.sn\_remedial\_action\_read, sn\_request\_approver\_read, sn\_request\_read, sn\_request\_write, sn\_skill\_builder.viewer, sn\_sla\_definition\_query, sn\_sow.it\_agent\_dashboard\_user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sow\_slo.create, sn\_sow\_slo.read, sn\_sow\_slo.write, sn\_sow\_srm\_common.create, sn\_sow\_srm\_common.delete, sn\_sow\_srm\_common.read, sn\_sow\_srm\_common.write, sn\_sttrm\_condition\_read, sn\_uib\_collab.user, sn\_uxc\_gen\_ai.sn\_aia\_sla\_explain, survey\_reader, task\_editor, template\_editor, template\_read\_global, tracked\_file\_reader, view\_changer, viz\_creator, workspace\_user

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
</table>Learn more about Supplier Lifecycle Operations at [Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supp-mgmt-landing-page.md).

**Parent Topic:**[Supplier Lifecycle Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/slo-ai-agents-overview.md)

