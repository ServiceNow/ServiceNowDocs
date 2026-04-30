---
title: Using the HR Service Delivery Agent Workspace
description: As an HR agent, use HR Service Delivery Agent Workspace or the Agent Workspace for HR Case Management to interact with employees, respond to inquiries, and resolve issues.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Using the HR Service Delivery Agent Workspace

As an HR agent, use HR Service Delivery Agent Workspace or the Agent Workspace for HR Case Management to interact with employees, respond to inquiries, and resolve issues.

**Important:**

-   HR Service Delivery Agent Workspace \(Classic\) is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.
-   If you are an existing user of HR Service Delivery Agent Workspace \(Classic\), you can migrate to the Agent Workspace for HR Case Management \(Configurable\) for enhanced features and capabilities. See [Migration Guidelines](https://www.servicenow.com/community/hrsd-articles/hr-agent-workspace-migration-guidelines-from-classic-to/ta-p/2310606).

**Note:** The COEs available to you may differ depending on the HR package you have.

-   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
-   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](hr-catalog-item-configuration.md). Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
-   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](../task/configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
-   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.

You can start work in HR Service Delivery Agent Workspace or the Agent Workspace for HR Case Management from one of these areas:

-   Landing page
-   List queue
-   Agent inbox
-   Chat
-   Phone
-   Global search

For additional information on working within Agent Workspace, see [Using workspace](https://www.servicenow.com/docs/access?context=using-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Along the left side and top of the Home page are a series of icons you can select.

<table id="table_wff_rcx_gjb"><thead><tr><th>

Agent Workspace feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![HR Agent WS - Home icon](../image/agent-ws-hr-home-icon.png)Home

</td><td>

Select to take you back to the Home page.

</td></tr><tr><td>

![List icon](../image/agent-ws-hr-list-icon.png) HR case list

</td><td>

Select to view a list of HR cases, interactions, HR tasks, and more. You can access the list icon from any screen.

</td></tr><tr><td>

![Inbox icon](../image/agent-ws-hr-inbox-icon.png)Inbox

</td><td>

Shows any work items assigned to you.You can also indicate if you are:

-   Available
-   Offline
-   Away

 you are available**Note:** Requires activation of the Advanced Work Assignment \(com.glide.awa\) and Agent Chat \(com.glide.interaction.awa\) plugins.

</td></tr><tr><td>

![Add New](../image/agent-ws-hr-add-icon.png) Add New

</td><td>

Select to create one of the following:-   Interaction
-   HR case

 **Note:** Found at the top, left side of the Home screen.

</td></tr></tbody>
</table>## Create a new case

From the HR Agent Workspace home page, select the ![create case icon](../image/IconCreateRecordMenu.png) create case icon.

## New case or interaction

You can create a new HR case or an interaction. An interaction is when an employee contacts an HR agent and you want to ensure the interaction is documented and captured.

## Searching for an existing case or employee or skip

You can search for an existing case or create a case from any screen. Select the ![create case icon](../image/IconCreateRecordMenu.png) create case icon.

Searching for an employee also helps to verify that you are creating a case for the correct person.

If your company uses **Employee Relations**, you can select the **Skip verification** link to create an ER case without identifying an Opened for person. For more information on Employee Relations, see [Create an HR Service Delivery Employee Relations case using the legacy UI](../task/create-hr-employee-relations.md).

<table id="table_gft_knx_gjb"><thead><tr><th>

Agent Workspace feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search field

</td><td>

Field where you enter a name, partial name, or case number.**Note:** Unlike the platform web-based UI, you can't search for or create cases for inactive users.

</td></tr></tbody>
</table>## Starting from the List queue

You can select a case or an interaction from the ![List icon](../image/agent-ws-hr-list-icon.png) list icon.

For additional information, see Setting up list view in a workspace.

## Working from the agent inbox

You can also start work by going to the ![HR Agent Workspace Agent inbox icon](../image/agent-ws-hr-inbox-icon.png) agent inbox, which is on the left side of the navigation bar.

<table id="table_t44_dfd_hjb"><thead><tr><th>

Agent Responsibilities

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select an HR case from agent inbox.

</td><td>

Inbox that contains the HR cases that are assigned to you.Chats and interactions also appear in agent inbox. For more information on using chat, see [Using chat in HR Service Delivery Agent Workspace](agent-ws-hr-chat.md#).

</td></tr></tbody>
</table>For additional information, see [Working from the agent inbox](https://www.servicenow.com/docs/access?context=live-agent-overview&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

