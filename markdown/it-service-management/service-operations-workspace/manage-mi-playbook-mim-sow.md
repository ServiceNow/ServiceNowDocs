---
title: Manage major incidents using the MI playbook
description: Manage major incidents using the MI playbook from the contextual side panel or the Playbook tab of an incident record page. This playbook provides a simple, concise, and task-oriented interface for managing the major incident process.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Managing major incidents using playbooks, Managing a major incident record, Major Incident Management in Service Operations Workspace, Incident Management in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Manage major incidents using the MI playbook

Manage major incidents using the MI playbook from the contextual side panel or the **Playbook** tab of an incident record page. This playbook provides a simple, concise, and task-oriented interface for managing the major incident process.

## Before you begin

The incident must be proposed as a major incident candidate. For more information, see [Propose a major incident](propose-major-incident-sow.md).

The MI playbook must be assigned to Major Incident Management. For more information, see [Assign a playbook to Major Incident Management](assign-playbook-mim-sow.md).

Role required: major\_incident\_manager or admin

## About this task

The MI playbook in Service Operations Workspace provides a guided approach to the entire major incident process. It provides a way to visualize business process workflows for major incidents in a simple, concise, and task-oriented view.

## Procedure

1.  Open an incident record that has been proposed as a major incident candidate.

2.  Select the **Major Incident Playbooks** \(![Major incident playbook](../image/mim-playbook-icon.png)\) icon on a contextual side panel to launch the major incident playbook.

    The Major Incident Playbook panel opens on the side panel. The panel includes the following tabs:

    -   Current
    -   History
3.  On the **Current** tab, select **MI playbook**.

    You can view the major incident process steps and your progress along the following steps:

    -   Review Situation
    -   Communicate
    -   Collaborate
    -   Adhoc Communications &amp; Collaborations
    -   Resolve
    -   Create problem
    -   Post Incident Review
    ![List of the major incident process steps to complete found in the MI Playbook](../image/mi-playbook.png)

4.  Review the incident information and then promote the major incident.

    1.  Select **Review Situation**.

    2.  Review the incident information.

    3.  Select **Promote** to promote the incident to a major incident based on the incident information.

        For more information, see [Promote a major incident](promote-major-incident-sow.md).

5.  Communicate with stakeholders by composing a communication message, such as email or SMS.

    1.  Select **Communicate**.

    2.  On a communication task that you want to complete, select **Compose** to compose a communication message, such as email or SMS.

        For more information, see [Compose communications for incidents and major incidents](compose-communication-mim-sow.md).

    3.  Select the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon for a communication task and then select **Manage Recipients** to add or manage the recipients for communications.

        For more information, see [Manage recipients in a communication task](manage-recipients-mim-sow.md).

    For more information, see [Compose communications for incidents and major incidents](compose-communication-mim-sow.md). You can also add or manage recipients for the communications. For more information, see [Manage recipients in a communication task](manage-recipients-mim-sow.md).

6.  Collaborate with stakeholders.

    1.  Select **Collaborate**.

    2.  Select a collaboration record, and then select one of the following options based on the selected type of collaboration channel:

        -   Start - To start a call.
        -   Open discussion - To start a chat.
        For more information on how to use these collaboration channels, see [Collaborate with stakeholders during a major incident](collaborate-stakeholders-mim-sow.md).

7.  Perform unplanned communications and collaborations.

    1.  Select **Adhoc collaboration and communication**.

        This section contains the following collaboration and communication records that are created separately than pre-defined and configured communications and collaboration plans:

        -   Communications – All the communications that you create using the **New communication** option from the **Communicate** tab or using the Incident communication plan related list on the **Related records** tab are displayed in this section. For more information on creating unplanned communications, see [Create an adhoc communication task](create-adhoc-comm-task-mim-sow.md) and [Create adhoc communication and collaboration using the Related record tab](create-adhoc-comm-collab-mim-sow.md).
        -   Collaboration – All the collaboration records that you create using the Incident Communications plan related list on the **Related records** tab are displayed in this section. For more information on creating unplanned communications and collaboration, see [Create adhoc communication and collaboration using the Related record tab](create-adhoc-comm-collab-mim-sow.md).
    2.  Select the one of the following options for unplanned communications and collaboration.

        -   For unplanned communications, you can do one of the following actions:
            -   Select **Compose** to compose a communication message such as email or SMS. For more information, see [Compose communications for incidents and major incidents](compose-communication-mim-sow.md).
            -   Select the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon for a communication task and then select **Manage Recipients** to add or manage the recipients list for the communication task. For more information, see [Manage recipients in a communication task](manage-recipients-mim-sow.md).
        -   For unplanned collaboration, you can do one of the following actions:
            -   Start a call - Select **Start** on a collaboration record to start a call with the stakeholders. For more information, see [Collaborate with stakeholders during a major incident](collaborate-stakeholders-mim-sow.md).
            -   Start a chat – Select **Open discussion** to start a chat with the stakeholders. For more information, see [Collaborate with stakeholders during a major incident](collaborate-stakeholders-mim-sow.md).
8.  Select **Resolve**.

    For information on how to resolve a major incident, see, [Resolve and close a major incident](resolve-close-mim-sow.md).

9.  Select **Create Problem**.

    **Note:** This section is visible in the playbook only if:

    -   The incident doesn’t have a problem record associated with it.
    -   The Problem Management Best Practice - Madrid - State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin is activated on the instance.
    -   The **Create problem from major incident** flow is inactive on the instance. This flow is shipped as part of the base system in the **Inactive** status. Once activated, it creates a problem record automatically when an incident is promoted to a major incident.
    You can also configure if the incident field information is copied automatically to the respective fields in a problem record using the **List of attributes \(comma-separated\) that will be copied from the incident to create a new problem** \(**com.snc.problem.create\_from\_incident.attributes**\) system property when a problem record is created. For more information, see [Create a problem](../../problem-management/task/create-a-problem-v2.md).

    A problem record is created automatically. You can select **View Problem** to view the problem record on a separate tab.

10. Mark the post incident review as complete.

    1.  Select **Post Incident Review**.

    2.  Select **Mark Complete** to end the major incident process in the **Playbook** side panel.

        You can continue to work on the post incident report review from the **Post Incident Report** tab on the Incident record page. For more information, see [Review and update a post incident report](review-update-pir-mim-sow.md).


**Parent Topic:**[Managing major incidents using playbooks](../concept/managing-mi-playbook-sow.md)

