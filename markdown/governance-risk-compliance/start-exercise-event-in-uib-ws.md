---
title: Create an exercise
description: Create an exercise in BCM UIB Workspace. You can then test your business continuity and recovery plans on a planned date and monitor the completion of the event tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/start-exercise-event-in-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Structured workflows for Exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create an exercise

Create an exercise in BCM UIB Workspace. You can then test your business continuity and recovery plans on a planned date and monitor the completion of the event tasks.

## Before you begin

Role required: sn\_bcm.program\_manager, for event assignment group filter: sn\_recovery.event\_user, sn\_recovery.event\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select **New**.

2.  Fill in the required fields in the **Details** tab.

    For more information on the fields, see [Create Exercise Event form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-exercise-event-ref-form.md).

    The exercise event is created in the **Pending** state and it is displayed in the List view. The state and details of the exercise event are displayed in the tabs:

    -   **Overview**: You can view the current state and overall state progression of the exercise event.
    -   **Details**: You can update the fields in the form such as **Short description**, **Assigned to**, **Exercise method**.
    -   **Assets**: You can select the impacted item type or the primary elements that you want to recover for an asset type.
    -   **Plans**: You can add an ad-hoc plan for the selected asset to the event.
    -   **Emergency Notifications**: You can create an emergency notification for the exercise event.
    -   **Event tasks**: You can add an ad-hoc task to the event.
3.  In the User Administration or Assignment details section, locate the **Event owner group** and **Event owner** fields.

4.  To assign group ownership, select the **Event owner group** field and select a group from the list.

    The list shows only groups that hold the Event Owner or equivalent BCM Manager role. This role-based filtering verifies that only eligible groups are displayed as selectable options.

    \[Omitted image "event-grp-owner-field.png"\] Alt text: Event owner group field.

5.  Select the **Event owner** field \(individual owner\) and select a user from the filtered list.

    The list now shows only members of the group you selected in the previous step. You can choose the specific person responsible for the record.

6.  To assign individual ownership only, select the **Event owner** field, select a user, and save the record.

    The Event record is owned by the selected individual. The **Event owner group** field remains empty. This is the legacy ownership model and is fully supported alongside group ownership.

7.  To assign group ownership only, select the **Event owner group** field, select a group, leave the **Event owner** field \(individual owner\) empty and save the record.

    The Event record is owned by the group as a whole, with no specific individual designated. Any member of the group can take action on the record.

8.  To change the individual owner when a group is selected, select **Event owner**, clear the current selection, select a new user from the filtered list, and save the record.

    The individual owner is updated while the group ownership remains unchanged.

9.  To handle the "outside group" scenario, select an individual owner, select the **Event owner group** field, select a group that does not include the previously selected owner, and save the record.

    The record saves with both the individual owner and the group. This accommodates cases where an individual outside the group is responsible for the record.

10. To remove a group and revert to unfiltered selection, clear the **Event owner group** field, select a user in the **Event owner** field, and save.

    The group field clears, reverting to individual-only ownership.

11. To validate ownership requirements, verify at least one of the **Event owner group** field or the **Event owner** field is populated and save.

    If both are empty, both fields highlight in red with an asterisk and a validation error appears. An informational banner prompts you to select either a group or an individual. The record saves only when at least one ownership field is populated.

12. Complete the remaining required fields on the Event record form and save the record.

    The Event record is now owned by the selected group, with a specific individual designated as the point of contact. If the individual leaves the group, the group ownership remains intact, and another member can take over as the individual owner.

13. To perform more actions on the event, select **More actions**.

    |Step|Description|
    |----|-----------|
    |**Select __Discuss__.**|Add the subject for the discussion and add participants that have access to the event record. Include a brief message for the participants and select **Start discussion**.|
    |**Select __Generate MS Word__.**|Generate a report of the BIA, BCP, exercise, or crisis record in Microsoft Word format. The Microsoft Word copy of the event record is successfully generated that you can download.|
    |**Select __Generate PDF__.**|Generate a PDF of the event. The PDF of the event record is successfully generated that you can download. In the Impact Assessments section of the PDF, details of the Smart assessment are covered, including questions and answers for RPO and RTO in a tabular format, along with dependencies, contributors, and attachments.|
    |**Select __360º view__.**|Generate 360º relationships for the event. A graphical presentation of the event and its relationships is displayed. Refresh the planned order for the recovery task.|
    |**Select __Delete__.**|Delete the event record. A warning message is displayed that deleting the record will result in an automatic deletion of related records, which may also cause a cascade of additional records to be deleted.|

14. View your Event group's pending tasks and Event owner's assigned items in the My tasks page.

15. Review and confirm the group ownership, issue details, and collaboration thread details for the event in separate sections of the PDF and Microsoft Word reports.

    For information on the collaboration block in Microsoft Word and PDFs, see [Create a collaboration thread in an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/comp-email-collab-thread-event.md). For information on Microsoft Word template with collaboration block, see [Update the Word template with a collaboration block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-collaboration-block-docudesigner.md).

16. Select **Save**.

    The event is saved in the **Pending** state.


-   **[Create Exercise Event form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-exercise-event-ref-form.md)**  
Use the Create Exercise Event form in BCM UIB Workspace to add details about an Exercise event.

**Parent Topic:**[Structured workflows for Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/performing-tasks-to-manage-exercise-events.md)

**Related topics**  


[My tasks page view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/my-tasks-page-uib-ws.md)

[Group ownership in BIA, plan, and event records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/group-ownership-bias.md)

[Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/managing-issues-in-bcm.md)

