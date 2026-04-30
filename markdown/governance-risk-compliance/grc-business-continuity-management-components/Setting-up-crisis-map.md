---
title: Setting up the crisis map
description: Before you integrate the crisis management map with the geographical locations of your assets, there are certain configurations that you must do to display the active alerts in the crisis map.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Setting up the crisis map

Before you integrate the crisis management map with the geographical locations of your assets, there are certain configurations that you must do to display the active alerts in the crisis map.

## Understanding feed, alert, and event

-   **Feed**

    A feed is news content updated frequently and provided on a world-wide website. You can subscribe to a news feed by manually entering the web address or URL of the feed channel in the **Web** field of the Feed form.

-   **Alert**

    An alert is a notification that reports an incident happened at a particular place and time. First, an incident or an event reportedly happens. Then, the alert triggers a notification that reports or notifies the incident to the concerned people to take an action.

-   **Event**

    Based on the severity of the alerts, you can take actions by just notifying the stakeholders of the incident that happened or declare a crisis event. An event can become a crisis event if it disrupts the business operations. In such a case, you can run the [Crisis Management workflow](bcm-recovery-exercise-management.md) to activate the business continuity and disaster recovery plans for the locations impacted by the event.


## Setup steps to integrate crisis map

You require these configurations for the threat and alert feeds to show up in the crisis map visualization.

-   To search locations on the crisis map, [set up the system property](../task/crisis-map-place-api-configuration.md).
-   To manage your threat feed subscriptions sourced internally and externally, [configure scheduled data imports](../task/crisis-map-scheduled-data-imports.md).
-   To plot your organization's assets or resources on the crisis map, [configure the resources](../task/crisis-map-configure-resource.md).
-   To specify the conditions under which a feed should bubble up as an alert on the crisis map, [configure alert rules](../task/crisis-map-alert-configuration.md).
-   Finally, to act on a critical alert from the crisis map dashboard, [configure an alert action](../task/crisis-map-alert-actions.md).

