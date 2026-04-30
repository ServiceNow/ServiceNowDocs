---
title: Linear Assets Support properties
description: Linear assets support for Field Service Management uses the following system properties, which are located in the System Properties \[sys\_properties\] table.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Field Service Management]
---

# Linear Assets Support properties

Linear assets support for Field Service Management uses the following system properties, which are located in the System Properties \[sys\_properties\] table.

<table id="table_bwr_vnm_11c"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm.default\_location\_for\_linear\_work\_order

</td><td>

Default location for linear asset work order.-   Type: choice list
-   Default value: start\_location

</td></tr><tr><td>

sn\_fsm.linear\_assets\_map\_distance\_unit

</td><td>

Distance unit used in calculation of radius on map for linear assets.-   Type: choice list
-   Default value: kilometers

</td></tr><tr><td>

sn\_fsm.linear\_assets\_map\_initial\_zoom

</td><td>

Controls the initial zoom level of Google Maps while displaying linear assets in the Field Service Management Service Locations feature.-   Type: integer
-   Default value: 3

</td></tr><tr><td>

sn\_fsm.linear\_assets\_map\_load\_distance

</td><td>

Map load distance radius for linear assets-   Type: integer
-   Default value: 10

</td></tr><tr><td>

sn\_fsm.linear\_assets\_map\_max\_zoom\_level

</td><td>

Controls the maximum auto-zoom level of Google Maps while displaying linear assets in the Field Service Management Service Locations feature. It limits how far the map automatically zooms in while fitting markers or assets into view.-   Type: integer
-   Default value: 12

</td></tr><tr><td>

sn\_fsm.linear\_assets\_map\_type

</td><td>

Distance unit used on service location google maps-   Type: Choice list
-   Default value: roadmap

</td></tr></tbody>
</table>**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

