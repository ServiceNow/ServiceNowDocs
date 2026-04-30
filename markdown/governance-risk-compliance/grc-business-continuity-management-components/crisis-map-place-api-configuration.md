---
title: Configure search for places in crisis map
description: Set the system property to manage searching places on the crisis map.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up the crisis map, Crisis Management map, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure search for places in crisis map

Set the system property to manage searching places on the crisis map.

## Before you begin

Role required: Administrator

## About this task

To enable crisis map functionality in the GRC: Crisis Map application, you must set up Google maps. For more information, see [Set up Google Maps API](https://www.servicenow.com/docs/access?context=set-up-google-maps-api&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

**Note:** Prior to enabling the Crisis Map feature, confirm that you have purchased and set up Google Maps API.

## Procedure

1.  To open the System Properties table \[sys\_properties\], enter sys\_properties.list in the left pane of the application navigation filter.

2.  Search for sn\_bcm\_map.use\_google\_places\_lib in the **Name** column.

3.  To search places in the Google map, set the value to **True** in the **Value** column for the sn\_bcm\_map.use\_google\_places\_lib system property.


-   **[Configure scheduled data imports for crisis map](crisis-map-scheduled-data-imports.md)**  
Manage your subscriptions to threat feeds from internal or external sources by configuring scheduled data imports.
-   **[Configure a resource for crisis map](crisis-map-configure-resource.md)**  
Configure resources to plot the organization's assets on the crisis map. The assets can be locations, employees, data centers, suppliers, and others. Configuring resources is also required as an input to set up alert rules.
-   **[Configure alert rules to display alerts in crisis map](crisis-map-alert-configuration.md)**  
Set alert rules to specify conditions under which a feed has to be bubbled up and displayed in the dashboard as an alert. You can also specify the conditions under which an alert is no longer valid and dismiss it from the dashboard.
-   **[Configure an alert action](crisis-map-alert-actions.md)**  
The alert actions are the follow-up actions that you can perform from the crisis map dashboard.

**Parent Topic:**[Setting up the crisis map](../concept/Setting-up-crisis-map.md)

