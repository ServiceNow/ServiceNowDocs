---
title: Find resources with indoor positioning
description: When indoor positioning is enabled on your device, you can get step-by-step interactive directions to resources in a building that has been mapped for this feature.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Indoor positioning, Indoor Wayfinding and reservations, Using the mobile apps, Mobile Platform]
---

# Find resources with indoor positioning

When indoor positioning is enabled on your device, you can get step-by-step interactive directions to resources in a building that has been mapped for this feature.

## Before you begin

Your ServiceNow instance admin must configure indoor positioning before you can enable it on your device.

Role required: none

## Procedure

1.  Open your ServiceNow mobile app on your device.

2.  Search for a resource.

    For example, you can search for a person, a conference room, or other indoor resource.

3.  When you’ve located the resource, select **Get directions**.

    ![Mobile app screen showing the 'Get directions' button](../image/ind-posit-select-get-directions.png)

    The map shows where the person or resource is on the map. The mobile app prompts for whether the device can use your location.

4.  Respond to the request to use your location.

    Choose from the following options.

    |Location option|Description|
    |---------------|-----------|
    |Allow Once|Your location appears on the map with an icon \(![Blue dot indicating user's position on the indoor wayfinding map](../image/blue-dot-icon.png)\). This permission only lasts for this session. The next time you search for an asset or person, you're prompted to permit the mobile app to use your location again.|
    |Allow While Using the App|Your location appears on the map with an icon \(![Blue dot indicating user's position on the indoor wayfinding map](../image/blue-dot-icon.png)\). This permission persists each time you use the app. The next time you search for an asset or person, you aren't prompted to permit the mobile app to use your location.|
    |Don't Allow|No icon shows your location on the map.|

5.  Depending on whether you allowed the mobile app to use your location, use the following steps.

<table id="choicetable_sht_lj2_zvb"><thead><tr><th align="left" id="d100861e174">

Option

</th><th align="left" id="d100861e177">

Procedure

</th></tr></thead><tbody><tr><td id="d100861e183">

**If you allowed the mobile app to use your location**

</td><td>

1.  Select **Start directions**.

Your path to the person or resource appears on the map.

2.  Select **View steps**.

Follow the path and your position is updated automatically. Directions appear on the top banner, which indicate the way to turn \(left or right\) and if you must climb stairs. In addition, the distance, time left to travel to the resource, and expected arrival time also appear on your device. This information is updated in real time.

</td></tr><tr><td id="d100861e215">

**If you didn't allow the mobile app to use your location**

</td><td>

1.  Select **Choose start location**.

Follow the prompts on the screen to choose your start location.

2.  Select **Save** to save your start location.
3.  Select **View steps**.

The route to the person or resource you searched for appears on the map. The expected distance, travel time, and arrival time also appear in the mobile app.

</td></tr></tbody>
</table>6.  When you arrive at your destination, select **End Directions**.


