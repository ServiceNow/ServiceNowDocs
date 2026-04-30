---
title: Fine-tune Service Mapping with MID affinity and IP reuse
description: The MID Server needed to map an application service might be misidentified in subnetworks with overlapping IP ranges and reused IP addresses. To enable the successful discovery of resources associated with a subnetwork, Service Mapping provides several properties for MID Server identification.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-08-03"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Fine-tune Service Mapping with MID affinity and IP reuse

The MID Server needed to map an application service might be misidentified in subnetworks with overlapping IP ranges and reused IP addresses. To enable the successful discovery of resources associated with a subnetwork, Service Mapping provides several properties for MID Server identification.

The networks of large organizations are often divided into numerous subnetworks, each acting as a network of its own. Service Mapping selects the MID Server based on its IP range. Subnetworks with overlapping IP ranges and reuse of IP addresses risk misidentification of the MID Server needed to map an application service. Discovery can therefore fail, resulting in incomplete or inaccurate service maps.

Two properties included with Service Mapping offer a solution to system administrators.

**Note:** For full functionality, this feature requires the installation of CMDB CI Class Models version 1.50.0 or later.

-   MID affinity: If horizontal discovery has been configured, you can enable the **sm.topdown.reuse\_mid\_from\_hd\_schedule** system property. It identifies the subnetwork MID Server that was previously configured during horizontal discovery and reuses it for top-down discovery in Service Mapping. Configuring the MID Server using this method requires less time and results in fewer misidentifications.
-   Network location: After locations have been assigned to the horizontal discovery schedules, you can enable the **sm.network\_location.detect\_host\_by\_location** system property, which adds a **Network Location** field to the Entry point form. The top-down discovery process starts with the entry point defined on this form and can then identify both the MID Server and the host using the location provided in the horizontal discovery schedule.

To learn more about enabling each property, see [Components installed with Service Mapping](../reference/components-installed-with-service-mapping.md)

**Related topics**  


[Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md)

[MID Server configuration for Service Mapping](configure-mid-service-mapping.md)

