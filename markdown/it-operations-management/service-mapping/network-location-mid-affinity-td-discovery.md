---
title: Fine-tune Service Mapping with MID affinity and IP reuse
description: The MID Server needed to map an application service might be misidentified in subnetworks with overlapping IP ranges and reused IP addresses. To enable the successful discovery of resources associated with a subnetwork, Service Mapping provides several properties for MID Server identification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/network-location-mid-affinity-td-discovery.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Fine-tune Service Mapping with MID affinity and IP reuse

The MID Server needed to map an application service might be misidentified in subnetworks with overlapping IP ranges and reused IP addresses. To enable the successful discovery of resources associated with a subnetwork, Service Mapping provides several properties for MID Server identification.

The networks of large organizations are often divided into numerous subnetworks, each acting as a network of its own. Service Mapping selects the MID Server based on its IP range. Subnetworks with overlapping IP ranges and reuse of IP addresses risk misidentification of the MID Server needed to map an application service. Discovery can therefore fail, resulting in incomplete or inaccurate service maps.

Two properties included with Service Mapping offer a solution to system administrators.

**Note:** For full functionality, this feature requires the installation of CMDB CI Class Models version 1.50.0 or later.

-   MID affinity: If horizontal discovery has been configured, you can enable the **sm.topdown.reuse\_mid\_from\_hd\_schedule** system property. It identifies the subnetwork MID Server that was previously configured during horizontal discovery and reuses it for top-down discovery in Service Mapping. Configuring the MID Server using this method requires less time and results in fewer misidentifications.

    **Note:** For subnet-based MID affinity to take effect, an executed horizontal Discovery schedule configured to use the IP range targeted by top-down Service Mapping must exist. If no matching horizontal Discovery history exists for the IP range, affinity will not apply.

-   Network location: After locations have been assigned to the horizontal discovery schedules, you can enable the **sm.network\_location.detect\_host\_by\_location** system property, which adds a **Network Location** field to the Entry point form. The top-down discovery process starts with the entry point defined on this form and can then identify both the MID Server and the host using the location provided in the horizontal discovery schedule.

Legacy MID Server selection: Verify that **sa.mapping.legacy\_mid\_selection** is set to false. When set to true, Service Mapping uses the legacy MID Server selection algorithm and the MID affinity properties have no effect, regardless of their configuration.

To learn more about enabling each property, see [Components installed with Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/components-installed-with-service-mapping.md)

**Related topics**  


[Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md)

[MID Server configuration for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/configure-mid-service-mapping.md)

