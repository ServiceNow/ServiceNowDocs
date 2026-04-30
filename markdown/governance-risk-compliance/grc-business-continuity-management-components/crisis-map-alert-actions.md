---
title: Configure an alert action
description: The alert actions are the follow-up actions that you can perform from the crisis map dashboard.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure search for places in crisis map, Setting up the crisis map, Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure an alert action

The alert actions are the follow-up actions that you can perform from the crisis map dashboard.

## Before you begin

Role required: System administrator

## Procedure

1.  Navigate to **Threat and Alert Data Feeds** &gt; **Administration** &gt; **Alert Actions**.

    These actions are available within the base system.

    |Name|Description|
    |----|-----------|
    |Notify|Used to send email notifications to stakeholders and the asset managers that are within the impact radius.|
    |Declare Crisis|Used to declare a combination of alert and critical assets as a crisis event.|

2.  To add a new alert action, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Title|Title of the alert action.|
    |Description|Detailed description of the alert action.|
    |Name|Name of the action in the crisis map dashboard.|
    |Action name|Unique name for the alert action.|
    |Run once|Option to indicate the execution of the action one or more times from the dashboard.|
    |Type|Type of action to be executed. It can be a task, script, or flow.|
    |Task type|Task type used for the action.|
    |Application|Read-only field. The field is used as a flag to filter the items relevant to crisis management from a common list of actions.|
    |Active|Option to indicate that the alert action is active.|
    |Order|Display order to be followed on the dashboard.|
    |Run automatically|Option for enabling the action to be executed automatically based on a condition.|
    |Roles|User roles who can execute the task successfully.|
    |Display Fields|Fields to be displayed in the response actions after the actions are executed.|
    |Condition|Conditions to execute the actions.|
    |Task script|Task script to be executed when the user clicks the action control on the dashboard.|

4.  Click **Submit**.


**Parent Topic:**[Configure search for places in crisis map](crisis-map-place-api-configuration.md)

