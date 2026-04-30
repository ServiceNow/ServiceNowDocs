---
title: Crisis map view
description: When you install the GRC: Crisis map application in your instance, you can view the Crisis map icon in the List view. You can integrate the Crisis map application with BCM and analyze real-time threat alerts from different locations in a map view. You can then take remedial actions and manage the crisis events from Business Continuity Workspace.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [BCM Configurable Workspace, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Crisis map view

When you install the GRC: Crisis map application in your instance, you can view the Crisis map icon in the List view. You can integrate the Crisis map application with BCM and analyze real-time threat alerts from different locations in a map view. You can then take remedial actions and manage the crisis events from Business Continuity Workspace.

## Panels displayed in Crisis map

The Crisis map displays real‑time alerts from integrated threat feeds. Users can search locations, view assets at risk, and respond to alerts. Panels include:

-   Alerts panel for viewing and filtering alerts
-   Map view for exploring impacted locations

    **Note:**

    To enable the search functionality in Crisis map, you must set the **sn\_bcm\_map.use\_google\_places\_lib** system property. For more information on setting the property, see [Properties installed with BCM](../reference/properties-bcm.md).

    To enable Crisis map functionality in the GRC: Crisis map application, you must set up Google maps. For more information, see [Set up Google Maps API](https://www.servicenow.com/docs/access?context=set-up-google-maps-api&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

-   Asset and task details for assessing risk and acting on alerts

A typical view of the Crisis map application is shown in the example.

![Integrating alerts in Crisis map.](../image/crisis-map-uib-ws.png)

For more information on the feeds, alerts, and events in Crisis map, see [Crisis map interface](threats-feeds-alerts-crisis-map.md).

## Tasks for BCM administrators

With the BCM administrator role, perform these setup tasks for Crisis map:

-   Enable threat feed integrations that are provided by the base system.
-   Configure additional threat feeds into the Crisis Management application. These configurations alert the crisis managers about the threats and aids them to take an appropriate action on time.

For more information on the setup tasks for Crisis map, see [Setup for Crisis map](crisis-map-admin-tasks.md) in the configuration section.

## Alerts panel in Crisis map

The **Alerts** panel in Crisis map displays the details:

-   **Search field**: You can search for an alert by using specific keywords.
-   **Show**: You can select this option to display types of alerts:
    -   **Active Alerts**
    -   **Dismissed Alerts**
-   **Sort by**: You can select this option to sort the alerts. Select one of these options:
    -   **Severity**: Select this option to sort and display the alerts based on their severity such as **Extreme** or **Severe**.
    -   **Created**: Select this option to sort and display the alerts based on their creation date.
    -   **Updated**: Select this option to sort and display the alerts based on the date that they were updated on.
    -   **Change sort order**: Select this option to display the alerts in an ascending or descending order.
    -   **Refresh**: Select this option to refresh the alerts display.

You can open or dismiss an alert in the alerts panel. You can also subscribe to an alert by selecting the bell icon as shown in the example.

![Single alert panel.](../image/alerts-panel-crisis-map.png)

## Alerts panel

When you select an alert in the **Alerts** panel, it launches a zoomed-in view with the alert details such as category, event, and so on as shown in the example.

![Focussed view for an alert.](../image/single-alert-zoomed-in-view.png)

You can view details of a single alert in the Alerts panel:

|Field|Description|
|-----|-----------|
|Title of the alert|Title of the alert such as Drought is ongoing in Angola, Congo, DRC.|
|Category|Category of the alert such as Geophysical.|
|Event|Event of the alert such as Drought area.|
|Urgency|Urgency of the alert such as Past.|
|Severity|Severity of the alert such as Extreme.|
|Certainty|Certainty of the alert such as Unknown.|
|Source|Source of the alert such as GDAC.|
|Latitude|Latitude of the alert such as -14.0701845.|
|Longitude|Longitude of the alert such as 13.0958574.|
|Web URL|Web URL of the alert such as Web [https://www.gdacs.org/report.aspx?eventtype=DR&amp;eventid=1014416](https://www.gdacs.org/report.aspx?eventtype=DR&eventid=1014416).|
|Description|Description of the alert such as The Drought alert level is Red.|
|Details tab|
|Assets at risk|Number of assets that are at risk as per locations. You can select the locations to view details such as Name, Contact, Phone, City, Latitude, Longitude, Updated, and so on. The Map view in the right panel shows the zoomed-in location and highlighted area of the alert.|
|Response tasks|Response tasks that are associated with the alert.|
|Activity|Activity related to the alert. It displays the Activity panel and the Compose section where you can add your notes.|
|Suggested actions|Suggested actions for the alert. For example, Notify Stakeholders: Use notifications to deliver important information to impacted stakeholders.|
|Back|Option to navigate to the Alerts panel view.|

## Map view in Crisis map

After you have set up Google maps, you can view the locations of the alerts in the Map view as shown in the example.

![Locations of the alerts in the Map view.](../image/layers-icon-in-map-view-crisis-map.png)

You can view these details in the Map view.

<table id="table_sml_hks_byb"><thead><tr><th>

Icons

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Search Assets and Locations** search bar

</td><td>

Search bar in the Map view. You can enter a location or a datacenter that is impacted by an alert. When you search for a location, a mixed list of your company results with the display value of the records along with their icons, and the Google map pin icons is displayed.

</td></tr><tr><td>

zoom-in and zoom-out

</td><td>

Zoom control buttons to change the zoom level of the map and view specific areas.

</td></tr><tr><td>

Layers icon

</td><td>

Layers icon to select and display the assets such as asset locations, datacenters, or core companies on the map. The layers on the map are displayed as pins on a Google map and they are configurable. All the layer details such as the asset locations, assets, datacenters, and core companies are displayed on the map by their configured icons.

Use the Layers icon to view only the selected or all assets that can be toggled on and off on the map. As a crisis manager, when viewing the active alerts you can make an informed decision by concentrating on a single asset that can be critical at that moment from the rest. The assets are displayed:

-   Locations
-   Web Server
-   Datacenters
-   Vendors

</td></tr><tr><td>

Reset icon

</td><td>

Reset icon to clear the map of all the search results.

</td></tr></tbody>
</table>