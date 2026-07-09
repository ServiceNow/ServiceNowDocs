---
title: Configure guided selling activities in a playbook
description: Define the mandatory activities that sales agents must complete at each opportunity stage by configuring a playbook. Agents cannot advance an opportunity to the next stage until all activities for the current stage are complete.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-guided-selling-exit-criteria.html
release: australia
topic_type: task
last_updated: "2026-07-03"
reading_time_minutes: 3
keywords: [guided selling, playbook, stage exit criteria, opportunity stages, process compliance, mandatory activities]
breadcrumb: [Install and configure Opportunity Management, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Configure guided selling activities in a playbook

Define the mandatory activities that sales agents must complete at each opportunity stage by configuring a playbook. Agents cannot advance an opportunity to the next stage until all activities for the current stage are complete.

## Before you begin

The opportunity stages for your sales cycle must be defined before you configure guided selling activities. For more information, see [Create opportunity stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-opportunity-stages.md).

Role required: sn\_opty\_mgmt\_core.opportunity\_admin

## About this task

Guided selling uses a playbook to define the activities that sales agents must complete at each opportunity stage. When an agent tries to advance an opportunity to the next stage, the system checks whether all activities for the current stage are complete. If any activities are incomplete, the system prevents the stage change and displays the outstanding actions.

The default playbook is configured for opportunities with a sales cycle type of **New Business**. You can configure additional playbooks for other sales cycle types. Each stage in a playbook requires a stage entry automation activity at the start and a stage exit automation activity at the end. Between these two automation activities, you can add any combination of activities based on your business requirements.

The system records activity completion state in the Sales CRM Progression Checkpoint table. When an agent tries to advance an opportunity, the system checks this table to determine whether all activities for the current and preceding stages are complete.

## Procedure

1.  Navigate to **All** &gt; **Playbooks Designer**.

2.  Open the **Sales essentials playbook**.

    The default playbook is triggered when an opportunity is created or updated with a sales cycle type of **New Business**. Configure the trigger condition to match the sales cycle type you want to support.

3.  Add and configure a stage in your playbook, for more information, see [Add and configure a stage in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/add-configure-stage.md).

4.  Select the stage for which you want to configure activities, for more information see [Add and configure an activity in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/add-configure-activity.md).

    The playbook displays each opportunity stage as a lane. Each lane must contain a stage entry automation activity as the first activity in the stage lane and a stage exit automation activity as the last activity in the stage lane.

    This activity creates a record in the Sales CRM Progression Checkpoint table to track activity completion for the stage.

5.  Add the mandatory and optional activities between the stage entry and stage exit automation activities.

    You can use the following default activity definitions to build activities for common use cases.

    |Activity definition|Description|
    |-------------------|-----------|
    |**Required Fields Activity Definition**|Fields specified on the opportunity record must not be empty. Use when agents must complete required fields, such as owner or short description, before advancing.|
    |**Related Records Activity Definition**|One or more related records must exist on the opportunity. Use when agents must add a related record, such as a contact or team member, before advancing.|

    For standard playbook activity types such as questionnaires and instructions, add the **Playbook Activity Event Create** subflow immediately before the activity and the **Playbook Activity Event Update** subflow immediately after it. These subflows track completion state in the Sales CRM Progression Checkpoint table.

6.  Save and activate the playbook.


## Result

The playbook is active. When an opportunity with the configured sales cycle type is created or updated, the playbook triggers and displays the configured activities to the sales agent in the guided selling panel. Agents must complete all activities for a stage before the system allows them to advance the opportunity.

**Related topics**  


[Guided selling on opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-guided-selling.md)

[Create opportunity stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-opportunity-stages.md)

[Install and configure Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-opportunity-mgmt.md)

