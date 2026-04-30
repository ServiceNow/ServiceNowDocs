---
title: Configure the kiosk position and map settings
description: Configure the kiosk position and camera position on the map.
locale: en-US
release: yokohama
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with Kiosk Indoor Mapping, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Configure the kiosk position and map settings

Configure the kiosk position and camera position on the map.

## Before you begin

Create a kiosk configuration to use for the kiosk indoor mapping feature. For more information about creating a kiosk configuration, see [Create a kiosk configuration](../../workplace-services-kiosk/task/create-kiosk-device-config.md).

Role required: sn\_wsd\_indoor\_map.admin and sn\_wsd\_central.workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

2.  Select the Kiosk Indoor Mapping icon \(![Kiosk Indoor Mapping icon.](../images/kiosk-indoor-mapping-icon.png)\).

3.  On the Kiosk Map Configurations list, select the record that you want to configure.

    For more information about creating a kiosk configuration, see [Create a kiosk configuration](../../workplace-services-kiosk/task/create-kiosk-device-config.md).

    The **Map configuration** tab is open by default.

4.  On the Kiosk Placement pane, select **Place Kiosk on Map**, then select a position on the map.

5.  On the Kiosk Placement pane, select a view type for the map.

6.  Enter a kiosk title to be displayed to the kiosk users.

7.  Select **Save Placement**.

    The kiosk placement is saved on the map. You can edit the placement or remove the kiosk from the map.

8.  Select the Map Settings icon.

9.  Select **Edit position**, then move the map to set the default camera position.

    You can also enter values in the fields to set the camera position.From Workplace Services Kiosk version 1.4.3, you can enter decimal values for the camera position.

    |Field|Value Range|
    |-----|-----------|
    |Default Zoom|16 to 23|
    |Default Bearing|-180 to 180|
    |Default Pitch|0 to 60|

10. Select **Confirm**, then select **Save Configuration**.


## Result

The kiosk position and map settings are saved in the kiosk configuration.

If you get the `Map can't be initialized` error on the Map configuration tab, try any of the following actions:

-   Ensure that the kiosk location matches the location of the map that you want to use.
-   Provide the view type permissions to the user who must have access to kiosk indoor mapping.
-   Navigate to **All** &gt; **Indoor Mapping** &gt; **View types**
    -   Ensure that the **Kiosk** view type is active.
    -   If the **Kiosk** view type is not available, ensure that you have installed [Workplace Services Kiosk](../../workplace-services-kiosk/concept/workplace-services-kiosk.md).

**Parent Topic:**[Working with Kiosk Indoor Mapping](../concept/working-kiosk-ind-map.md)

**Previous topic:**[Configure map features for kiosk](config-map-features.md)

**Next topic:**[Configure a module for kiosk indoor mapping](config-kiosk-ind-map-module.md)

