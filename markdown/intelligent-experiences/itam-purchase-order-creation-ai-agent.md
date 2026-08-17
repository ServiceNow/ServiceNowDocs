---
title: Purchase order creation AI agent
description: This AI agent is used to create a purchase order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itam-purchase-order-creation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Asset Management AI agents, IT Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Purchase order creation AI agent

This AI agent is used to create a purchase order.

## Workflow

1.  Use the Get Destination Stockrooms for requested item tool to retrieve a list of destination stockrooms.
2.  Ask the user to select a stockroom if multiple choices are available. If none are available, end the workflow.
3.  Use the Get Vendors for requested item tool to retrieve a list of vendors.
4.  Ask the user to select a vendor if multiple choices are available. If none are available, end the workflow.
5.  If the requested item is software, use the Get Metric Group and License Metric conversational topic tool to help user get a license.
6.  If the requested item is not software, use Create purchase order for requested item tool to create a purchase order for the specified stockroom and vendor.
7.  Display purchase order to the user.

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

Create purchase order for requested item

Generate guided purchase order plan and create PO

Get Destination Stockrooms for requested item

Get Vendors for requested item

Purchase Order Auto-Completion

-   **Conversational Topic**

Get metric group and license metric


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

procurement\_user

</td></tr><tr><td>

Data access roles

</td><td>

procurement\_user, itil, sn\_request\_write

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

-   Help manage enterprise asset requests
-   Help manage hardware asset requests
-   Help manage software requests

</td></tr></tbody>
</table>Learn more about IT Asset Management at .

**Parent Topic:**[IT Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itam-ai-agents-overview.md)

