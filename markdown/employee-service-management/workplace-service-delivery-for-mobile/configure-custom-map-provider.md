---
title: Configure a custom Map provider
description: Configure map providers so that directions are displayed from one location to another in Workplace Service Delivery for Mobile
locale: en-US
release: yokohama
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Mobile Wayfinding Administration, Configure, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Configure a custom Map provider

Configure map providers so that directions are displayed from one location to another in Workplace Service Delivery for Mobile

## Before you begin

Ensure that you have the following:

-   Workplace Service Delivery for Mobile.
-   Indoor Mapping is the inbuilt map provider with the Workplace Service Delivery application.
-   Mappedin is a third-party map provider.

**Note:** You must configure a map provider for each building individually.

Role required: sn\_wsd\_core.admin

## Procedure

1.  Navigate to **All** &gt; **Space Mapping** &gt; **Mobile Wayfinding Administration** &gt; **Custom Map Provider**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_j1j_pxs_prb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key table

</td><td>

Table entry for which you want to configure the map provider. f you have selected Building \[sn\_wsd\_core\_building\] from the list.

</td></tr><tr><td>

Key

</td><td>

Table entry for which you want to configure the map provider. For example, if you have selected Building \[sn\_wsd\_core\_building\] as your key table. Search for a document on the Select the document dialog box that appears.and select, Building:BuildingC. Search using the lookup list icon \( ![look up list icon](../../workplace-case-mgmt/image/search-icon.png)\).

</td></tr><tr><td>

iOS location provider

</td><td>

Location provider for iOS. Select **Apple** or **Atlas** as the location provider.

</td></tr><tr><td>

Android location provider

</td><td>

Location provider for Android. Select **Atlas**.

</td></tr><tr><td>

Application

</td><td>

Name of the application. This field is auto-generated.Ensure that the application is set to **Workplace Core**.

</td></tr><tr><td>

Map provider

</td><td>

From the drop-down list, select any of the following based on the map provider that you are using: -   **ServiceNow**: For Indoor Mapping.
-   **Mappedin**: For Mappedin


</td></tr><tr><td>

Location provider app id

</td><td>

Location provisioning In IndoorAtlas for indoor positioning or blue dot experience. From your Atlas account, navigate to **Apps** &gt; **IA support** &gt; **API Key** and copy the API key id. This option is available only if you have selected **ServiceNow** \(Indoor Mapping\) as your map provider.

 **Note:** If you have Apple as your location provider, then, this is an optional step for you.

 Location app Id Shows the current location or positioning of employees \(bluedot experience\) on the maps. The start location in wayfinding is automatically determined by the application. If location positioning is enabled, you can see the positioning icon \( ![icon showing enabled indoor positioning on map](../../workplace-space-mapping/images/location-bluedot-icon.png)\) on your mobile app for wayfinding.

</td></tr><tr><td>

Location provider app secret

</td><td>

From your Atlas account, navigate to **Apps** &gt; **IA support** &gt; **API Key** and copy the API key secrete id.

 This option is available if you have installed Indoor Mapping as your

 **Note:** If you have Apple as your location provider, then you are not required to fill this field information. This option is available only if you have selected **ServiceNow** \(Indoor Mapping\) as your map provider

</td></tr><tr><td>

Map provider app id

</td><td>

User name for Mappedin. Available only if you have installed Mappedin as your map provider.To find the user name, navigate to **Space Mapping** &gt; **Mappedin Administration** &gt; **Credentials**. Select **Mappedin Credentials** and copy the user name.

</td></tr><tr><td>

Map provider app secret

</td><td>

App secret of the map provider \(Mappedin\). Available only if you have installed Mappedin as your map provider.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The custom map provider is configured for the table entity that you selected. For example, the map provider shows directions for locations in Building1.

    **Note:** The **CustomMapConfigId** is mapped with sys Id of mapped reservations of Indoor Mapping and Mappedin. To get Indoor Mapping maps, users must update **CustomMapDefaultProviderId** and **CustomMapConfigId** in both **location\_custom\_map** and **locations\_custom\_map**. The **CustomMapDefaultProviderId** is the sys Id of Indoor Mapping associated record in the custom map provider. For more information, see [Enable map view to create reservations](enable-map-view-mobile-reservations.md).

    For more information on how to select a map provider map properties, see [Customize the map properties](../../workplace-space-mapping/task/wsm-configure-map-properties.md).


**Parent Topic:**[Mobile Wayfinding Administration](../concept/mobile-wayfinding.md)

