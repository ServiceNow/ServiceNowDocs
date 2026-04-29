---
title: Advanced resource filter tables
description: The tables that contain the values administrators must enable for dispatchers to use to create resource filters can be found listed below.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Field Service Management]
---

# Advanced resource filter tables

The tables that contain the values administrators must enable for dispatchers to use to create resource filters can be found listed below.

The available tables are different if you have assignment groups or territories configured.

<table id="table_l1j_zzv_gdc"><thead><tr><th>

Name

</th><th>

Tables

</th></tr></thead><tbody><tr><td>

Assignment group agent configuration \(agent\_filter\_config\_view\)

</td><td>

-   sys\_user\_grmember
-   sys\_user
-   sys\_user\_has\_skill

</td></tr><tr><td>

Assignment group crew configuration \(crew\_filter\_config\_view\)

</td><td>

-   wm\_crew\_group
-   wm\_crew
-   wm\_crew\_skill

</td></tr><tr><td>

Territory agent configuration \(terr\_agent\_filter\_config\_view\)

</td><td>

-   sys\_user
-   sys\_user\_grmember
-   sn\_tp\_territory\_group
-   sn\_tp\_territory\_membership\_override
-   sys\_user\_has\_skill

</td></tr><tr><td>

Territory crew configuration \(terr\_crew\_filter\_config\_view\)

</td><td>

-   wm\_crew
-   wm\_crew\_group
-   sn\_tp\_territory\_group
-   sn\_tp\_territory\_membership\_override
-   wm\_crew\_skill

</td></tr></tbody>
</table>**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

