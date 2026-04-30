---
title: Enable map view to create reservations
description: Enable map view for mobile employee users so that they can reserve spaces using floor maps Now Mobile app.
locale: en-US
release: xanadu
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-04-22"
reading_time_minutes: 3
breadcrumb: [Configure Workplace Service Delivery for Mobile, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Enable map view to create reservations

Enable map view for mobile employee users so that they can reserve spaces using floor maps Now Mobile app.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

Activate the Enable Map view option. Users can view maps supported by Indoor Mapping or Mappedin while reserving a space.

## Procedure

1.  Navigate to **All** &gt; **Space Mapping** &gt; **Custom Map Provider** to modify the base system map provider.

    Modify the base system map provider to use one of your buildings as a key and use either your Workplace Indoor Mapping or Mappedin credentials.

2.  Mappedin: If your Map provider is Mappedin, perform the following steps:

    1.  Open the base system custom map provider record.

        This record does not have a name. If your system has multiple custom map providers, you have to identify this record by its sys\_id. To check the sys\_id of a record, right-click the record, select **Copy sys\_id** from Additional Actions on top left , and paste the sys\_id **c5d49d2265072010f87794bf508527f6** into a text document.

    2.  Modify the following fields on the Custom Map Provider form:

        |Field|Description|
        |-----|-----------|
        |Key|Table entry for which you want to configure the map provider. For example, Building1.|
        |Map provider app id|User name for the Mappedin credentials. To find the user name, navigate to **All** &gt; **Space Mapping** &gt; **Mappedin Administration** &gt; **Credentials**. Select your Mappedin Credentials and copy the user name.|
        |Map provider app secret|Your map provider's \(Mappedin\) app secret credentials.|

    3.  Select **Update**

    4.  For Mappedin, update **CustomMapDefaultProviderId** and **CustomMapConfigId** in both location\_custom\_map and locations\_custom\_map with corresponding Sys IDs.

    5.  Navigate to **All** &gt; **sys\_sg\_input\_list** to open the Inputs page.

    6.  Select and open the **location\_custom\_map** and **locations\_custom\_map** and make the following changes for both these properties:

        1.  On the Location Map View and Locations Map view page, Edit the **CustomMapDefaultProviderId** and verify that it is mapped with sys id of Mappedin associated record on the Custom map provider page \(see step 2a\).
        2.  Edit the **CustomMapConfigId** and verify that it is mapped with sys id of sys\_sg\_custom\_map\_config.list. To copy the sys\_id, navigate to **All** &gt; **sys\_sg\_custom\_map\_config.list**. Select **Mapped Reservations** and copy the sys\_id and then paste it for **CustomMapConfigId**.
3.  If you have installed Indoor Mapping as your map provider, perform the following steps:

    1.  Navigate to **All** &gt; **Space Mapping** &gt; **Custom Map Provider** to modify the base system map provider.

    2.  A new map provider **ServiceNow** is created for Workplace Indoor Mapping in the Custom Map Provider.

    3.  Open the base system custom map provider record to edit.

    4.  Right-click the record, select **Copy sys\_id** from Additional Actions on top left, and paste the sys\_id **5a0a15aac35301100f926ff4c840dd9a** into a text document.

    5.  Modify the following fields on the Custom Map Provider form:

<table id="table_mxq_mnk_jvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key table

</td><td>

Building \(sn\_wsd\_core\_building\) that is integrated with Workplace Indoor Mapping.Selecting a building to enable map functionality for all other Workplace Indoor Mapping buildings.

</td></tr><tr><td>

Key

</td><td>

Workplace Indoor Mapping building name. For example: Building A.

</td></tr><tr><td>

Map provider

</td><td>

Select **ServiceNow** from the drop-down list.

</td></tr></tbody>
</table>    6.  Click **Update**.

    7.  To get Workplace Indoor Mapping maps, user needs to update **CustomMapDefaultProviderId** and **CustomMapConfigId** in both location\_custom\_map and locations\_custom\_map with corresponding sys ids.

    8.  Navigate to **All** &gt; **sys\_sg\_input\_list** to open the Inputs page.

    9.  Select and open the **location\_custom\_map** and **locations\_custom\_map** and make the following changes for both these properties:

        1.  On the Location Map View and Locations Map view page, Edit the **CustomMapDefaultProviderId** and verify that it is mapped with sys id of ServiceNow associated record in Custom map provider page \(see step 3c\).
        2.  Edit the **CustomMapConfigId** and verify that it is mapped with sys id of sys\_sg\_custom\_map\_config.list. To copy the sys\_id, navigate to **All** &gt; **sys\_sg\_custom\_map\_config.list**. Select **Mapped Reservations-Indoor Map** and copy the sys\_id and then paste it for **CustomMapConfigId**.
4.  Click **Update**.

5.  Navigate to **All** &gt; **Workplace Service Delivery for Mobile** &gt; **Properties**.

6.  Navigate to the Enable Map view option for WSD Mobile Reservations property.

7.  Select the Enable Map view option for WSD Mobile Reservations property to enable it.

8.  Select **Save**.


## Result

Option to view a floor map using the Map view instead of a list view is available for Workplace Service Delivery for Mobile users. You can use the **Toggle map view** option while making a reservation to view floor maps and select spaces. For more information, see [Configure the Toggle map view property](configure-toggle-map-view.md).

**Parent Topic:**[Configure Workplace Service Delivery for Mobile](../concept/configure-wsd-mobile.md)

**Previous topic:**[Configure a custom Map provider](configure-custom-map-provider.md)

**Next topic:**[Configure the Toggle map view property](configure-toggle-map-view.md)

