---
title: Use guided selling on an opportunity
description: Track stage exit criteria, complete playbook activities, and manage deal-related actions on an opportunity to advance deals through the sales cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/use-guided-selling-opportunity.html
release: australia
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 3
keywords: [guided selling, action center, playbook, stage exit criteria, opportunity]
breadcrumb: [Opportunity Management, Sales automation apps, Use, Sales Customer Relationship Management]
---

# Use guided selling on an opportunity

Track stage exit criteria, complete playbook activities, and manage deal-related actions on an opportunity to advance deals through the sales cycle.

## Before you begin

Guided selling activities must be configured in a playbook for the opportunity stages in your sales cycle. For more information, see [Configure guided selling activities in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-guided-selling-exit-criteria.md).

Role required: sn\_opty\_mgmt\_core.sales\_agent

## About this task

The opportunity **Overview** tab displays the Action Center and playbook activities for the current stage. The Action Center consolidates tasks, meetings, touchpoints, and stage guidance in one panel and updates in real time as you complete actions. You must complete all activities for the current stage before you can advance the opportunity to the next stage.

**Note:** With sn\_opty\_mgmt\_core.opportunity\_stage\_guidance\_override role, the users can bypass the stage validations and can move the Opportunity stage forward without completing the mandatory activities configured in the stage.

The sn\_opty\_mgmt\_core.opportunity\_admin role can move the stage of Opportunity forward bypassing all validations.

## Procedure

1.  In the CSM Configurable Workspace, navigate to **Opportunity** &gt; **All** and select the opportunity to open.

2.  Select the **Overview** tab.

    The Action Center panel displays the playbook activities for the current stage. Each activity shows its completion status.

    -   When the opportunity has no records to display in the Action Center, an empty state appears with an action to create an opportunity task.
    -   The created task is added to the **All** and **Tasks** filters without a page refresh.
    -   The **Stage guidance** filter is hidden when no playbook is active or when all playbook activities are complete.
3.  Review the activities in the Action Center and complete each required action.

    Depending on the activity type, you may need to:

    -   Complete a task linked to the opportunity.
    -   Update a required field on the opportunity record.
    -   Add a related record such as a contact or team member.
    -   Answer a questionnaire or acknowledge an instruction.
    -   Complete a quote task associated with the primary quote for the opportunity. The quote task card displays the related quote record as a link that opens the quote in a new workspace tab.
    The Action Center updates in real time as you complete each action.

4.  Select a playbook activity card in the Action Center to view guidance for the current stage.

    The inline compact playbook view opens within the **Overview** tab. You can review general guidelines and recommended actions for the stage without leaving the opportunity workspace.

5.  Advance the opportunity to the next stage by updating the **Stage** field on the opportunity record.

    If any activities are incomplete, the system doesn't allow the stage change and highlights the outstanding actions in the Action Center.

    If your admin enabled closed stage reason enforcement, you must complete the following fields before you can change the stage:

    -   For Closed Won stage: **Win reason** and **Outcome notes**
    -   For Closed Lost stage: **Loss reason**, **Lost to**, and **Outcome notes**
    If a required field is empty, the system prevents the stage change and displays a message that names the mandatory field and the target stage.


## Result

The opportunity advances to the next stage. The Action Center refreshes to display the playbook activities for the new stage.

**Parent Topic:**[Using Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-mgmt-using.md)

**Related topics**  


[Guided selling on opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-guided-selling.md)

[Configure guided selling activities in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-guided-selling-exit-criteria.md)

[Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management.md)

