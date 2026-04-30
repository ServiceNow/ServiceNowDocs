---
title: Using Workplace Space Mapping
description: With Workplace Space Mapping, your organization can integrate with third-party applications such as Mappedin, customize imported maps, and manage the required data.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Using Workplace Space Mapping

With Workplace Space Mapping, your organization can integrate with third-party applications such as Mappedin, customize imported maps, and manage the required data.

## View interactive location directories

You can view your imported map in interactive location directories.

## Type mappings

When you integrate with a indoor map provider - Indoor Mapping or Mappedin, you must first associate the map types to the map types used by Workplace Service Delivery. This association ensures that your spaces are imported to the correct table with the correct type \(Workplace and Desk\).

-   Indoor Mapping provides inbuilt indoor maps for indoor navigation and wayfinding. Synchronize Indoor Mapping place types with Workplace Indoor Mapping places and spaces. Configure Indoor Mapping place and place type in the Map studio and then import the map objects and place types in Workplace Indoor Mapping. After the map data and map objects are synchronized, use Workplace Service Portal for managing reservations within workplace, case management, and move management. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).
-   Mappedin is a third party map provider and provides indoor maps and wayfinding for workplace users. For more information on how type mappings are converted from Mappedin to Workplace Space Mapping, see [Convert Mappedin data to Workplace Space Mapping data](wsm-mappedin-type-table.md).
-   For more information on maintaining type mappings for Mappedin, see [Maintain type mappings](../task/wsm-mappedin-type-mappings.md).

## Import flow

The weekly \(Saturday\) **Auto-Import Buildings** iHub Flow keeps your map up to date by querying the API of your integrated applications. Any changes to one building in the application's software should be reflected in Workplace Space Mapping.

For example, if you integrate with Mappedin and the Auto-import Buildings iHub Flow runs successfully:

-   The Auto-Import Buildings iHub Flow queries for all buildings associated with Mappedin.
-   The Auto-Import Buildings iHub Flow works with the Mappedin export API to look for any changes to a building made by Mappedin. If there are changes, the building is updated.

## External IDs

Use external IDs to resolve spaces that don't match locations between Workplace Service Delivery Mappedin after importing a building or for existing buildings. For more information, see [Use external IDs to match spaces between Workplace Service Delivery for Mappedin](../task/wsm-mappedin-ext-ids.md).

## Configuring map properties

Configure map properties to customize the way your map renders in the Workplace Service Portal location directory. For more information, see [Customize the map properties](../task/wsm-configure-map-properties.md). For more information about space update and allocation using interactive floor maps, see Map-based Administration [Edit a building's spaces using a map](../../workplace-central/task/edit-space-details-for-buildings.md).

-   **[Use external IDs to match spaces between Workplace Service Delivery for Mappedin](../task/wsm-mappedin-ext-ids.md)**  
After importing a new Mappedin building or after importing an existing Mappedin building, if the locations don't match in Mappedin and Workplace Service Delivery, then use external IDs to resolve space location issues.

**Parent Topic:**[Workplace Space Mapping](wsm-mappedin-admin.md)

