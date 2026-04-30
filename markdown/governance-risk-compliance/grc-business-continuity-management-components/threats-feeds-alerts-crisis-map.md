---
title: Crisis map interface
description: You can integrate Crisis map with the BCM application and initiate the response workflows for crisis management. After installing the Crisis map application, you can view the Threat and Alert Data Feeds module in your BCM application instance.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Crisis map interface

You can integrate Crisis map with the BCM application and initiate the response workflows for crisis management. After installing the Crisis map application, you can view the **Threat and Alert Data Feeds** module in your BCM application instance.

## Feeds, alerts, and events in BCM

When you integrate the Crisis map application with the BCM application, you can view and analyze the feeds, alerts, and events from different locations in the Crisis map view.

-   **Feed**

    A feed is news content updated frequently and provided on a worldwide website. You can subscribe to a news feed by manually entering the URL of the feed channel in the **Web** field of the Feed form.

-   **Alert**

    An alert is a notification that reports an incident happened at a particular place and time. First, an incident, or an event reportedly happens. Then, the alert triggers a notification that reports or notifies the incident to the concerned people to take an action.

-   **Event**

    Based on the severity of the alerts, you can take actions such as notifying the stakeholders of the incident or declaring a crisis event. An event can become a crisis event if it disrupts the business operations. For information on the crisis events, see [Crisis map view](crisis-map-uib-ws.md). You can then activate the business continuity plans for the locations that are impacted by the event.


## Threat and Alert Data Feeds module in BCM

The **Threat and Alert Data Feeds** module in BCM displays the following information:

-   **Feeds**
-   **Alerts**
-   **Administration**

The **Threat and Alert Data Feeds** module is shown in the following example.

![Threat alerts and data feeds.](../image/threat-alert-data-feeds-admin-tasks.png)

## Feeds module in BCM

A threat feed is the data intelligence information of a potential or current threat that can pose a danger to an organization. It can disrupt the business routine or disable its business processes. The Crisis map application receives the feeds from third-party sources such as GDAC Feeds and Weather Gov Alerts.

The **Feeds** module in BCM displays the following types of feeds:

-   **Active feeds**
-   **Archived feeds**

A sample view of the active feeds is displayed in the following example.

![Active feeds view.](../image/feeds.png)

You can use the **Personalize List** icon to configure the list columns in the **Feeds** module. For example, you can display the following additional details on the alert:

-   Headline
-   Event
-   Severity
-   Certainty
-   Category
-   Response type
-   Data source
-   Process state

Threat feeds include information about real-time disruptive events as shown in the following sample list:

-   Civil unrest or riots
-   Flood advisory
-   Flood warning
-   Drought area
-   Earthquake
-   Hurricane
-   Wildfire or red flag warnings
-   War or military conflict
-   Volcano eruption

## Alerts module in BCM

An alert is a notification that reports an incident happened at a particular place and time. First, an incident or an event reportedly happens. Then, the alert triggers a notification that reports or notifies the incident to the concerned people to take an action.

The **Alerts** module in BCM displays the following types of feeds:

-   **Active alerts**
-   **Dismissed alerts**
-   **Alert responses**

A sample view of the active alerts is shown in the following example.

![Active alerts.](../image/alerts.png)

You can use the **Personalize List** icon to configure the list columns in the **Alerts** module. For example, you can display the following details on the alert:

-   Title
-   Severity
-   Feed
-   Source
-   Alert rule
-   Impact type
-   Updated

## Administrative tasks in the Threat and Alert Data Feeds module

If you have the BCM administrator role, see [Setup for Crisis map](crisis-map-admin-tasks.md) for information on the setup tasks.

The **Administration** module in BCM displays the following types of feeds:

-   **Scheduled imports**

    To manage your threat feed subscriptions that are sourced internally and externally, you must schedule a data import from the data source at defined intervals. For more information on scheduled imports, see [Configure Scheduled Data Imports records](../task/sched-data-imports-crisis-map-uib-ws.md).

-   **Resource configuration**

    To plot your organization's assets or resources on the Crisis map, you must configure the resources in the application. For more information on resource configuration, see [Configure Resource Configuration records](../task/conf-resource-for-crisis-map-uib-ws.md).

-   **Alert rules**

    To display the feeds as alerts on the Crisis map, configure the alert rules. For more information on alert rules, see [Configure alert rules](../task/conf-alert-rule-uib-ws.md).

-   **Alert actions**

    To act on a critical alert from the Crisis map dashboard, see [Configure alert actions](../task/configure-alert-action-uib-ws.md).


-   For information on the administrative tasks for Crisis map, see [Setup for Crisis map](crisis-map-admin-tasks.md).
-   To search for locations on the Crisis map, you must set the **sn\_bcm\_map.use\_google\_places\_lib** system property. For more information, see [Properties installed with BCM](../reference/properties-bcm.md).

## Crisis map

For information on managing the alerts in Crisis map, see [Structured workflows for Crisis map](crisis-map-collective-tasks.md).

**Parent Topic:**[Exploring Business Continuity Management](exploring-bcm.md)

