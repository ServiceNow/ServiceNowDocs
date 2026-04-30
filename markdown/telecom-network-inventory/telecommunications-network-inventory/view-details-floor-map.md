---
title: View details of floor map
description: Use the floor map in the Telecommunications Network Inventory application to view placement of network assets on a datacenter floor and their details such as asset specific and operational data.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-06-04"
reading_time_minutes: 4
breadcrumb: [Using the floor map, Using Network visualization view, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# View details of floor map

Use the floor map in the Telecommunications Network Inventory application to view placement of network assets on a datacenter floor and their details such as asset specific and operational data.

## Before you begin

-   Make sure that a datacenter record is mapped to the campus whose details you want to view.
-   Make sure that you have installed the Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) and Customer Service Problem Management \(CSPM\) \(sn\_sprb\_mgmt\) plugin to view alert and incident details.
-   Role required: sn\_ni\_core.dc\_ops\_agent

## About this task

Use the floor map to view the following:

-   Details of the places on the floor.
-   View alert information
-   Visualize a rack
-   View floor and rack health information
-   View operational metrics

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the blue hub icon ![Blue Hub Icon.](../image/icon-blue-hub.png).

    The Network viewer window is displayed.

3.  Select the **Floor map** tab.

4.  In the **Choose location** field, select your Site, Building, and Floor.

    The floor map appears.

5.  View the details of the floor map by performing the following actions on the map pane.

<table id="choicetable_qtk_fr3_yxb"><thead><tr><th align="left" id="d40744e140">

Action

</th><th align="left" id="d40744e143">

Details

</th></tr></thead><tbody><tr><td id="d40744e149">

**View the details of floor**

</td><td>

Select an empty space on the floor. You can view the following details on the details pane.-   **Campus**

Campus name

-   **Building**

Building name

-   **Floor**

Floor name

-   **Floor area**

Total floor area in square feet

-   **Total cabinets**

Total count of cabinets on the floor

-   **Total equipment**

Total count of equipment on the floor

-   **Total interfaces**

Total count of interfaces on the floor

-   **Available interfaces**

Available count of interfaces on the floor

-   **Connections**

Count of logical connections and power circuits related to datacenter

</td></tr><tr><td id="d40744e242">

**View the details of a place**

</td><td>

Select a place on the map pane. The selected place is highlighted on map pane. You can view the place details on the details pane. If the place is mapped to a Configuration Item \(CI\), then you can see the CI-specific details.

</td></tr><tr><td id="d40744e254">

**View the alert information**

</td><td>

Select the alert icon \(![Alert Icon.](../image/icon-alert-floor-map.png)\) on a place in the map pane. On the details pane, you can view the following information about the CI that is mapped on that place.-   Active alerts
-   Active events
-   Active change requests
You can also select the green lightening bolt icon \(![Green Lightening Bolt Icon.](../image/icon-green-lightening-bolt.png)\) to view the alert information.

</td></tr><tr><td id="d40744e287">

**Visualize a rack**

</td><td>

Select a rack CI on the map pane. The Rack view opens. Do the following on the Rack view.-   To open the rack record, select **Open rack**.
-   To view the back of the rack, select **View rear panel**.


</td></tr><tr><td id="d40744e311">

**View floor and rack health information**

</td><td>

Select an empty space on the map pane to view the following floor health information on the details pane.

-   Cabinet capacity
-   Temperature
-   Power usage
-   Humidity
 Select a rack on the map pane to view the following health information.

-   Rack usage
-   Temperature
-   Power usage
-   Humidity
 Select the more option icon \(![More Options Icon.](../image/icon-more-option.png)\) in the health section, and select **Open metrics** to view the metric values.

</td></tr><tr><td id="d40744e366">

**View operational metrics**

</td><td>

Overlays on a floor map are visual indicators displayed directly on a datacenter's floor map. These indicators show real-time or past operational metrics.

 1.  In the **View By** field, select an overlay. The following overlays are available.
    -   Temperature
    -   Power
    -   RU utilization
2.  Select the time duration that you want. The default time duration is set as **Recent**. The following time durations are available.
    -   Recent
    -   Past 3 hours
    -   Past 6 hours
    -   Past 12 hours
 For example, select **Temperature** overlay and **Past 3 hours** time duration.The floor map updates with the colors according to the map legend. If the current time is 9:00 PM, the map shows the average of operational values from 6:00 PM to 9:00 PM.

 To disable overlays, select **None** in the **View By** field.

 **Note:**

-   You can only use the **Recent** time series option with the **RU utilization** overlay.
-   If no metric data available, system shows an error message **No metrics found for the specified duration**.
 To deselect overlay, select **None** in the **View By** field.

</td></tr><tr><td id="d40744e467">

**View floor map related to a company account**

</td><td>

In the **Filter By Accounts** field, select an account. The map highlights the CIs related to that company account in bluish green color. CIs related to other accounts are grayed out. You can also select more than one account.

</td></tr><tr><td id="d40744e482">

**Open a record from details pane**

</td><td>

1.  On the details pane, select the more options icon \(![More Options Icon.](../image/icon-more-option.png)\) of a card. The card can be a place, CI, incident, alert, or change request.
2.  Select **Open record**.
 The corresponding record opens. To open a rack record, you can also select **Open rack** on the Rack view.

</td></tr></tbody>
</table>
**Parent Topic:**[Using the floor map](../concept/using-floor-map.md)

**Related topics**  


[Visualization of floor map](../concept/visualization-floor-maps.md)

[Configuring overlays on floor map](../concept/configure-overlays-floor-map.md)

