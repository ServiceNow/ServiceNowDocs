---
title: Escalation triggers in SRM
description: Trigger an escalation policy for the associated team.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up escalation policies for your team in SRM, Working with SRM teams, Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Escalation triggers in SRM

Trigger an escalation policy for the associated team.

## Before you begin

Role required: Manager or Administrator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  From the left navigation pane, select the teams icon \(![Teams.](../image/icon-sr-teams.png)\).

3.  Select the **Escalation triggers and policies** tab.

4.  Under **Escalation triggers** in the left panel, select **Create trigger**.

5.  On the Escalation trigger form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Escalation trigger name|Name of the trigger.|
    |Active|Option to activate or deactivate the trigger.|
    |Order|Order of execution. When there are multiple escalation triggers in a team, the one with smaller order number is checked first.|
    |Conditions|Conditions for the trigger. Select a table and condition set. When conditions are met, escalation triggers are triggered for shifts in SRM team.|

6.  Select **Save changes**.

    **Note:** When a new or updated record is created for a team with an escalation trigger that matches the record's condition \(for example, priority 1\), the escalation trigger should activate, and the team's escalation policy should take effect. However, this functionality is not available.

    You can also add support for escalation triggers to run on alerts, if needed \(instead of incidents\). You can add up to 5000 events or 250 alerts per second stream. To add the on-call for alerts support, either run the XML on trigger\_rule\_table\_cfg trigger table or create the record manually in the Trigger Rule Table Config page.


**Parent Topic:**[Set up escalation policies for your team in SRM](sr-create-escalation-policies.md)

