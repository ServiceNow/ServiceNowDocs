---
title: Tasks page for AI Risk and Compliance
description: The Tasks page in the AI Risk and Compliance Workspace provides a view of your pending tasks, your group's tasks, and your watchlist. You can update tasks directly from the Tasks page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/tasks-ai-risk-compliance.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Tasks page, pending tasks, AI Risk and Compliance workspace]
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Tasks page for AI Risk and Compliance

The Tasks page in the AI Risk and Compliance Workspace provides a view of your pending tasks, your group's tasks, and your watchlist. You can update tasks directly from the Tasks page.

## Tabs in the Tasks page

The Tasks page in the AI Risk and Compliance workspace displays the following tabs:

-   **My pending tasks**
-   **My group's tasks**
-   **My items**
-   **Watchlist**

A sample Tasks page for a logged-in user is shown in the following example. A user with the sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst role can view the Tasks page.

\[Omitted image "ai-tasks.png"\] Alt text: AI Risk and Compliance tasks page.

## My pending tasks

The **My pending tasks** section helps you to access all the cases and tasks that have been assigned to you. This section includes the following information:

-   **AI asset tasks**: All the AI asset tasks assigned to you.
-   **Bulk risk assessments**: Any bulk risk assessments assigned to you.
-   **Cases**: All the AI cases assigned to you to work on.
-   **Inquiries**: AI inquiries pending with you for review. For example, as an AI case analyst you create an inquiry and assigned it to an inquiry owner to work on it. The inquiry owner completed the inquiry and submitted it to you for review. All such inquiries are available in this section.
-   **Issues**: All the issues originating from AI cases, Risk assessments, Control attestations, and more are visible to you.
-   **Risk assessments**: All the risk assessments of the AI systems are visible to you.

## My group's tasks

The **My group's tasks** section helps you access all the cases and tasks that have been assigned to your assignment group. This section includes the following information:

-   **Cases**: All the AI cases assigned to your assignment group.
-   **Inquiries**: All inquiries pending with your assignment group for review.

## My items

The **My items** section helps you to access various items that have been assigned to you. This section includes the following information:

-   **AI asset tasks**: All the AI asset tasks assigned to you.
-   **Bulk risk assessments**: Any bulk risk assessments assigned to you.
-   **Inquiries**: AI inquiries pending with you for review.
-   **Issues**: All the issues originating from AI cases are visible to you.
-   **Policy exceptions**: All the policy exceptions for the AI systems are visible to you.

## Watchlist

The **Watchlist** section lets you access all the cases and tasks where you're added to the watchlist.

## Edit list

You can add or remove the reporting columns under any of the tabs on the Tasks page. To add or remove columns:

1.  Navigate to the required tab and select the required category.
2.  Select the List Actions icon \[Omitted image "list-actions-icon.png"\] Alt text: and then **Edit columns**.
3.  Select and move the required columns from the list of **Available columns** to **Selected columns** and the other way around.
4.  Select **OK**.

The selected columns are added or removed.

## Assessment scope context

After upgrading to version 22.3.5, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role, assessment task list and work queue views display additional columns that show the governance scope \(related entity such as AI asset, model, or dataset\) of each control attestation-based assessment. These columns let you identify which AI asset, entity, and control an assessment belongs to without opening the individual record.

<table id="table_scope_context_columns"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Applies to**

</td><td>

Specific AI record that the assessment targets, such as a particular AI system, AI model, or dataset. Use this column to identify the exact governance target without opening the assessment.

</td></tr><tr><td>

**Entity**

</td><td>

Type of AI record associated with the assessment, such as AI system, AI model, or dataset. This column shows the category of the record, while **Applies to** shows the specific record within that category.

</td></tr><tr><td>

**Control**

</td><td>

Control associated with the assessment. When an assessment is generated for a specific control on an AI record, this column displays the control. Use this column to help you prioritize and triage tasks directly from the list or work queue.

</td></tr></tbody>
</table>If these columns aren't visible, use the **Edit columns** option to add them to the list view.

## Other options

On the Tasks page, use the following action buttons to manage the task list:

-   **New**: Creates a task in the current view.
-   **Delete**: Deletes tasks from the list.
-   **Edit**: Modifies the details of the selected task.
-   **Refresh**: Refreshes the list to display the latest updates.

