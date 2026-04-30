---
title: Communicating with stakeholders about incidents and major incidents in SOW
description: Use the Communicate tab to create and manage all communications with stakeholders during the various phases of an incident or a major incident.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Managing a major incident record, Major Incident Management in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Communicating with stakeholders about incidents and major incidents in SOW

Use the **Communicate** tab to create and manage all communications with stakeholders during the various phases of an incident or a major incident.

The **Communicate** tab contains the following options to create and manage communications:

-   **Group By**

    Group communication tasks the following ways:

    -   Communication plan – The communication tasks that are associated with a particular communication plan are grouped.
    -   Completion status - The communication tasks are grouped based on the completion status and due dates. You can choose to list the tasks from the following group sections:
        -   Overdue – Communication tasks with past due dates.
        -   Upcoming – Communications tasks with an upcoming due date.
        -   Completed – Communication tasks that are completed.
        -   Skipped – Communication tasks that are skipped.
-   **Filter by communication plan**

    Filter the communication task by a communication plan.

-   **Compose**

    Compose a communication message, such as an email, DEX Desktop Assistant, SMS, Microsoft Teams, or Slack message. For more information on DEX Desktop Assistant, see [Use DEX Desktop Assistant](../../digital-end-user-experience/concept/use-dex-desktop-exp.md).

    **Note:**

    DEX Desktop Assistant is supported as a channel in Major Incident Management in SOW only if the following conditions are met:

    -   SOW must be version 7.0 or later.
    -   The instance must be on Yokohama release or later.
    -   DEX must be version 2.5.0 or later.
-   **Manage recipients**

    Add and manage recipients for a communications task. You can add a user role and a user in the recipient list. You can also access this option by selecting the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon on the communication task and then selecting **Manage recipients**.

-   **New Communication**

    Create a communication task. This option is available only to the following users:

    -   User with the major\_incident\_manager role
    -   User with both the ia\_admin and itil roles
-   **Manage announcements**

    Create and manage an announcement to broadcast messages for Service Portal users to keep them informed about the ongoing major incident.

-   **View Record**

    View detailed information about the incident communication task \(ICT\) record. Select the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon on the communication task and then select **View record**.

    From the ICT record, you can do the following actions:

    -   Initiate a call or chat from the collaborate tab on the side panel using the **Collaborate** \(![Collaborate icon](../image/mim-collaborate-icon.png)\) icon on the contextual side panel. For more information, see [Collaborate with stakeholders during a major incident](../task/collaborate-stakeholders-mim-sow.md).
    -   Add collaboration channels from the Communication Channel related list of the **Related records** tab.
    -   Add communication channels such as DEX Desktop Assistant from the Communication Channel related list of the **Related records** tab.
-   **Close**

    Close the communication task. Select the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon on the communication task and then select **Close**. The communication task is then moved to either the Completed or Skipped section of the **Communicate** tab based on the following scenarios:

    -   If a communication task has the **Frequency** field set to **Recurring** and at least one communication has been composed and sent, selecting **Close** moves the communication task to the Completed section.
    -   If a communication task has the **Frequency** field set to **One time** or **Recurring** and no communication has been composed and sent, selecting **Close** moves the communication task to the Skipped section.
-   **Start**

    Start the communication task with the **Pending** status. Select the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon on the communication task and then select **Start**.

-   **Snooze**

    Increase the **Due in** time for a communication task. Select the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon on the communication task and then select **Snooze**.


-   **[Compose communications for incidents and major incidents](../task/compose-communication-mim-sow.md)**  
Compose communication messages for incidents and major incidents using communication channels such as email and SMS.
-   **[Manage recipients in a communication task](../task/manage-recipients-mim-sow.md)**  
Manage the recipients list for a communication task to create flexible and effective communication with the required stakeholders.
-   **[Create an adhoc communication task](../task/create-adhoc-comm-task-mim-sow.md)**  
Create an adhoc communication task as required during the various phases of an incident in Major Incident Management.
-   **[Manage an announcement for communicating about major incidents](../task/create-announcements-major-inc.md)**  
Create and manage an announcement to broadcast messages for Service Portal users to keep them informed about the ongoing major incident. Major incident managers can create and deploy announcements from Service Operations Workspace \(SOW\).

**Parent Topic:**[Managing a major incident record](managing-major-incident-sow.md)

