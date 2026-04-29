---
title: Create an exercise
description: Create an exercise in BCM UIB Workspace. You can then test your business continuity and recovery plans on a planned date and monitor the completion of the event tasks.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create an exercise

Create an exercise in BCM UIB Workspace. You can then test your business continuity and recovery plans on a planned date and monitor the completion of the event tasks.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select **New**.

    The **Create New Event** form is displayed as shown in the example.![Create New Event form.](../image/create-new-event.png)

2.  Fill in the required fields in the **Details** tab.

    For more information on the fields, see [Create Exercise Event form](../reference/create-exercise-event-ref-form.md).

    The exercise event is created in the **Pending** state and it is displayed in the List view. The state and details of the exercise event are displayed in the tabs:

    -   **Overview**: You can view the current state and overall state progression of the exercise event.
    -   **Details**: You can update the fields in the form such as **Short description**, **Assigned to**, **Exercise method**.
    -   **Assets**: You can select the impacted item type or the primary elements that you want to recover for an asset type.
    -   **Plans**: You can add an ad-hoc plan for the selected asset to the event.
    -   **Emergency Notifications**: You can create an emergency notification for the exercise event.
    -   **Event tasks**: You can add an ad-hoc task to the event.
    The Event form is shown in the example.

    ![Sample event form.](../image/event-form-details-tab.png)

3.  To perform more actions on the event, select **More actions**.

    |Step|Description|
    |----|-----------|
    |**Select __Discuss__.**|Add the subject for the discussion and add participants that have access to the event record. Include a brief message for the participants and select **Start discussion**.|
    |**Select __Generate MS Word__.**|Generate a report of the BIA, BCP, exercise, or crisis record in Microsoft Word format. The Microsoft Word copy of the event record is successfully generated that you can download.|
    |**Select __Generate PDF__.**|Generate a PDF of the event. The PDF of the event record is successfully generated that you can download. In the Impact Assessments section of the PDF, details of the Smart assessment are covered, including questions and answers for RPO and RTO in a tabular format, along with dependencies, contributors, and attachments.|
    |**Select __360º view__.**|Generate 360º relationships for the event. A graphical presentation of the event and its relationships is displayed. Refresh the planned order for the recovery task|
    |**Select __Delete__.**|Delete the event record. A warning message is displayed that deleting the record will result in an automatic deletion of related records, which may also cause a cascade of additional records to be deleted.|

4.  Select **Save**.

    The event is saved in the **Pending** state.


-   **[Create Exercise Event form](../reference/create-exercise-event-ref-form.md)**  
Use the Create Exercise Event form in BCM UIB Workspace to add details about an Exercise event.

**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)

