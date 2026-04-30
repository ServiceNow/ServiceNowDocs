---
title: Convert Mappedin data to Workplace Space Mapping data
description: Use the Mappedin Type Mappings table to convert data from Mappedin to Workplace Space Mapping data.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Mappedin, Configure Workplace Space Mapping, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Convert Mappedin data to Workplace Space Mapping data

Use the **Mappedin Type Mappings** table to convert data from Mappedin to Workplace Space Mapping data.

The **Mappedin Type Mappings** table has configurations to convert the Type and Subtype data used in a Mappedin map to **Table** and **Space type** used in Workplace Core.

## Terms

The terms used in Mappedin and how they relate to Workplace Core:

|Mappedin term|Workplace Core term|
|-------------|-------------------|
|Venue|Building|
|Map|Floor|
|Location|Spaces|

## Mappedin data

For example, you want to convert a Mappedin map with the following information:

-   Single floor building
-   14 total locations
    -   10 desks \(Mappedin type = Desk\)
    -   Two conference rooms \(Mappedin type = Meeting room\)
    -   Two restrooms \(Mappedin type = Amenities, Subtype = Universal Washroom\)

## Workplace Core data

You want to convert the Mappedin data from the 14 locations, and want them converted to:

-   Desks
-   Rooms
-   Restrooms

**Note:** You don't want all the Mappedin data to be converted to Spaces or Desks.

## Type mappings

To ensure your locations move to the correct Space \(sn\_wsd\_core\_space\) or Room \(sn\_wsd\_core\_room\) tables, and ensure that the locations have the correct type \(Restroom or Desk\), make the following type mappings in the **Mappedin Type Mappings** table:

-   Mappedin locations with the type = Desk \(no subtype\) converted to the Space \(sn\_wsd\_core\_space\) table and have the Space type set to Workspace/Desk.
-   Mappedin locations with the type = Meeting room \(no subtype\) converted to the Room \(sn\_wsd\_core\_room\) table and have the Space type set to Room.
-   Mappedin locations with the type = Amenities and subtype = Universal Washroom converted to the Space \(sn\_wsd\_core\_space\) table and have the Space type set to Restroom.

You can import a Mappedin building \(single floor building\) and the 14 locations go to the correct tables and have the correct types.

-   **[Maintain type mappings](../task/wsm-mappedin-type-mappings.md)**  
Use **Type mappings** to convert the Type and Subtype locations in Mappedin to the Table and Space type used in Workplace Space Mapping.
-   **[Import a new building - Mappedin](../task/wsm-mappedin-import-building.md)**  
Use **Import a new building** to import the Mappedin map and define the building details.
-   **[Import an existing building - Mappedin](../task/wsm-mappedin-import-existing-bldg.md)**  
Follow these steps to import an existing building for a Mappedin map.

**Parent Topic:**[Configure Mappedin](mappedin-integration-topics.md)

