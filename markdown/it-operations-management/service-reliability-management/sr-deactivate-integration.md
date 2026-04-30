---
title: Deactivate an integration
description: If you want to temporarily deactivate an integration, move it to an inactive state. When you deactivate integrations, the alerts received via this integration are no longer processed. You might consider disabling an integration if you plan to take a system in maintenance mode and don’t want to receive unnecessary alerts during that time.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Available SRM integrations, Working with SRM integrations, Add a service to SRM, Working with SRM services, Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Deactivate an integration

If you want to temporarily deactivate an integration, move it to an inactive state. When you deactivate integrations, the alerts received via this integration are no longer processed. You might consider disabling an integration if you plan to take a system in maintenance mode and don’t want to receive unnecessary alerts during that time.

## Before you begin

Role required: Responder, Manager, or Administrator

## About this task

Responders and managers can disable any integration they’ve created or was created by their team. An administrator can disable any integration in SRM.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  On the **Services** page \(![Services module icon](../image/icon-sr-services.png)\), select a service.

3.  Select the **Integrations** tab.

<table id="choicetable_p5q_5wj_1zb"><thead><tr><th align="left" id="d324217e97">

Option

</th><th align="left" id="d324217e100">

Steps

</th></tr></thead><tbody><tr><td id="d324217e106">

**From the Integrations tab**

</td><td>

1.  For each active integration you want to deactivate, select the More actions icon ![more actions icon](../image/icon-sr-more-actions-vertical.png).
2.  Select **Deactivate**.


</td></tr><tr><td id="d324217e133">

**In the Integration record**

</td><td>

1.  Select the integration to open the record.
2.  Select **Deactivate**.


</td></tr></tbody>
</table>    **Note:** You can enable an inactive integration and make it available again by Selecting **Activate** from the More actions icon ![more actions icon](../image/icon-sr-more-actions-vertical.png). But, if the service associated with the deactivated integration has been deactivated, you won’t be able to reactivate the integration.


**Parent Topic:**[Available SRM integrations](../concept/sr-builtin-integrations.md)

