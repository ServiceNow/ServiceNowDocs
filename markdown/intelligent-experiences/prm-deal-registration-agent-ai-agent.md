---
title: Deal Registration AI agent
description: Manages the end-to-end deal registration workflow. Creates, updates, and submits deal registrations for channel partners; resolves customer and product information; and handles product line item management including additions and removals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/prm-deal-registration-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 3
breadcrumb: [PRM AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Deal Registration AI agent

Manages the end-to-end deal registration workflow. Creates, updates, and submits deal registrations for channel partners; resolves customer and product information; and handles product line item management including additions and removals.

## Workflow

The Deal Registration Agent assists users in creating, modifying, and submitting deal registrations for partner and enterprise channels. It guides users through customer resolution, product selection, field updates, and submission, while ensuring all mandatory information is captured and validated.

The agent enforces authorization through internal role checks \(Partner Staff or Enterprise Staff\). It validates user access against the deal registration categories users can create: Account, Consumer, or both.

1.  Verify your user type and access permissions to determine which deal categories you can create.
2.  Provide mandatory information: channel partner details and either Account or Consumer information.
3.  Resolve customer information by name; select from matches or add as a new customer.
4.  Optionally update deal registration fields such as deal type, partner program, or estimated close date.
5.  Add products to the deal registration by resolving product names against the catalog.
6.  Confirm and review the complete deal registration details.
7.  Submit the deal registration for processing.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Conversational Topics**

Create Deal Registration

Create Deal registration line item

Delete Deal registration line item

Get Deal registration details

Look up Deal Registration Line item

Resolve Customer information

Resolve Product offerings

Update Deal registration fields

Update work notes

-   **Flow Actions and Subflows**

Fetch User type and Access

Submit Deal registration

Validate Channel Partner information

Validate Program and Deal registration type


</td></tr><tr><td>

Allowed user roles

</td><td>

Multiple internal and external roles can access this agent. For the full list of roles and access points, see the Roles that can access Deal Registration AI agent section.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

-   Deal Registration Workflow
-   Default VA Workflow

</td></tr></tbody>
</table>## Roles that can access Deal Registration AI agent

The following roles can access the Deal Registration AI agent:

|Role|User type|Access point|
|----|---------|------------|
|Enterprise Deal Registration Relationship Manager|Internal|Now Assist Panel|
|Enterprise Deal Registration Relationship Contributor|Internal|Platform workspace|
|Enterprise B2B Deal Registration Agent|Internal|Platform workspace|
|Enterprise B2C Deal Registration Agent|Internal|Platform workspace|
|Enterprise Deal Registration Agent|Internal|Platform workspace|
|Partner B2B Deal Registration Initiator|External|Partner portal|
|Partner B2C Deal Registration Initiator|External|Partner portal|
|Partner B2B Sales Representative|External|Partner portal|
|Partner B2C Sales Representative|External|Partner portal|

**Parent Topic:**[PRM AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/prm-ai-agents.md)

