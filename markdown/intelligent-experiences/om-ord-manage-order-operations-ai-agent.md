---
title: Manage order operations AI agent
description: This AI agent helps customers change an order by requesting faster delivery, increasing quantities, changing the shipping address, or combining these changes. The agent checks inventory, delivery, and pricing, then resolves the case within a price threshold, creates a quote, or hands off to a specialist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-ord-manage-order-operations-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Order Management AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Manage order operations AI agent

This AI agent helps customers change an order by requesting faster delivery, increasing quantities, changing the shipping address, or combining these changes. The agent checks inventory, delivery, and pricing, then resolves the case within a price threshold, creates a quote, or hands off to a specialist.

## Workflow

The agent validates the order and the requested changes, checks whether the changes fit within the price threshold, and either resolves the case, creates a quote, or hands off to a specialist.

1.  The agent retrieves your order and confirms the order number.
2.  The agent identifies what you want to change and which order line the change applies to.
3.  The agent collects the details for each change: a new shipping address, an increased quantity, or a faster delivery date. You can combine these changes in one request.
4.  The agent confirms the changes with you and creates an order case.
5.  The agent validates inventory, delivery, and location feasibility for the requested changes, shows you the results, and asks you to accept or decline each result.
6.  If you accept all the changes, the agent checks the pricing. If the changes are within the standard pricing threshold, the agent resolves the case.
7.  If the changes exceed the threshold, the agent asks whether to create a quote. If you agree and then accept the quote, the agent resolves the case with the quote.
8.  If the changes can't be processed, or you decline the quote, the agent updates the case and offers to connect you with a live agent. The agent transfers you only after you confirm.
9.  The agent summarizes the outcome and shares the case details with you.

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

Check availability and earliest delivery

Check threshold for Quote Creation

Create order case

Get Customer Orders Tool

Get Order Line Items

Resolve Order Case and Quote

Update Case Lines with Exception Results

Validate Address

Validate Order Exception Change Request

-   **Subflows**

Create Quote

-   **Topic blocks**

Fetch the order number from the url &amp; interaction id


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_customerservice.customer

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

ord.exception.aia

 actsub\_user, agent\_schedule\_user, agent\_workspace\_user, app\_service\_user, assignment\_workbench, canvas\_user, chat\_admin, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, data\_manager\_user, decision\_table\_reader, dependency\_views, email\_client\_template\_read, email\_composer, fsm\_skill\_user, interaction\_agent, knowledge, notify\_view, now\_assist\_panel\_user, personalize\_form, platform\_ml\_read, prompt\_library\_user, skill\_user, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_bm\_client.benchmark\_data\_viewer, sn\_case\_line.characteristic\_creator, sn\_case\_line.characteristic\_delete, sn\_case\_line.characteristic\_viewer, sn\_case\_line.characteristic\_writer, sn\_change\_read, sn\_cmdb\_user, sn\_csm\_case\_types.service\_definition\_viewer, sn\_csm\_household.viewer, sn\_csm\_pricing.pricelist\_viewer, sn\_customerservice.csm\_workspace\_user, sn\_customerservice.customer\_data\_viewer, sn\_customerservice\_agent, sn\_esm\_agent, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_gd\_guidance.guidance\_user, sn\_ind\_tmt\_orm.fulfillment\_viewer, sn\_ind\_tmt\_orm.order\_viewer, sn\_l2c\_core.entity\_mapping\_viewer, sn\_lookup\_verify\_user, sn\_nb\_action.next\_best\_action\_user, sn\_order\_case.agent, sn\_order\_case.creator, sn\_order\_case.navigation\_menu, sn\_order\_case.viewer, sn\_order\_case.writer, sn\_ord\_qual\_mgmt.alternate\_proposal\_read, sn\_prd\_invt.product\_inventory\_operations\_read, sn\_prd\_invt.product\_inventory\_viewer, sn\_prd\_pm.characteristics\_viewer, sn\_prd\_pm.product\_catalog\_viewer, sn\_prd\_pm.product\_model\_characteristic\_viewer, sn\_pss\_core.service\_contract\_viewer, sn\_query\_gen.user, sn\_quote\_mgmt\_core.quote\_writer, sn\_req\_criteria.viewer, sn\_service\_org.customer\_criteria\_read, sn\_service\_org.service\_criteria\_read, sn\_shn.editor, sn\_shn.user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_sttrm\_condition\_read, sn\_templated\_snip.template\_snippet\_reader, sn\_tmt\_core.inbound\_queue\_read, sn\_udc.basic\_read, sn\_uib\_collab.user, sn\_workflow\_studio.workflow\_studio\_read, survey\_reader, task\_editor, template\_editor, template\_read\_global, view\_changer, workspace\_user

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

Not applicable.

</td></tr></tbody>
</table>Learn more about customer self-service via Business Portal at [Customer self-service for Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-self-service-business-portal.md).

**Parent Topic:**[Order Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/om-ai-agents-overview.md)

