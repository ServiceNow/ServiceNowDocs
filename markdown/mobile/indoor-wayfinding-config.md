---
title: Indoor Wayfinding configuration
description: Indoor Wayfinding enables ServiceNow mobile app users to locate an asset, such as a desk or meeting room, on a map and then reserve it.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Indoor Wayfinding configuration

Indoor Wayfinding enables ServiceNow mobile app users to locate an asset, such as a desk or meeting room, on a map and then reserve it.

Indoor Wayfinding involves an indoor map that is rendered on a custom map screen. Reservations are rendered as a custom map input on the indoor map. Indoor Wayfinding and reservations are part of Workplace Service Delivery for Mobile [Indoor Mapping](https://www.servicenow.com/docs/access?context=Indoor-mapping&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

To use this feature on your instance, you must install and enable the following ServiceNow Store apps and plugins:

-   Required: Indoor Mapping \(sn\_map\_core\)
-   Because the following plugins eliminate the need to hand-configure Indoor Mapping, admins should install and enable the following plugins as well:

    -   Workplace Service Delivery for Mobile \(sn\_wsd\_mobile\)
    -   Workplace Core \(sn\_wsd\_core\)
    -   Workplace Space Mapping \(sn\_wsd\_space\_map\)
    -   Workplace Reservation Management \(sn\_wsd\_rsv\)
    -   Workplace Indoor Mapping \(sn\_wsd\_indoor\_map\)

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) for information about requesting and installing apps. For more information, see [Install Workplace Indoor Mapping dependent plugins](https://www.servicenow.com/docs/access?context=wsm-install-ind-mapping-plugins&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)

After installing and activating these plugins, you must do the following configurations:

-   [Configure Indoor Mapping](https://www.servicenow.com/docs/access?context=configure-ind-mapping&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) , which explains how to configure the following parts of Indoor Mapping:
    -   Install the Indoor Mapping application.
    -   Create a campus with buildings and floors.
    -   Upload and import the AutoCAD floor plans for floors that you have created.
    -   Upload and import raster floor plan sources.
-   [Configure input form screen inputs](../task/param-screen-config-inputs.md) so that you can add the Custom Map input to an input form screen on your organization's mobile app. Adding this input to your mobile app enables end users to select and view the map. For more information about the Custom Map input type, see [Input form screen attributes for inputs](../reference/parameter-screen-var-attr.md).
-   [Configure a custom map screen to use your provider](https://www.servicenow.com/docs/access?context=create-custom-map-screen&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) .

-   **[Configure indoor positioning](../task/configure-indoor-positioning.md)**  
Indoor positioning enables end users to see their live location on an Indoor Wayfinding map and get guided navigation to their desired destination.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

