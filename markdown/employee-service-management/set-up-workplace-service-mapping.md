---
title: Setting up Workplace Space Mapping
description: Configure and synchronize Indoor Mapping and Mappedin map data and objects with Workplace Service Delivery.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Setting up Workplace Space Mapping

Configure and synchronize Indoor Mapping and Mappedin map data and objects with Workplace Service Delivery.

## Activating Workplace Space Mapping

Activation of the Workplace Space Mapping plugin depends on what family release you are currently using.

For Workplace Service Delivery to work with Workplace Indoor Mapping and Mappedin install both Indoor Mapping and Workplace Indoor Mapping plugins from store. For Mappedin install the Mappedin plugin \(sn\_wsd\_mappedin\) from store.

## Configure Indoor Mapping with Workplace Service Delivery

Synchronize the Indoor Mapping map data and map objects to work with Workplace Service Delivery, see [Configure Workplace Indoor Mapping](wsd-integration-indoor-mapping.md).

## Configure Mappedin with Workplace Service Delivery

To use Mappedin as your third-party map application, complete the configuration requirements.

<table id="table_xwx_ffn_trb"><thead><tr><th>

Requirement

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Obtain Mappedin credentials and export credentials

</td><td>

ServiceNow uses credentials provided by MappedIn to import space data \(buildings, floors, and spaces\).

 Export credentials are required by the ServiceNow AI Platform to render a Mappedin map and to successfully periodically reimport updated floor plans.

 -   The Client ID credential is the equivalent of a user name in Workplace Core
-   The Client Secret is the equivalent a password in Workplace Core

</td></tr><tr><td>

Install and activate the Mappedin integration

</td><td>

Install and activate the Mappedin integration in order to use Workplace Space Mapping to manage imported data and customize the map. For more information, see [Install the Mappedin integration](../task/wsm-mappedin-activate.md)

</td></tr><tr><td>

Enter credentials in Workplace Space Mapping

</td><td>

You must enter your Mappedin credentials in Workplace Space Mapping. For more [Maintain Workplace Service Delivery Mappedin credentials](../task/wsm-mappedin-credentials.md)

</td></tr><tr><td>

Configure a connection in Workplace Space Mapping

</td><td>

The base system provides a pre-configured connection to Mappedin.

</td></tr></tbody>
</table>-   **[Maintain Workplace Service Delivery Mappedin credentials](../task/wsm-mappedin-credentials.md)**  
To configure and work with Mappedin ensure that you have a valid login credential. Work with the Mappedin to obtain these credentials.
-   **[Customize the map properties](../task/wsm-configure-map-properties.md)**  
Customize how your map renders in the Workplace Service Portal by configuring Workplace Space Mapping properties.

**Parent Topic:**[Configuring Workplace Space Mapping](wsm-config_space_mapping.md)

**Related topics**  


[Configure Workplace Indoor Mapping](wsd-integration-indoor-mapping.md)

[Configure Mappedin](mappedin-integration-topics.md)

