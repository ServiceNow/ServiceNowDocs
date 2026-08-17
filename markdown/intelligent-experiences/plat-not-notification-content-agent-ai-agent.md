---
title: Notification content AI agent
description: This AI agent prepares email notification templates and layouts. It begins by analyzing user input to understand the notification's content requirements and design expectations. Before generating any content, the agent searches for similar existing templates and presents the results to the user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-not-notification-content-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 3
breadcrumb: [Notifications AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Notification content AI agent

This AI agent prepares email notification templates and layouts. It begins by analyzing user input to understand the notification's content requirements and design expectations. Before generating any content, the agent searches for similar existing templates and presents the results to the user.

## Workflow

The agent is strictly scoped to email notification template and layout creation only.

1.  Perform content preparation and request analysis to build a clear understanding of the notification content to be created.
2.  Find a default template.
3.  Extract template and layout requirements
4.  Select the email sections that are required for the user's request.
5.  Select interaction elements that are required for the user's request.
6.  Determine whether the email should be div-based, table-based, or a hybrid.
7.  Select a design style.
8.  Determine content and tone.
9.  Determine layout requirements.
10. Identify all dynamic fields required for the template which are explicitly mentioned in content requirements or the user's request.
11. Summarize results and confirm with the user.
12. Generate the template and layout.

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

Fetch Resolved Template HTML

Get Most Used Email Layout

Mail Script Resolver

Render canvas content

Save Layout

Save Template

Template fetcher


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

admin, notification\_admin

</td></tr><tr><td>

Data access roles

</td><td>

notification\_generator\_ai\_useraccess\_analyzer\_ai\_user, actsub\_user, agent\_role\_config\_viewer, agent\_schedule\_user, agent\_workspace\_user, approver\_user, app\_service\_user, assignment\_workbench, awa\_agent, awa\_integration\_user, canvas\_user, chat\_admin, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, contact\_user, data\_manager\_user, decision\_table\_reader, dependency\_views, doc\_page\_number\_config\_writer, doc\_toc\_config\_writer, email\_client\_template\_read, email\_composer, fd\_read\_operations, flow\_operator, fsm\_skill\_user, interaction\_agent, knowledge, localization\_editor, localization\_requestor, notify\_view, now\_assist\_panel\_user, one\_extend\_viewer, pa\_viewer, personalize\_form, personalize\_responses, platform\_ml\_di.creation\_agent, platform\_ml\_di.extraction\_agent, platform\_ml\_read, prompt\_library\_user, quickactions\_user, report\_user, role\_viewer, skill\_user, sla\_admin, sla\_manager, sn\_ace.ace\_user, sn\_aia.viewer, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_ap\_apm.reader, sn\_ap\_cm.admin, sn\_ap\_cm.agent, sn\_ap\_cm.agent, sn\_ap\_cm.requester, sn\_ap\_cm.requester, sn\_ap\_cm.task\_owner, sn\_ap\_gen\_ai.now\_assist\_fulfiller, sn\_bm\_client.benchmark\_data\_viewer, sn\_change\_read, sn\_cmdb\_user, sn\_comm\_management.comm\_plan\_viewer, sn\_compliance.reader, sn\_csm\_case\_types.service\_definition\_viewer, sn\_csm\_household.viewer, sn\_csm\_pricing.pricelist\_viewer, sn\_customerservice.consumer\_agent, sn\_customerservice.csm\_workspace\_user, sn\_customerservice.customer\_data\_viewer, sn\_customerservice\_agent, sn\_data\_kit.analyst, sn\_data\_registry.reader, sn\_dex\_desktop.notification\_template\_admin, sn\_diagram\_builder.db\_read sn\_doc.reader, sn\_doc.writer sn\_docintel.extraction\_agent, sn\_esm\_agent sn\_fin.finance\_user, sn\_fin.procurement\_user, sn\_fsc\_genai.now\_assist\_fulfiller sn\_gaf.data\_viewer, sn\_gaf.data\_writer sn\_gd\_guidance.guidance\_user, sn\_grc.business\_user sn\_grc.reader, sn\_grc.user\_hierarchy\_reader, sn\_grc\_taxonomy.taxonomy\_user, sn\_grc\_workspace.task\_reader sn\_grc\_workspace.user, sn\_incident\_read sn\_ind\_tmt\_orm.fulfillment\_viewer, sn\_ind\_tmt\_orm.order\_viewer, sn\_l2c\_core.entity\_mapping\_viewer, sn\_lg\_cf\_workspace.legal\_workspace\_user, sn\_lg\_gen\_ai.legal\_user sn\_lg\_gen\_ai.request\_fulfiller, sn\_lg\_ops.legal\_report\_viewer, sn\_lg\_ops.legal\_sla\_read, sn\_lg\_ops.legal\_user, sn\_lg\_ops.request\_fulfiller, sn\_lookup\_verify\_user sn\_mcp\_client.viewer, sn\_nb\_action.next\_best\_action\_user, sn\_notif\_agents.notification\_generator, sn\_nowassist\_admin.user, sn\_ord\_qual\_mgmt.alternate\_proposal\_read, sn\_prd\_invt.product\_inventory\_operations\_read, sn\_prd\_invt.product\_inventory\_viewer, sn\_prd\_pm.characteristics\_viewer, sn\_prd\_pm.product\_catalog\_viewer, sn\_prd\_pm.product\_model\_characteristic\_viewer, sn\_pren.experience\_issue\_read, sn\_prompt\_assist.prompt\_developer, sn\_pss\_core.service\_contract\_viewer, sn\_publications\_recipients\_list\_user, sn\_publications\_recipients\_user sn\_query\_gen.user, sn\_query\_gen.user, sn\_request\_read, sn\_req\_criteria.viewer, sn\_service\_org.customer\_criteria\_read, sn\_service\_org.service\_criteria\_read sn\_shn.editor, sn\_shn.user, sn\_shop.invoice\_owner, sn\_shop.procurement\_common\_reader, sn\_shop.shopper, sn\_skill\_builder.viewer, sn\_sla\_definition\_query sn\_slm.fulfiller, sn\_smart\_asmt.actor, sn\_smart\_asmt.assessment\_reader, sn\_smart\_asmt.template\_reader, sn\_sow.it\_agent\_dashboard\_user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sttrm\_condition\_read, sn\_supplier\_gen\_ai.now\_assist\_fulfiller, sn\_templated\_snip.template\_snippet\_reader, sn\_tmt\_core.inbound\_queue\_read, sn\_tprm\_genai.nowassist\_user sn\_udc.basic\_read, sn\_uib\_collab.user, sn\_uni\_req.universal\_request\_read, sn\_uxc\_gen\_ai.platform\_ai\_field\_predictor, sn\_uxc\_gen\_ai.platform\_ai\_image\_processor, sn\_uxc\_gen\_ai.platform\_ai\_record\_mgmt, sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer, sn\_workflow\_studio.workflow\_studio\_read,sn\_wsd\_core.workplace\_user, survey\_reader task\_editor, template\_editor, template\_editor\_global, template\_read\_global, vendor\_reader, view\_changer, viz\_creator workspace\_user

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

Default VA Workflow

</td></tr></tbody>
</table>Learn more about Notifications in [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notifications.md).

**Parent Topic:**[Notifications AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-notifications-ai-agents-overview.md)

