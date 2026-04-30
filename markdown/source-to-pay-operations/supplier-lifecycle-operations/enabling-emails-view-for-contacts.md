---
title: Emails view for supplier managers
description: Supplier managers can access all emails including system-triggered emails, inbound replies, and error emails from the Source-to-Pay Workspace at case, task, and supplier levels.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-02-03"
reading_time_minutes: 3
breadcrumb: [Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Emails view for supplier managers

Supplier managers can access all emails including system-triggered emails, inbound replies, and error emails from the Source-to-Pay Workspace at case, task, and supplier levels.

**Important:** This feature is available from the March 26 Yokohama release onwards.

Supplier managers can access all emails linked with a case, task, or supplier from the **Emails** tab in the case, task, and supplier details pages respectively. Email actions are reflected, incomplete email errors are handled, and email-related activities can be summarized from the workspace.

## Email sources

-   System-triggered outbound notification emails \(for task creation\)
-   Inbound replies from supplier contacts \(for example, task completion email\)
-   Inbound replies from internal stakeholders \(for example, task completion email\)
-   Error handling emails

## Email notification to supplier stakeholders for tasks

When a task is created and assigned, the system automatically triggers an notification email to the assigned stakeholder.

-   When the task is assigned to a supplier contact, the email provides the receiver with two options: complete the task directly from the email, or view the task in the Supplier Collaboration Portal.
-   When the task is assigned to an internal stakeholder, the email provides the receiver with two options: complete the task directly from the email, or view the task in the Source-to-Pay Workspace.

**Note:** If the email subject or reference ID is modified while marking the task as complete via email, the system detects the mismatch and sends an automated error notification emails.

## Email summarization for tasks and cases

An AI summary of all emails linked to a task or case can be generated using the **Summarize** button on the **Emails** page.

The following sections are displayed:

-   **Summary**: Includes number of emails, key theme, tone, and actions required.
-   **Next steps**: Includes list of tasks, outstanding questions or escalations, and further updates.

To enable email summarization, set the default model for the One Extend capabilities.

1.  Navigate to **Sys\_One\_Extend\_Capability**.
2.  Open the **Summarize** record.
3.  In the **OneExtend Definition Configs** related list, verify that at least one model is marked as **Default** to **True**.

**Note:** Email summarization is not available for supplier records.

**Parent Topic:**[Using Source-to-Pay Workspace](../concept/use-supp-mgr-wsp.md)

**Related topics**  


[Create a supplier from the Source-to-Pay Workspace](new-supplier.md)

[Source-to-Pay Workspace Supplier page](../concept/supp-ws-details-page.md)

[Manage internal stakeholders](../concept/manage-internal-stakeholders.md)

[Manage supplier contacts from the Source-to-Pay Workspace](../concept/managing-contacts-smw.md)

[Manage supplier cases from the Source-to-Pay Workspace](../concept/managing-cases.md)

[Manage supplier tasks from the Source-to-Pay Workspace](../concept/managing-tasks.md)

[Offboard a supplier from the Source-to-Pay Workspace](offboard-supplier.md)

[Accept an incoming chat request from the Source-to-Pay Workspace](accept-chat-supp-ws.md)

[Interaction Management in Supplier Lifecycle Operations](../concept/interaction-mgmt-supplier-mgr-ws.md)

[Composing emails with predefined content from the Source-to-Pay Workspace](../concept/email-composer-slm-workspace.md)

[Overall supplier dashboard](../concept/overall-supplier-db.md)

[Create supplier case from Universal Request](create-supplier-case-ur.md)

