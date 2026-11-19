---
title: Use guided selling on an opportunity
description: Track stage exit criteria, complete playbook activities, and manage deal-related actions on an opportunity to advance deals through the sales cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/use-guided-selling-opportunity.html
release: zurich
topic_type: task
last_updated: "2026-07-06"
reading_time_minutes: 2
keywords: [guided selling, action center, playbook, stage exit criteria, opportunity]
breadcrumb: [Opportunity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Use guided selling on an opportunity

Track stage exit criteria, complete playbook activities, and manage deal-related actions on an opportunity to advance deals through the sales cycle.

## Before you begin

Guided selling activities must be configured in a playbook for the opportunity stages in your sales cycle. For more information, see [Configure guided selling activities in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/configure-guided-selling-exit-criteria.md).

Role required: sn\_opty\_mgmt\_core.sales\_agent

## About this task

The opportunity **Overview** tab displays the Action Center and playbook activities for the current stage. The Action Center consolidates tasks, meetings, touchpoints, and stage guidance in one panel and updates in real time as you complete actions. You must complete all activities for the current stage before you can advance the opportunity to the next stage.

**Note:** With sn\_opty\_mgmt\_core.opportunity\_stage\_guidance\_override role, the users can bypass the stage validations and can move the Opportunity stage forward without completing the mandatory activities configured in the stage.

The sn\_opty\_mgmt\_core.opportunity\_admin role can move the stage of Opportunity forward bypassing all validations.

## Procedure

1.  In the CSM Configurable Workspace, navigate to **Opportunity** &gt; **All** and select the opportunity to open.

2.  Select the **Overview** tab.

    The Action Center panel displays the playbook activities for the current stage. Each activity shows its completion status.

3.  Review the activities in the Action Center and complete each required action.

    Depending on the activity type, you may need to:

    -   Complete a task linked to the opportunity.
    -   Update a required field on the opportunity record.
    -   Add a related record such as a contact or team member.
    -   Answer a questionnaire or acknowledge an instruction.
    The Action Center updates in real time as you complete each action.

4.  Select a playbook activity card in the Action Center to view guidance for the current stage.

    The inline compact playbook view opens within the **Overview** tab. You can review general guidelines and recommended actions for the stage without leaving the opportunity workspace.

5.  Advance the opportunity to the next stage by updating the **Stage** field on the opportunity record.

    If any activities are incomplete, the system doesn't allow the stage change and highlights the outstanding actions in the Action Center.


## Result

The opportunity advances to the next stage. The Action Center refreshes to display the playbook activities for the new stage.

**Parent Topic:**[Using Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/opportunity-mgmt-using.md)

**Related topics**  


[Guided selling on opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/explore-guided-selling.md)

[Configure guided selling activities in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/configure-guided-selling-exit-criteria.md)

[Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/opportunity-management.md)

