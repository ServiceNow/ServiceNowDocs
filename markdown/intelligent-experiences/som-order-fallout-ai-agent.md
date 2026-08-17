---
title: Order fallout AI Agent
description: This Sales Customer Relationship Management agent analyzes order task comments and work notes to detect issues matching known fallout types, creates fallout records for any matches, and summarizes the results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/som-order-fallout-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales Automation, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Order fallout AI Agent

This Sales Customer Relationship Management agent analyzes order task comments and work notes to detect issues matching known fallout types, creates fallout records for any matches, and summarizes the results.

## Workflow

1.  Fetch the task details for the given order task number.
2.  Get the list of recognized fallout types from the system.
3.  Compare the work notes against available fallout types and create any matching fallouts that are identified.
4.  Display a summary of all steps taken, including any created fallout numbers, or note that none were found.

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

Create validated and confirmed fallouts

Find all available fallout types

Find all notes for order task


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent

</td></tr><tr><td>

Data access roles

</td><td>

actsub\_user, agent\_schedule\_user, agent\_workspace\_user, app\_service\_user, assignment\_workbench, awa\_agent, baseline\_user, canvas\_user, chat\_admin, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, data\_manager\_user, decision\_table\_reader, demand\_user, dependency\_views, document\_management\_user, email\_client\_template\_read, email\_composer, fsm\_skill\_user, interaction\_agent, inventory\_user, it\_demand\_user, it\_project\_portfolio\_user, it\_project\_user, knowledge, notify\_view, now\_assist\_panel\_user, personalize\_form, planning\_console\_user, platform\_ml\_di.creation\_agent, platform\_ml\_read, pps\_resource, project\_portfolio\_user, project\_user, prompt\_library\_user, quickactions\_user, service\_fulfiller, skill\_user, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_apptmnt\_booking.appointment\_booking\_user, sn\_bm\_client.benchmark\_data\_viewer, sn\_change\_read, sn\_cmdb\_user, sn\_csm\_case\_types.service\_definition\_viewer, sn\_csm\_household.viewer, sn\_csm\_pricing.pricelist\_viewer, sn\_customerservice.case\_viewer, sn\_customerservice.consumer\_agent, sn\_customerservice.csm\_workspace\_user, sn\_customerservice.customer\_data\_viewer, sn\_customerservice\_agent, sn\_esm\_agent, sn\_fallout\_mgmt.fallout\_agent, sn\_fallout\_mgmt.fallout\_creator, sn\_fallout\_mgmt.fallout\_viewer, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_gd\_guidance.guidance\_user, sn\_gf.goal\_user, sn\_gf.goal\_user\_read, sn\_gf.strategy\_planner, sn\_gf.strategy\_planner\_read, sn\_ind\_tmt\_orm.fulfillment\_viewer, sn\_ind\_tmt\_orm.fulfillment\_viewer, sn\_ind\_tmt\_orm.fulfillment\_writer, sn\_ind\_tmt\_orm.order\_creator, sn\_ind\_tmt\_orm.order\_fulfilment\_agent, sn\_ind\_tmt\_orm.order\_fulfilment\_agent, sn\_ind\_tmt\_orm.order\_viewer, sn\_itam\_recomm.recommendations\_read, sn\_l2c\_core.entity\_mapping\_viewer, sn\_lookup\_verify\_user, sn\_nb\_action.next\_best\_action\_user, sn\_ord\_qual\_mgmt.alternate\_proposal\_create, sn\_ord\_qual\_mgmt.alternate\_proposal\_read, sn\_ord\_qual\_mgmt.alternate\_proposal\_write, sn\_prd\_invt.product\_inventory\_operations\_read, sn\_prd\_invt.product\_inventory\_relationship\_create, sn\_prd\_invt.product\_inventory\_relationship\_read, sn\_prd\_invt.product\_inventory\_relationship\_write, sn\_prd\_invt.product\_inventory\_viewer, sn\_prd\_pm.characteristics\_viewer, sn\_prd\_pm.product\_catalog\_viewer, sn\_prd\_pm.product\_model\_characteristic\_viewer, sn\_pss\_core.service\_contract\_viewer, sn\_query\_gen.user, sn\_req\_criteria.viewer, sn\_service\_org.customer\_criteria\_read, sn\_service\_org.service\_criteria\_read, sn\_shn.editor, sn\_shn.user, sn\_sla\_definition\_read, sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sttrm\_condition\_read, sn\_templated\_snip.template\_snippet\_reader, sn\_tmt\_core.inbound\_queue\_read, sn\_tmt\_core.outbound\_request\_read, sn\_tmt\_core.outbound\_request\_write, sn\_udc.basic\_read, sn\_uib\_collab.user, sn\_uxc\_gen\_ai.platform\_ai\_image\_processor, sn\_uxc\_gen\_ai.platform\_ai\_record\_mgmt, sn\_workflow\_studio.workflow\_studio\_read, survey\_reader, task\_activity\_reader, task\_activity\_writer, task\_editor, template\_editor, template\_read\_global, territory\_user, timecard\_user, view\_changer, wm\_basic, wm\_read, workspace\_user

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
</table>Learn more about Sales Customer Relationship Management at [Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-overview.md).

**Parent Topic:**[Sales Automation AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sales-automation-ai-agents-overview.md)

