---
title: Traffic-based connections list
description: Refer to this chart for information about traffic-based connections when you remove CIs from an application service.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Traffic-based connections list

Refer to this chart for information about traffic-based connections when you remove CIs from an application service.

<table id="id_fcw_cny_31c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP

</td><td>

The IP address of the application connected to the selected CI.

</td></tr><tr><td>

Port

</td><td>

The port on the selected CI that is used to communicate to the other application.

</td></tr><tr><td>

Process

</td><td>

The ID of the process in the selected CI.

</td></tr><tr><td>

Already on map

</td><td>

-   **Yes** — if this connection shows on the map.
-   **No** — if this connection is not part of the service instance and not on the map.

</td></tr><tr><td>

System decision

</td><td>

The setting defines if Service Mapping keeps the discovered traffic-based connection or removes it. The value comes from the algorithm that Service Mapping uses.

</td></tr><tr><td>

User decision

</td><td>

\(Optional\) The setting overrides the System decision setting, which defines if Service Mapping keeps the discovered traffic-based connection or removes it. For example, if the System decision setting for a connection is Keep, and you want to remove this connection, select `Remove`.

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

