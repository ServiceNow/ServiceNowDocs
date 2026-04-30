---
title: Manually create SRM tags
description: Tags help you classify and categorize data, or otherwise add information there isn't a field for. SRM imports tags and attaches them to services, alerts, and incidents. However, you can also create tags manually.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SRM interface, Get started with Service Reliability Management, Exploring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Manually create SRM tags

Tags help you classify and categorize data, or otherwise add information there isn't a field for. SRM imports tags and attaches them to services, alerts, and incidents. However, you can also create tags manually.

## Before you begin

Role required: Responder, Manager, or Administrator

## About this task

There are two ways that tags can enter the system and attach to an alert or incident. The first is automated but the last one is manual.

-   Imported from a third-party integration such as Datadog.
-   Using the tag icon in the header of a Service, Alert or Incident.
-   Added using the **Modify field values** action in an automation rule.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  In the left navigation pane, select **Services**,**Alerts**, or **Incidents**.

3.  Open a service, alert, or incident.

4.  In the header, use the Tag icon ![Tag icon](../image/icon-sr-tag.png) to add tags.

5.  Enter your tag in the pop-up window.

    Your tag is saved and appears below the Add Tag box along with any other tags already applied.

    ![The Tags box showing a created tag](../image/sr-tag-added.png)

6.  Select anywhere in the form to close the pop-up.

    **Note:**

    Tags are also shown under the description in the alert and incident list views.

    Adding tags to an alert is not considered an update, so no automations run when you add a tag.


**Parent Topic:**[SRM interface](../concept/sr-navigate-interface.md)

