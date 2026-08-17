---
title: Invoice dispute intake assistant AI agent
description: This AI agent helps requesters identify the correct invoice, confirm dispute details, and submit invoice disputes related to quantity issues. It guides users step by step through invoice identification, validation, and dispute submission to ensure a smooth and accurate experience. The agent also analyzes the sentiment of the user throughout the conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-inv-invoice-dispute-intake-assistant-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Order Management AI agents, Order Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Invoice dispute intake assistant AI agent

This AI agent helps requesters identify the correct invoice, confirm dispute details, and submit invoice disputes related to quantity issues. It guides users step by step through invoice identification, validation, and dispute submission to ensure a smooth and accurate experience. The agent also analyzes the sentiment of the user throughout the conversation.

## Workflow

By interpreting emotional cues related to invoice or order issues, the agent classifies sentiment as Positive, Neutral, or Negative, and uses this insight to adjust response tone and offer escalation to a live agent when appropriate. This agent can resolve quantity-related invoice disputes only.

1.  If the user requests help beyond the agent’s capabilities or encounters repeated issues, always offer live agent support as option.
2.  Check the current page URL first to determine whether an invoice number is available. If not, look up associated invoices for the user and clarify with the user which invoice is being disputed.
3.  Validate the invoice and determine which line of the invoice is in dispute.
4.  Identify the issue and capture disputed details.
5.  Create an invoice case.
6.  Off resolution options to the user.
7.  If the user chooses a resolution option, resolve the invoice case.

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

Create invoice case

Get invoice details

Resolve invoice dispute

Validate and confirm invoice dispute

Validate Invoice Line

-   **Conversational topics**

Fetch the invoice number from the url and interaction id


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_customerservice.customer, sn\_csm\_invoice.agent, sn\_otc.account\_receivable\_agent

</td></tr><tr><td>

Data access roles

</td><td>

invoice.exception.aia

 actsub\_user, agent\_schedule\_user, agent\_workspace\_user, app\_service\_user, assignment\_workbench, canvas\_user, chat\_admin, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, data\_manager\_user, decision\_table\_reader, dependency\_views, email\_client\_template\_read, email\_composer, fsm\_skill\_user, interaction\_agent, knowledge, notify\_view, now\_assist\_panel\_user, personalize\_form, platform\_ml\_read, prompt\_library\_user, skill\_user, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_bm\_client.benchmark\_data\_viewer, sn\_case\_line.characteristic\_creator, sn\_case\_line.characteristic\_delete, sn\_case\_line.characteristic\_viewer, sn\_case\_line.characteristic\_writer, sn\_change\_read, sn\_cmdb\_user, sn\_csm\_case\_types.service\_definition\_viewer, sn\_csm\_household.viewer, sn\_csm\_invoice.agent, sn\_csm\_invoice.creator, sn\_csm\_invoice.navigation\_menu, sn\_csm\_invoice.viewer, sn\_csm\_invoice.writer, sn\_csm\_pricing.pricelist\_viewer, sn\_customerservice.csm\_workspace\_user, sn\_customerservice.customer\_data\_viewer, sn\_customerservice\_agent, sn\_esm\_agent, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_gd\_guidance.guidance\_user, sn\_ind\_tmt\_orm.fulfillment\_viewer, sn\_ind\_tmt\_orm.order\_viewer, sn\_l2c\_core.entity\_mapping\_viewer, sn\_lookup\_verify\_user, sn\_nb\_action.next\_best\_action\_user, sn\_ord\_qual\_mgmt.alternate\_proposal\_read, sn\_otc.ar\_invoice\_viewer, sn\_prd\_invt.product\_inventory\_operations\_read, sn\_prd\_invt.product\_inventory\_viewer, sn\_prd\_pm.characteristics\_viewer, sn\_prd\_pm.product\_catalog\_viewer, sn\_prd\_pm.product\_model\_characteristic\_viewer, sn\_pss\_core.service\_contract\_viewer, sn\_query\_gen.user, sn\_req\_criteria.viewer, sn\_service\_org.customer\_criteria\_read, sn\_service\_org.service\_criteria\_read, sn\_shn.editor, sn\_shn.user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sttrm\_condition\_read, sn\_templated\_snip.template\_snippet\_reader, sn\_tmt\_core.inbound\_queue\_read, sn\_udc.basic\_read, sn\_uib\_collab.user, sn\_workflow\_studio.workflow\_studio\_read, survey\_reader, task\_editor, template\_editor, template\_read\_global, view\_changer, workspace\_user

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
</table>Learn more about Order Management at [Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md).

**Parent Topic:**[Order Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/om-ai-agents-overview.md)

