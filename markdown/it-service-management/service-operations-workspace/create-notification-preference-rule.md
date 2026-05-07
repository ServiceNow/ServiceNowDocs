---
title: Create notification preference rule
description: Define your preferred notification methods and delivery channels for receiving alerts whenever an escalation ticket is raised.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring On-Call Scheduling in Service Operations Workspace, On-Call Scheduling in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Create notification preference rule

Define your preferred notification methods and delivery channels for receiving alerts whenever an escalation ticket is raised.

## Before you begin

Get an overview of how to add delivery channels and notification preferences in this video.

Create notification preference rule and delivery channels

Role required: itil, rota\_manager, rota\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operation Workspace**.

2.  Select the **Schedule** icon.

3.  On **Schedules** page, select **On-call notification preferences** tab.

4.  To define your preferred notification, select **Create new** and provide the following details:

    -   Rule name
    -   Select **Define active days and hours** to customise the rule with the following details:

        -   All-day selection box
        -   From and Until
        -   Active days detail
        -   Active days
        -   Notification attempt
        ![Create notification preferences form](../image/crete_notification_preference_sow.png)

    -   Select **Use preferred schedule** to reuse an existing schedule and provide required details.
    -   In **Notification Attempts**, select **Add new** and select your preferred methods from the following:
        -   Slack
        -   MS Teams
        -   Email IDs
5.  Select **Save**.


-   **[Edit On-call team preference using Teams menu](oncall-team-preference-tab-in-teams.md)**  
Use the **Teams** menu to edit the on-call preferences for a selected team.
-   **[Manage delivery channel](work-on-a-notification-preference-rule-in-sow.md)**  
Add, edit, and delete delivery channels for notification preference rules in .

**Parent Topic:**[Configuring On-Call Scheduling in Service Operations Workspace](configuring-oncall-scheduling-sow.md)

