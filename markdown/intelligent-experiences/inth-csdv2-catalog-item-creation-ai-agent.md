---
title: Catalog item creation AI agent
description: This AI agent creates service catalog items for applications from Microsoft Intune, Jamf, and Microsoft Endpoint Configuration Manager. It configures the software model, identifies or creates the target groups or collections, and creates the software configuration and catalog item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-csdv2-catalog-item-creation-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 3
breadcrumb: [Client Software Distribution 2.0 AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Catalog item creation AI agent

This AI agent creates service catalog items for applications from Microsoft Intune, Jamf, and Microsoft Endpoint Configuration Manager. It configures the software model, identifies or creates the target groups or collections, and creates the software configuration and catalog item.

## Workflow

The agent helps the user create a service catalog item for an application that is managed in Microsoft Intune, Jamf, or Microsoft Endpoint Configuration Manager.

1.  Ask the user for the application name if they haven't provided it.
2.  Look up the application and, if several match, show them grouped by provider and server and ask the user to choose one.
3.  Identify the software model type and configure a Client Software Distribution software model, or ask the user to choose a Software Asset Management software model.
4.  Find the install and, where applicable, uninstall groups or collections for the application's provider, and ask the user to choose one when several are found.
5.  Offer to create a group or collection when none exists, collecting the required details such as type, limiting collection, deploy purpose, and enforcement deadline.
6.  For Microsoft Intune applications, ask whether the deployment is user-based or device-based.
7.  Create the software configuration and the catalog item, and report the catalog item's sys\_id to the user.

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

-   **Flow Actions**

Create Jamf Catalog item

Create Microsoft Endpoint Configuration Manager Catalog Item

Create Microsoft Intune Catalog item

Look up Jamf Target groups

-   **Scripts**

Identify Software model

Look up Computer Target group by Name

Look up Mobile Target Group by Name

Look up User Target Group by Name

-   **Subflows**

Configure CSD Software model

Configure Jamf Target group

Configure Microsoft Endpoint Configuration Manager Collection

Configure Microsoft Intune group

Configure SAM Software model

Create Jamf Software configuration

Create Microsoft Endpoint Configuration Manager Software Configuration

Create Microsoft Intune Software configuration

Look up Applications

Look up Microsoft Endpoint Configuration Manager Collection

Look up Microsoft Intune groups

Look up SAM Software models


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_csd.CSD Admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_csd.CSD Admin

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
</table>**Parent Topic:**[Client Software Distribution 2.0 AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-csdv2-ai-agents-overview.md)

**Related topics**  


[Client Software Distribution 2.0 application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/csd-app-2.md)

[Integration Hub solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/solutions.md)

