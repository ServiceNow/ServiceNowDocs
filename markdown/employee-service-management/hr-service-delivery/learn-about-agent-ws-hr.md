---
title: Exploring HR Service Delivery Agent Workspace
description: Use HR Service Delivery Agent Workspace to manage your employee HR requests from one place.The contextual side panel in HR Service Delivery Agent Workspace provides information designed to help you work an HR case and interact with your employees.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Exploring HR Service Delivery Agent Workspace

Use HR Service Delivery Agent Workspace to manage your employee HR requests from one place.

**Important:**

-   HR Service Delivery Agent Workspace \(Classic\) is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.
-   If you are an existing user of HR Service Delivery Agent Workspace \(Classic\), you can migrate to the Agent Workspace for HR Case Management \(Configurable\) for enhanced features and capabilities. See [Migration Guidelines](https://www.servicenow.com/community/hrsd-articles/hr-agent-workspace-migration-guidelines-from-classic-to/ta-p/2310606).

## Home page

The Home page provides you with an overview of your work at a glance. It provides you with information that can help you decide what you should act on first, like HR cases and their Service Level Agreement \(SLA\) status, items that affect your team, and general information and announcements.

## Case list

From the Home page, you can access the Case list. The Case list provides you with a view into all HR cases or you can filter and sort by what is relevant to you.

## HR case form

Manage multiple cases, view information that is related to the case, and use knowledge articles or similar cases to manage the case.

<table id="table_obz_g2x_gjb"><thead><tr><th>

Agent Workspace feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tabs

</td><td>

Tabs display lists, HR case numbers, and the Add icon![Add icon](../image/IconCreateRecordMenu.png). The Add icon enables you to instantly **Create HR case** or **Create interaction**.When you have multiple tabs open, you can only see the case number on the tab by default. However, you can also configure the information you want to be displayed on the tab. For more information, see [Customize tab label in Agent Workspace for HR Case Management](../task/customise-tab-lable-agent-ws.md).

 If you point to the number, you can quickly see more details related to a case, for example, the description of the case, HR Service and Subject person.

</td></tr><tr><td>

Form header

</td><td>

Displays brief details of an HR case like HR service, priority, state, and assigned-to agent.

</td></tr><tr><td>

UI actions

</td><td>

Action button that enables you to save changes you made, change the status, cancel, or other relevant actions for a case.**Note:** The buttons that appear are similar to the native platform UI.

The button types that appear depends on the type and status of the HR case.

</td></tr><tr><td>

Related items

</td><td>

Shows details about the HR case and records from other tables that have a relationship with the HR case.**Note:** When a case appears under Playbook, these tabs change. For more information, see [Exploring HR Service Delivery Playbook](playbook-hr-explore.md).

</td></tr><tr><td>

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

Activity stream

</td><td>

Comments, work notes, and current and past states of the case.

</td></tr><tr><td>

Contextual side panel

</td><td>

Manage and work on the case using various task-oriented icons. The icons appearing on the Contextual side panel depend on the type of case that you are working on. For more information, see [HR Service Delivery Agent Workspace contextual side panel](learn-about-agent-ws-hr.md#).

</td></tr></tbody>
</table>## Tabs

Use tabs to display the records that are associated with an HR case, like case details and tasks. You can select a tab and jump to the information. Child tabs appear below the top tabs and display case details, HR profile information, and tasks.

**Note:** Any reference that you select under a parent tab opens as a child tab.

## Related Items menu

Use the Related Items menu to see information about the details, tasks, and other information that is associated with a case. This menu provides a quick and easy way to look up information about a case and subject person.

**Note:** The type of HR case determines what tabs appear.

## HR profile icons

Icons that enable you to get quick access to information about the opened for and subject person.

-   ![HR profile icon](../reference/images/hr-profile-icon.png): Select the HR profile icon to access the HR profile for people who are related to the case. Selecting an HR profile also displays the at-a-glance side panel where you can see information that your HR admin configures and other things like the email, office location, and the employee's organization information. For more information, see the [At a Glance panel](hr-profile-for-hr-agent-workspace.md#).
-   ![Search for record icon](../image/magnifying-glass.png): Select the Search for record icon to access a list of all HR profiles within your company.
-   ![Open deep link icon](../reference/images/deep-link-icon.png): Select the Open deep link icon to access information outside of the application to help fulfill the case. For information about configuring deep links, see [Link generator for HR Service Delivery](HRLinkGenerator.md).

**Note:** For information on how to set up custom actions on record fields, see Set up custom actions on record fields in Workspace.

## HR Service Delivery Agent Workspace contextual side panel

The contextual side panel in HR Service Delivery Agent Workspace provides information designed to help you work an HR case and interact with your employees.

The contextual side panel provides a column of icons that provides you with information. Use the information when you interact with your employees or to complete the case.

The icons that appear depend on the type of HR case you are looking at.

<table id="table_tgj_p2l_cjb"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Click the At a Glance icon to show the At a Glance panel](../image/agent-ws-hr-at-a-glance-icon.png)

</td><td>

At a Glance: Provides key HR profile details for fast recall. Having this information readily available helps agents understand who they are trying to help when communicating with an employee.

</td></tr><tr><td>

![Agent Assist icon](../reference/images/knowledge-base-icon.png)

</td><td>

Agent Assist: Provides relevant knowledge articles about the case. You can also provide comments \(visible to employee\) or work notes \(not visible to employee\) or view all activities related to the case.**Note:** Agent Assist is also available for HR interactions.

</td></tr><tr><td>

![Employee Documents icon](../reference/images/employee-docs-icon.png)

</td><td>

Employee Documents: Lists documents related to the case you are on. Select the document and you can download it or rename it.**Note:** The Contextual side panel requires the Employee Document Management \[com.sn\_employee\_document\_management\] plugin to display the employee documents. For more information, see [Employee Document Management](hr-employee-doc-management.md).

</td></tr><tr><td>

![Attachment icon](../image/attach-icon.png)

</td><td>

Attachments: Documents relevant or related to the HR case are displayed as attachments. These attachments can be moved to Employee Document Management \(EDM\) for archival and historical purposes. For example, receipts for tuition reimbursement are attachments to an HR case. After you move attachments to Employee Document Management, they will be employee documents. See [Move employee documents using HR Service Delivery Agent Workspace](agent-ws-hr-edm.md#).Select an attachment to download or delete it.

 **Note:** A small green dot indicates there are attachments ![HR Agent WS - Attachment icon](../image/agent-ws-hr-attach-icon.png).

</td></tr><tr><td>

![Response Template icon](../reference/images/response-template-icon.png)

</td><td>

Response Templates: Shows reusable messages that you can use when responding to an employee that has a question about their case. Copy the text from the response template you want to use and paste the text into the Comments or Work notes section of the HR case.

 An HR service configures response templates and are a fast, consistent, and efficient way to respond to common questions related to HR cases.

 For more information, see [Response templates for HR Service Delivery](hr-templated-snippets.md#).

</td></tr><tr><td>

![Fulfillment instructions icon](../reference/images/fulfill-insts-icon.png)

</td><td>

Fulfillment Instructions: Provides you with focused and targeted information on how to complete an HR case faster and more efficiently. Can include specific instructions, KB articles, or a checklist of what to do on the case.

 For more information, see [HR fulfillment instructions](hr-fulfillment-instructions.md).

</td></tr><tr><td>

![Checklist icon](../reference/images/checklist-icon.png)

</td><td>

Checklist: Provides you with a list of things that need to be checked or done. Checklist helps you in resolving an issue efficiently and in a quicker way.For more information, see [Using checklists in HR Service Delivery Agent Workspace](agent-ws-hr-checklists.md).

</td></tr></tbody>
</table>