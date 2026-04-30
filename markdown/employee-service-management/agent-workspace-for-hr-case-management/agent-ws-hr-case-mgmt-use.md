---
title: Using Agent Workspace for HR Case Management
description: As an HR agent, use the Agent Workspace for HR Case Management to interact with employees, respond to inquiries, and resolve issues.
locale: en-US
release: yokohama
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Using Agent Workspace for HR Case Management

As an HR agent, use the Agent Workspace for HR Case Management to interact with employees, respond to inquiries, and resolve issues.

**Note:** The COEs available to you may differ depending on the HR package you have.

-   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
-   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](hr-catalog-item-configuration.md). Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
-   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](../task/configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
-   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.

You can start work in the Agent Workspace for HR Case Management from one of these areas:

-   Landing page
-   List queue
-   Agent inbox
-   Chat
-   Phone
-   Global search

For additional information on working within Agent Workspace, see [Using workspace](https://www.servicenow.com/docs/access?context=using-workspace&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

HR case form enables you to manage multiple cases, view information that is related to a case, and use knowledge articles or similar cases to manage the case.

![Agent Workspace for HR Case Management - Case form](../image/agent-ws-hr-case-mgmt-explore.png)

<table id="table_obz_g2x_gjb"><thead><tr><th>

Number

</th><th>

Agent Workspace feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![HR Agent Workspace case form callout 1](../reference/images/1.png)

</td><td>

Tabs

</td><td>

Use tabs to display the records that are associated with an HR case, like case details and tasks. You can select a tab and jump to the information. Child tabs appear below the top tabs and display case details, HR profile information, and tasks.**Note:** Any reference that you select under a parent tab opens as a child tab.

</td></tr><tr><td>

![HR Agent Workspace case form callout 2](../reference/images/2.png)

</td><td>

Form header

</td><td>

Displays brief details of an HR case like HR service, priority, state, and assigned-to agent.

</td></tr><tr><td>

![HR Agent Workspace case form callout 3](../image/3.png)

</td><td>

UI actions

</td><td>

Action button that enables you to save changes you made, change the status, cancel, or other relevant actions for a case.**Note:** The buttons that appear are similar to the native platform UI.

The button types that appear depends on the type and status of the HR case.

</td></tr><tr><td>

![HR Agent Workspace case form callout 4](../image/4.png)

</td><td>

Related items

</td><td>

Use the Related Items menu to see information about the details, tasks, and other information that is associated with a case. Also shows details of the records from other tables that have a relationship with the HR case. This menu provides a quick and easy way to look up information about a case and subject person.**Note:** The type of HR case determines the tabs that appear in this menu. When a case appears under Playbook, these tabs change. For more information, see [Exploring HR Service Delivery Playbook](playbook-hr-explore.md).

</td></tr><tr><td>

![HR Agent Workspace case form callout 5](../image/5.png)

</td><td>

Case details

</td><td>

Information about the case:-   Subject person
-   HR service requested
-   Priority assigned
-   Assignment group
-   Assigned agent
-   Description
-   Comments and Work notes

</td></tr><tr><td>

![HR Agent Workspace case form callout 6](../image/6.png)

</td><td>

Activity stream

</td><td>

Comments, work notes, and current and past states of the case.

</td></tr><tr><td>

![HR Agent Workspace case form callout 7](../image/7.png)

</td><td>

Contextual side panel

</td><td>

Manage and work on the case using various task-oriented icons. The icons appearing on the Contextual side panel depend on the type of case that you are working on. For more information, see [HR Service Delivery Agent Workspace contextual side panel](learn-about-agent-ws-hr.md#).

</td></tr></tbody>
</table>## HR profile icons

Icons that enable you to get quick access to information about the opened for and subject person.

-   ![HR profile icon](../reference/images/hr-profile-icon.png): Select the **Open HR Profile** icon to access detailed information related to the person in the HR case. You will see details like HR profile, employee information, contact information, cases opened for the person etc. The same information is briefly displayed in the At-a-glance side panel.
-   ![Search for record icon](../image/magnifying-glass.png): Select the **Search for Record** icon to access a list of all related records within your company. The list is displayed relevant to the field on which you are searching. You can filter or sort in the list to refine your search results.
-   ![Open deep link icon](../reference/images/deep-link-icon.png): Select the Open deep link icon to access information outside of the application to help fulfill the case. For information about configuring deep links, see [Link generator for HR Service Delivery](HRLinkGenerator.md).

**Note:** For information on how to set up custom actions on record fields, see Set up custom actions on record fields in Workspace.

