---
title: Create an escalation trigger for an SRM team
description: Define conditions that trigger a team's escalation policy in Service Reliability Management \(SRM\).
locale: en-US
release: yokohama
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up escalation policies for your team in SRM, Working with SRM teams, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Create an escalation trigger for an SRM team

Define conditions that trigger a team's escalation policy in Service Reliability Management \(SRM\).

## Before you begin

Role required: srm\_manager or srm\_admin

## About this task

This procedure shows how to create escalation triggers in SRM. If your organization manages on-call scheduling using IT Service Management \(ITSM\), you can also use ITSM On-Call Scheduling to define escalation triggers. See [Create an escalation trigger rule](https://www.servicenow.com/docs/access?context=create-trigger-rule-oncall&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information. While that procedure lists ITSM roles, SRM users only need the srm\_manager or srm\_admin role to complete the task.

For a broader overview of escalation processes in ITSM, see [Designing an escalation process](https://www.servicenow.com/docs/access?context=designing-escalation-process-oncall&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

**Note:** The following procedure supports trigger conditions based on assignment group changes only. For trigger conditions based on other fields, a workaround is required. Contact ServiceNow Support about accessing KB1702299 in the ServiceNow Support Knowledge Base.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select the **Teams** icon \(![Teams.](../image/icon-sr-teams.png)\).

3.  Select your team and then select the **Escalation triggers and policies** tab.

4.  Under **Escalation triggers** in the panel, select **Create trigger**.

5.  On the Escalation trigger form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Escalation trigger name|Name of the trigger.|
    |Order|Order of execution. When there are multiple escalation triggers in a team, the one with smaller order number is checked first.|
    |Active|Option to activate or deactivate the trigger.|
    |Conditions|Conditions for the trigger. Select a table and condition set. When conditions are met, escalation triggers are triggered for shifts in SRM team.|

6.  Select **Save**.

    You can also add support for escalation triggers to run on alerts instead of incidents. You can add up to 5000 events or 250 alerts per second stream. To add the on-call for alerts support, either run the XML on trigger\_rule\_table\_cfg trigger table or create the record manually in the Trigger Rule Table Config page.


**Parent Topic:**[Set up escalation policies for your team in SRM](sr-create-escalation-policies.md)

