---
title: Operating system-level virtualization discovery
description: Discovery can collect image and container information from Operating system-level virtualization \(OS-level virtualization\) engines.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Operating system-level virtualization discovery

Discovery can collect image and container information from Operating system-level virtualization \(OS-level virtualization\) engines.

Discovery can determine container status and size and identify images and their tags provided by operating-system-level virtualization.

**Note:** Currently, the ServiceNow® platform supports the discovery of Docker virtualization containers only.

## Table schema

|Table|Description|
|-----|-----------|
|cmdb\_ci\_oslv\_engine|Base table for all OSLV engines.|
|cmdb\_ci\_oslv\_image|Base table for globally unique OSLV images.|
|cmdb\_ci\_oslv\_local\_image|Base table for local instances of OSLV images.|
|cmdb\_ci\_oslv\_image\_tag|Base table for tags on OSLV images.|
|cmdb\_ci\_oslv\_container|Base table to store containers found on the host.|

## Data collected

<table id="table_lhw_yq2_5w"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Operating System Level Virtualization Engine \[cmdb\_ci\_oslv\_engine\]

</td><td>

Server \[server\]

</td></tr><tr><td>

Operating System Level Virtualization Image \[cmdb\_ci\_oslv\_image\]

</td><td>

-   Image ID \[image\_id\]
-   Image digest \[image\_digest\]
-   Image created \[image\_created\_at\]
-   Size \(bytes\) \[size\_bytes\]

</td></tr><tr><td>

Operating System Level Virtualization Local Image \[cmdb\_ci\_oslv\_local\_image\]

</td><td>

Image ID \[image\_id\]

</td></tr><tr><td>

Operating System Level Virtualization Image Tag \[cmdb\_ci\_oslv\_image\_tag\]

</td><td>

-   Image ID \[image\_id\]
-   Repository \[repository\]
-   Tag \[tag\]

</td></tr><tr><td>

Operating System Level Virtualization Container \[cmdb\_ci\_oslv\_container\]

</td><td>

-   Container ID \[container\_id\]
-   Status \[status\]
-   Size \(bytes\) \[size\_bytes\]
-   Image ID \[image\_id\]

</td></tr></tbody>
</table>-   **[Docker virtualization](c-docker-virtualization.md)**  
Discovery uses the **Docker Pattern** to collect data about specific objects in a Docker engine, running on a Linux host.

**Parent Topic:**[Data collected by ITOM Visibility](../reference/data-collected-by-itom-visibility.md)

