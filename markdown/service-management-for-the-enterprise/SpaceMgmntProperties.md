---
title: Space Management properties
description: Space Management Properties are available to configure floor plan, parsing, and space management defaults settings. You can control default settings like the color for selected space, compass on a floor plan, and logos and titles to appear.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Installed with Facilities Visualization Workbench, Activate Facilities Visualization Workbench, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Space Management properties

Space Management Properties are available to configure floor plan, parsing, and space management defaults settings. You can control default settings like the color for selected space, compass on a floor plan, and logos and titles to appear.

Space Management organizes properties into these sections:

-   Floor Plan
-   Parsing
-   Space Management

Navigate to **Space Management** &gt; **Map Configuration** &gt; **Properties**.

## Floor Plan

<table id="table_b4f_jcp_yq"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

The logo to use for the header of the interactive floor plan \[facilities.management.fvw.workbench.logo\]

</td><td>

Click to select a logo that appears in the top, left corner of an interactive floor plan.

</td></tr><tr><td>

The title to show on the workbench \[facilities.management.fvw.workbench.title\]

</td><td>

The title to show on the workbench.-   Type: string
-   Default value: Workbench

</td></tr><tr><td>

Use user's location as the default campus when available \[facilities.management.fvw.default.campus\]

</td><td>

The location of the user is used as the default campus when available.-   Yes: Use the location of the user.
-   No: Do not use the location of the user.

</td></tr><tr><td>

Allow copying a URL link when available on the workbench \[facilities.management.fvw.allow.copy.url\]

</td><td>

Allow copying a URL link when available on the workbench.-   Yes: Allow copying of a URL.
-   No: Do not allow copying of a URL.

</td></tr><tr><td>

Default to showing the compass on the floor plan \[facilities.management.fvw.show.compass\]

</td><td>

Determines if a compass appears in the top, right corner of a floor plan to provide directional orientation.

</td></tr><tr><td>

The maximum length allowed for a label before using ellipses \[facilities.management.fvw.max.label.length\]

</td><td>

The maximum number of characters allowed for a label before using ellipses.-   Type: integer
-   Default value: 30

</td></tr><tr><td>

The color to use for highlighting the selected space on the floor plan map \[facilities.management.fvw.highlight.color\]

</td><td>

The color that can be used for highlighting a specific space on the floor plan map.-   Type: string
-   Default value: \#F5F500

</td></tr><tr><td>

The colors for applying filters to the workbench \[facilities.management.fvw.filter.colors\]

</td><td>

The colors available for applying filters to the workbench.-   Type: string
-   Default value: \#278ECF; \#4BD762; \#FFCA1F; \#FF9416; \#D42AE8; \#535AD7; \#FF402C; \#83BFFF; \#6EDB8F; \#FFE366; \#FFC266; \#D284BD; \#8784DB; \#FF7B65; \#CAEEFC; \#9ADBAD; \#FFF1B2; \#FFE0B2; \#FFBEB2; \#B1AFDB

</td></tr><tr><td>

The colors for availability filtering on the workbench \[facilities.management.fvw.availability.colors\]

</td><td>

The colors for availability filtering on the workbench.-   Type: string
-   Default value: \#71e279; \#fcc742; \#278efc; \#f95050; \#00A0A6; \#fc8a3d; \#00FFFF; \#b1afdb

</td></tr><tr><td>

Maximum number of search results to return per level on spaces tab in workbench \[facilities.management.fvw.max.results.per.level\]

</td><td>

Maximum number of search results to return per level on spaces tab in workbench.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

Maximum number of search results to return per campuses on spaces tab in workbench \[facilities.management.fvw.max.results.per.campus\]

</td><td>

Maximum number of search results to return for campuses on spaces tab in workbench.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

Maximum number of search results to return for other campus on spaces tab in workbench \[facilities.management.fvw.max.results.per.other.campus\]

</td><td>

Maximum number of search results to return for other campuses on spaces tab in workbench. -   Type: integer
-   Default value: 20

</td></tr><tr><td>

Maximum number of search results to return when searching for tasks in workbench \[facilities.management.fvw.max.requests.per.search\]

</td><td>

Maximum number of search results to return when searching for facilities/move requests tabs in workbench. -   Type: integer
-   Default value: 200

</td></tr><tr><td>

Maximum number of spaces per zone to render for the zone edit tab \[facilities.management.fvw.max.spaces.per.zone\]

</td><td>

Maximum number of spaces per zone to render for the zone edit tab. -   Type: integer
-   Default value: 50

</td></tr><tr><td>

Maximum number of tasks to return per level on workbench \[facilities.management.fvw.max.requests.per.level\]

</td><td>

Maximum number of search results to return per level on spaces tab in workbench.-   Type: integer
-   Default value: 20

</td></tr></tbody>
</table>## Parsing

<table id="table_ubt_fdx_lcb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Specifies whether we should preserve the field values of records when parsing geoJSON files if the record already exists \[facilities.management.fvw.geojson.parsing.preserve.fields\]

</td><td>

Determines how to save the field values of existing records when parsing geoJSON files or to delete them.-   Yes: Do not change when parsing new map.
    -   The building name.
    -   The level name, level abbreviation, and the main level flag.
    -   The space name and internal name.
-   No: Use values from latest geoJSON file.

</td></tr><tr><td>

Specifies whether we should preserve the field values of records when parsing geoJSON files if the record already exists \[facilities.management.fvw.geojson.parsing.preserve.fields\]

</td><td>

If the space exists, specifies whether the sys\_class\_name of a space is preserved when parsing geoJSON files.-   Yes: Save
-   No: Update

**Note:** The sys\_class\_name \(fm\_bathroom, fm\_cubicle, and so on\) are only updated if both parsing properties are set to **No**.


</td></tr><tr><td>

Specifies whether we should preserve the sys\_class\_name of a space when parsing geoJSON files if the space already exists \[facilities.management.fvw.geojson.parsing.preserve.sys\_class\_name\]

</td><td>

Specifies how to handle area parsing. -   Preserve Existing Area: Saves the area space when the current value is greater than 0.0001 in the **Area** field in the **Space** form.
-   Overwrite Area: Always updates the area of a space from an area file.
-   Ignore Area Files: Does not parse any existing area files within the map set.

**Note:** Regardless of the flags, area roll ups are calculated after parsing.


</td></tr></tbody>
</table>## Space Management

<table id="table_mlq_pz1_qy"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

The system base area unit for facilities space tables. Set to true to use meters squared, or false to use feet squared \[facilities.management.fvw.area.unit\]

</td><td>

The system base area unit for facilities space tables. Set to true to use meters squared, or false to use feet squared.-   Type: true \| false
-   Default value: false

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Visualization Workbench](../../facilities-interactive-facility-maps/reference/r_InstallWFacVisWorkbench.md)

