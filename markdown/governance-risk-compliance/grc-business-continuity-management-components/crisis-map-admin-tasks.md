---
title: Setup for Crisis map
description: The BCM administrator can perform the administrative tasks to set up the Crisis map interface.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Setup for Crisis map

The BCM administrator can perform the administrative tasks to set up the Crisis map interface.

The BCM administrator performs the administrative tasks to set up the threat alerts and data feeds in Crisis map. The administrative tasks are displayed under **Administration** in the **Threat and Alert Data Feeds** module as shown in the following example.

**Note:** Prior to enabling the Crisis Map feature, ensure that you have purchased and set up Google Maps API.

![Threat alerts and data feeds.](../image/threat-alert-data-feeds-admin-tasks.png)

If you have the BCM administrator role, perform the following administrative tasks to set up the Crisis map:

-   **Scheduled Imports**: Configure a Scheduled Data Imports record for the Crisis map application. For more information, see [Configure Scheduled Data Imports records](../task/sched-data-imports-crisis-map-uib-ws.md).
-   **Resource Configuration**: Configure a Resource Configuration record for the Crisis map application. For more information, see [Configure Resource Configuration records](../task/conf-resource-for-crisis-map-uib-ws.md).
-   **Alert Rules**: Configure an alert rule in Crisis map so that you can specify the conditions under which a feed can be displayed in the dashboard as an alert. For more information, see [Configure alert rules](../task/conf-alert-rule-uib-ws.md).
-   **Alert Actions**: Configure an alert action in UIB Workspace for the Crisis map application. For more information, see [Configure alert actions](../task/configure-alert-action-uib-ws.md).

-   **[Customization properties for Google Maps](crisis-map-customization-properties-for-g-maps.md)**  
The Crisis map application users can configure the customization properties for Google Maps in the **Google Maps Properties** module.
-   **[Google Maps APIs used in Fam-map component](../reference/g-maps-api-in-fam-map-component.md)**  
The Fam-map component in Crisis map utilizes various Google Maps APIs to provide interactive mapping functionalities. This section lists the Google Maps APIs that are integrated into the Fam-map component, along with their usage information.
-   **[Configure Scheduled Data Imports records](../task/sched-data-imports-crisis-map-uib-ws.md)**  
Configure a Scheduled Data Imports record for the Crisis map application. You can then manage your subscriptions to the threat feeds from an internal or external source in the BCM Configurable Workspace.
-   **[Configure Resource Configuration records](../task/conf-resource-for-crisis-map-uib-ws.md)**  
Configure a Resource Configuration record for the Crisis map application in UIB Workspace. You can then plot the assets of your organization on the Crisis map. The assets can be locations, employees, datacenters, suppliers, and others. Configuring resources is also required as an input to set up the alert rules.
-   **[Configure alert rules](../task/conf-alert-rule-uib-ws.md)**  
Configure an alert rule in the Crisis map so that you can define when a feed is displayed as an alert on the dashboard. You can also specify the conditions under which an alert is no longer valid and dismiss it from the dashboard.
-   **[Configure alert actions](../task/configure-alert-action-uib-ws.md)**  
Configure an alert action from the Crisis map interface in the BCM Configurable Workspace.

**Parent Topic:**[Configuring Business Continuity Management](configuring-business-continuity-management.md)

