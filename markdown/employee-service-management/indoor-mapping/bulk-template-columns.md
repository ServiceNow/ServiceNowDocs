---
title: Bulk upload Excel columns
description: Use the bulk upload template to provide information about your campuses, buildings, and floors.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: reference
last_updated: "2025-10-07"
reading_time_minutes: 3
breadcrumb: [Reference, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Bulk upload Excel columns

Use the bulk upload template to provide information about your campuses, buildings, and floors.

|Column|Description|
|------|-----------|
|Campus Name|Unique identifier of the campus. This column is limited to 255 characters.|
|Campus Title|Title of the campus that is displayed on the map views.|
|Campus Address|Physical address of the campus. This column is optional.|
|Country|Country in which the campus is located. You must use the ISO 3166-1 Alpha-2 code for the country.|
|Marker latitude|Geographic latitude coordinate for the campus in the decimal degrees format.|
|Marker longitude|Geographic longitude coordinate for the campus in the decimal degrees format.|
|Enable in Kiosk View|Option to enable the campus for the Kiosk Indoor Mapping feature. You must fill in `YES` or `NO` in this column.|
|Enable in Scenario View|Option to enable the campus for the Scenario Planning feature. You must fill in `YES` or `NO` in this column.|
|Enable in Default View|Option to enable the campus for the Default Indoor Mapping feature. You must fill in `YES` or `NO` in this column.|

|Column|Description|
|------|-----------|
|Building Name|Unique identifier for the building. This column is limited to 255 characters.|
|Building Title|Title of the building that is displayed on the map views.|
|Campus Name|Name of the campus in which the building is located. The name must match an existing campus.|
|Building Address|Physical address of the building. This column is optional.|
|Marker latitude|Precise latitude coordinate for the building in the decimal degrees format.|
|Marker longitude|Precise longitude coordinate for the building in the decimal degrees format.|
|Enable in Kiosk View|Option to enable the building for the Kiosk Indoor Mapping feature. You must fill in `YES` or `NO` in this column.|
|Enable in Scenario View|Option to enable the building for the Scenario Planning feature. You must fill in `YES` or `NO` in this column.|
|Enable in Default View|Option to enable the building for the Default Indoor Mapping feature. You must fill in `YES` or `NO` in this column.|

<table id="table_fqs_pwz_wgc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Floor Number

</td><td>

Unique numerical identifier for the floor.

</td></tr><tr><td>

Floor Name

</td><td>

Name of the floor. This column is limited to 255 characters.

</td></tr><tr><td>

Floor Title

</td><td>

Title of the floor that is displayed on the map views. This column is optional.If this column is empty, the Floor Name is displayed on the map views.

</td></tr><tr><td>

Floor Short Title

</td><td>

Abbreviated title of the floor. This column is optional.If this column is empty, the Floor Number is used for identification.

</td></tr><tr><td>

Building Name

</td><td>

Name of the building in which the floor is located. The name must match an existing building

</td></tr><tr><td>

Campus Name

</td><td>

Name of the campus in which the building is located. The name must match an existing campus.

</td></tr><tr><td>

Source File Name

</td><td>

Name of the CAD file that contains the floor plan.

</td></tr><tr><td>

Source File Unit

</td><td>

Unit of measurement used in the source CAD file. You must select from the following:-   `INCHES`
-   `FEET`
-   `METERS`
-   `DECAMETERS`
-   `MILES`
-   `LIGHT_YEARS`
-   `KILOMETERS`
-   `US_SURVEY_YARD`
-   `ANGSTORMS`
-   `UNDEFINED`
-   `HECTOMETERS`
-   `MILLIMETERS`
-   `PARSECS`
-   `MICROINCHES`
-   `US_SURVEY_MILE`
-   `NANOMETERS`
-   `GIGAMETERS`
-   `CENTIMETERS`
-   `US_SURVEY_FEET`
-   `MILS`
-   `MICRONS`
-   `FEET`
-   `ASTRONOMICAL`
-   `US_SURVEY_INCH`
-   `YARDS`
-   `DECIMETERS`

If this column is empty, INCHES is used as the source file unit.

</td></tr><tr><td>

Enable in Kiosk View

</td><td>

Option to enable the floor for the Kiosk Indoor Mapping feature. You must fill in `YES` or `NO` in this column.

</td></tr><tr><td>

Enable in Scenario View

</td><td>

Option to enable the floor for the Scenario Planning feature. You must fill in `YES` or `NO` in this column.

</td></tr><tr><td>

Enable in Default View

</td><td>

Option to enable the floor for the Default Indoor Mapping feature. You must fill in `YES` or `NO` in this column.

</td></tr></tbody>
</table>**Parent Topic:**[Indoor Mapping references](../concept/indoor-mapping-references.md)

**Previous topic:**[Enhanced Sync Properties](enhanced-sync-properties.md)

**Next topic:**[Workplace Central](../../workplace-central/concept/workplace-central-feat.md)

