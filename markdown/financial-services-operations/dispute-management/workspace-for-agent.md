---
title: Dispute agent workspace
description: The dispute agent workspace provides a single, streamlined, and consistent workflow for agents. This workspace offers alignment with back‑end process steps and easier decision‑making through each stage of a dispute. The landing page provides an overview of your cases and tasks, which helps to monitor your workload, focus on high-priority items, and track the status of disputes.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Dispute agent workspace

The dispute agent workspace provides a single, streamlined, and consistent workflow for agents. This workspace offers alignment with back‑end process steps and easier decision‑making through each stage of a dispute. The landing page provides an overview of your cases and tasks, which helps to monitor your workload, focus on high-priority items, and track the status of disputes.

**Role required**: To access the disputes page, you need to have these roles: sn\_bom\_credit\_card.admin or sn\_bom\_credit\_card.dispute\_agent.

**Note:** The widgets and the data that are displayed in the widgets depend on your role.

## User interface of Dispute workspace

The disputes workspace for Financial Services Operations provides a centralized interface for managing and resolving dispute cases. As a dispute agent, you can resolve disputes in a visual and consistent workflow by handling chargebacks, fraud reports, duplicate transactions, SLAs, and ensure timely resolutions.

Let's understand the Financial Services Operations disputes page.![Dashboard of the tasks opened](../image/my-tasks.png)

The **Card Dispute Landing Page** consists of a dashboard with the following sections.

-   Your cases and tasks.
    -   Open vs resolved cases and task
    -   SLAs breached or at risk
    -   Agent workload
-   Team cases and tasks

## Dispute life cycle

The dispute life cycle of Financial Services Operations includes the following stages:

-   **Initiate**: Submit a dispute case in a playbook

    ![Dispute displayed as playbook](../image/dispute-initiate.png)

-   Processing: Investigate the dispute. In this stage, each transaction within a dispute case is presented as a process-based layout. This layout visually represents the distinct stages of the investigation workflow for that specific transaction.

    The Processing stage includes these stages:

    1.  Investigate
    2.  Chargeback
    3.  Complete
-   Closure: Close the case.

The dispute agent has continuous visibility into key financial transaction details while working on tasks, regardless of the transaction's stage.

The **Dispute Workspace** displays a list of all open tasks for the agent, each showing its SLA and current State.

-   When the agent selects a task, the task details expand and the Activity stream shifts down.
-   The agent can take action on a task directly within the expanded view without navigating to another tab.
-   The agent can attach documents related to the task within the task detail section.
-   The agent can write work notes for the task, which appears in the activity stream once the task is saved.
-   After a task is complete, it automatically moves to the **Closed** tab.

**Note:** If Card Data Security is installed and configured, **Attachments** in the contextual side panel will handle files differently in transaction records. For more information, see [Manage attachments in Card Data Security](../../fso-card-data-security/concept/manage-attachments-in-card-data-security.md).

**Parent Topic:**[Managing Disputes](managing-disputes.md)

