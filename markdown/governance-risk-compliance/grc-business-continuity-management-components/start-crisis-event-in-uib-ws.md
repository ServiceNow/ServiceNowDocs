---
title: Start a crisis event
description: Report a crisis event in the BCM Configurable Workspace. A crisis event is any significant disruption that threatens business operations. The BCM Configurable Workspace enables you to create crisis records, classify severity levels, set priorities, assign response teams, and document initial actions.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Start a crisis event

Report a crisis event in the BCM Configurable Workspace. A crisis event is any significant disruption that threatens business operations. The BCM Configurable Workspace enables you to create crisis records, classify severity levels, set priorities, assign response teams, and document initial actions.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **crisis events** &gt; **Pending** and select **New**.

    The **Create New Event** form is displayed.

3.  In the **Details** tab of the **Create New Event** form, fill in the required fields.

    **Note:** For a crisis event, the event type is **Actual**.

    For more information on the fields, see [Create Crisis Event form](../reference/create-crisis-event-ref-form.md).

    A crisis event is created in the **Pending** state as shown in the example.

    ![Details of the crisis event.](../image/crisis-event-pending-state.png)

    The state and details of the crisis event are displayed in the tabs:

    -   **Overview**: You can view the current state and overall state progression of the crisis event.
    -   **Details**: You can view details on the crisis event such as its short description, state, event type, assignee, and so on.
    -   **Assets**: You can select the impacted item type or the primary elements that you want to recover for an asset type.
    -   **Plans**: You can add an ad-hoc plan for the selected asset to the crisis event.
    -   **Emergency Notifications**: You can create a notification for the crisis event with the Everbridge integration.
    -   **Event tasks**: You can add an ad-hoc task to the crisis event.
4.  To perform more actions on the crisis event, select **More actions**.

    |Step|Description|
    |----|-----------|
    |**Select __Discuss__.**|Add the subject for the discussion and add participants that have access to the event record. Include a brief message for the participants and select **Start discussion**.|
    |**Select __Generate MS Word__.**|Generate a report of the BIA, BCP, exercise, or crisis record in Microsoft Word format. The Microsoft Word copy of the event record is successfully generated that you can download.|
    |**Select __Generate PDF__.**|Generate a PDF of the event. The PDF of the event record is successfully generated that you can download. In the Impact Assessments section of the PDF, details of the Smart assessment are covered, including questions and answers for RPO and RTO in a tabular format, along with dependencies, contributors, and attachments.|
    |**Select __360º view__.**|Generate 360º relationships for the event. A graphical presentation of the event and its relationships is displayed. Refresh the planned order for the recovery task|
    |**Select __Delete__.**|Delete the event record. A warning message is displayed that deleting the record will result in an automatic deletion of related records, which may also cause a cascade of additional records to be deleted.|

5.  Select **Save**.

    The crisis event is saved in the **Pending** state and it is displayed in the Crisis events list view of the record.


-   **[Create Crisis Event form](../reference/create-crisis-event-ref-form.md)**  
Use the Create Crisis Event form in BCM UIB Workspace to add details about a crisis event.

**Parent Topic:**[Structured workflows for crisis events](../concept/perform-tasks-to-manage-crisis-events.md)

