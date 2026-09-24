---
title: Start a crisis event
description: Report a crisis event in the BCM Configurable Workspace. A crisis event is any significant disruption that threatens business operations. The Business Continuity Workspace enables you to create crisis records and document initial actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/start-crisis-event-in-uib-ws.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Start a crisis event

Report a crisis event in the BCM Configurable Workspace. A crisis event is any significant disruption that threatens business operations. The Business Continuity Workspace enables you to create crisis records and document initial actions.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **crisis events** &gt; **Pending** and select **New**.

    The **Create New Event** form is displayed. By default, the event is in the **Pending** state.

3.  In the **Details** tab of the **Create New Event** form, add the description, impact, and priority of the event.

    **Note:** The event type is **Actual**.

    For field descriptions, see [Create Crisis Event form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-crisis-event-ref-form.md).

    \[Omitted image "cm-level-field-in-crisis-event.png"\] Alt text: Level field on the Create New Event form with 1-Site, 2-Regional, 3-Corporate, and 4-Global options.

4.  Choose a level for the crisis event.

    The **Level** field in the event header shows the escalation level of the crisis event and persists across all tabs. Select the field to update it to **1-Site**, **2-Regional**, **3-Corporate**, or **4-Global**, as shown in the example. The **BCM viewer** role sees this field as read-only, consistent with its read-only access across the crisis event record.

5.  To assign individual ownership only, select the **Assign to** field or to assign group ownership only, select the **Assignment group** field and save the record.

6.  Select **Save**.

    The crisis event is saved in the **Pending** state and appears in the Crisis events list view of the record.

    The tabs display the crisis event state and details:

    -   **Overview**: You can view the current state and overall state progression of the crisis event.
    -   **Details**: You can view details on the crisis event such as its short description, state, event type, assignee, and so on.
    -   **Assets**: You can select the impacted item type or the primary elements that you want to recover for an asset type.
    -   **Plans**: You can add an ad-hoc plan for the selected asset to the crisis event.
    -   **Action items**: You can view and create action items assigned during the response to the crisis event.
    -   **Emergency Notifications**: You can create a notification for the crisis event with the Everbridge integration.
    -   **Issues**: You can view and create issues associated with the crisis event.
    -   **Similar tasks groups**: You can group duplicate or similar event tasks together to eliminate redundant work.
    -   **Collaborations**: You can view and create collaboration threads that coordinate the response to the crisis event with recovery teams. For more information, see [Creating collaborations in exercises and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/creating-collaboration-threads-in-crisis.md).
    -   **Event tasks**: You can add an ad-hoc task to the crisis event.
    A crisis event is created in the **Pending** state.

    \[Omitted image "new-crisis-event-added.png"\] Alt text: New event added. \[Omitted image "cm-collaborations-rel-list-event-record.png"\] Alt text: Crisis event record with the Overview, Details, Assets, Plans, Action items, Issues, Similar tasks groups, Collaborations, and Event tasks tabs.

7.  To perform more actions on the crisis event, select **More actions**.

    |Action|Description|
    |------|-----------|
    |**Select __Discuss__.**|Add a subject, participants, and message, then select **Start discussion**.|
    |**Select __Generate MS Word__.**|Generates a downloadable Microsoft Word report of the event record.|
    |**Select __Generate PDF__.**|Generates a downloadable PDF of the event record. The Impact Assessments section includes Smart assessment questions and answers for RPO and RTO, dependencies, contributors, and attachments.|
    |**Select __360º view__.**|View a graphical presentation of the event and its relationships.|
    |**Select __Delete__.**|Deletes the event and its related records.|

8.  View pending tasks for your event group and assigned items for the event owner in the My tasks page.

9.  Review the **Activity** panel of the event to track a consolidated timeline of the event.

    Activity from the plans, action items, and collaboration threads associated with the event is propagated to the event's **Activity** panel, so you can track everything that happens during the event — for example, when assets are added from an activated plan, when a collaboration thread is created, or when an email is sent — from a single place.

10. Review and confirm the group ownership, issue details, and collaboration thread details for the event in separate sections of the PDF and Microsoft Word reports.

    For collaboration block details in the collaboration block in Microsoft Word and PDFs, see [Create a collaboration thread in a crisis event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/compose-email-collaboration-thread-crisis.md). For Microsoft Word template details with collaboration block, see [Add a collaboration block to the Word template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/add-collaboration-block-docudesigner.md).


-   **[Create Crisis Event form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-crisis-event-ref-form.md)**  
Use the Create Crisis Event form in BCM UIB Workspace to add details about a crisis event.

**Parent Topic:**[Structured workflows for crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/perform-tasks-to-manage-crisis-events.md)

**Related topics**  


[My tasks page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/my-tasks-page-uib-ws.md)

[Group ownership in BIA, plan, and event records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/group-ownership-bias.md)

[Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/managing-issues-in-bcm.md)

