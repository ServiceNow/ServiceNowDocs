---
title: Tasks page for AI Risk and Compliance
description: The Tasks page in the AI Risk and Compliance Workspace provides a single-pane view of your pending tasks, your group's tasks, and the tasks that are on your watchlist. You can also update the tasks directly from the Tasks page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/tasks-ai-risk-compliance.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Tasks page, pending tasks, AI Risk and Compliance workspace]
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Tasks page for AI Risk and Compliance

The Tasks page in the AI Risk and Compliance Workspace provides a single-pane view of your pending tasks, your group's tasks, and the tasks that are on your watchlist. You can also update the tasks directly from the Tasks page.

## Tabs in the Tasks page

The Tasks page in the AI Risk and Compliance Workspace displays the following tabs:

-   **My pending tasks**
-   **My group's tasks**
-   **My items**
-   **Watchlist**

A sample Tasks page for a logged-in user is shown in the following example. A user with the sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst role can view the Tasks workspace.

\[Omitted image "ai-tasks.png"\] Alt text: AI Risk and Compliance tasks page.

## My pending tasks

The **My pending tasks** section lets you access all the cases and tasks that have been assigned to you. This section includes the following information:

-   **AI asset tasks**: All the AI asset tasks assigned to you.
-   **AI assets**: Any AI assets assigned to you.
-   **Bulk risk assessments**: Any bulk risk assessments assigned to you.
-   **Cases**: All the AI cases assigned to you to work on.
-   **Inquiries**: AI inquiries pending with you for review. For example, as an AI case analyst, you created an inquiry and assigned it to an inquiry owner to work on. The inquiry owner completed the inquiry and submitted it to you for review. All such inquiries are available in this section.
-   **Issues**: All the issues originating from AI cases are visible to you.
-   **Risk assessments**: All the risk assessments of the AI systems are visible to you.

## My group's tasks

The **My group's tasks** section lets you access all the cases and tasks that have been assigned to your assignment group. This section includes the following information:

-   **Cases**: All the AI cases assigned to your assignment group.
-   **Inquiries**: All inquiries pending with your assignment group for review.

## My items

The **My items** section lets you access various items that have been assigned to you. This section includes the following information:

-   **AI asset tasks**: All the AI asset tasks assigned to you.
-   **Bulk risk assessments**: Any bulk risk assessments assigned to you.
-   **Inquiries**: AI inquiries pending with you for review.
-   **Issues**: All the issues originating from AI cases are visible to you.
-   **Policy exceptions**: All the policy exceptions for the AI systems are visible to you.

## Watchlist

The **Watchlist** section lets you access all the cases and tasks where you're added to the watchlist.

## Filter tasks

The Tasks page provides multiple filtering options to help you locate and review relevant tasks. Select the filter icon to apply additional conditions and refine the results displayed in the task list.

## Export tasks

The Export option lets you extract task data from the list view for external use or sharing. You can export the data in different file formats and choose how to receive the exported file.

When you select the **Export** button, a dialog opens where you can choose the file type, such as Excel, CSV, JSON, or PDF. Choose a format suitable for reporting, analysis, or documentation. You can select a delivery option to control how you receive the file:

-   **Download**: Generates the file and downloads it directly to your system.
-   **Email**: Sends the exported file to your registered email address.

The file is generated and delivered based on the selected delivery method.

## Edit columns

The Edit columns feature lets you customize the columns displayed across different tabs on the Tasks page. You can filter the list view by adding relevant columns or removing those that aren't needed. Within any tab, select a specific category to modify its list view. From the list actions \[Omitted image "list-actions-icon.png"\] Alt text: icon, access the column configuration option to manage the available columns. You can then move columns between the available and selected lists to control what appears in the view. After you save, the list displays only the chosen columns for that category.

## Assessment scope context

After upgrading to version 22.3.5, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role, assessment task list and work queue views display additional columns that show the governance scope \(related entity such as AI asset, model, or dataset\) of each control attestation-based assessment. These columns let you identify which AI asset, risk, and control an assessment belongs to without opening the individual record.

|Column|Description|
|------|-----------|
|**Applies to**|The assessable AI record within the entity, for example, a specific AI system, AI model, or dataset record. Use this column to identify the governance target without opening the assessment.|
|**Entity**|The type of AI record, such as AI system, AI model, or dataset that the assessable entity belongs to. This column shows the entity category, while **Applies to** shows the specific record within that category.|
|**Risk**|The risk that is in scope for this assessment. When an assessment targets a specific risk associated with an AI record, this column displays that risk so you can prioritize and triage assessment tasks across the list or work queue.|

If these columns aren't visible, use the **Edit columns** option to add them to the list view.

## Other options

On the Tasks page, use the following action buttons to manage the task list:

-   **New**: Creates a task from the current view.
-   **Delete**: Deletes tasks from the list.
-   **Edit**: Modifies the details of the selected task.
-   **Refresh**: Refreshes the list to display the latest updates.

**Related topics**  


[AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/ai-gov-lifecycle.md)

