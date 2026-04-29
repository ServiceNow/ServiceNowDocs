---
title: MID Server configuration for Service Mapping in upgraded deployments
description: For ServiceNow deployments upgraded from earlier versions to Istanbul, Service Mapping uses the legacy algorithm to choose a MID Server for a discovery request.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Server configuration for Service Mapping, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# MID Server configuration for Service Mapping in upgraded deployments

For ServiceNow deployments upgraded from earlier versions to Istanbul, Service Mapping uses the legacy algorithm to choose a MID Server for a discovery request.

MID Servers have the following selection criteria that Service Mapping in upgraded deployments uses to choose a MID Server for a discovery request:

-   Application — defines what application a MID Server works with. Set it to Service Mapping to reserve this MID Server exclusively to Service Mapping discovery requests. Alternatively, set it to ALL to allow any ServiceNow application to use this MID Server.

    In earlier releases, you could configure MID Servers to work only with Service Mapping by using the **Capability** parameter. If you had MID Servers with this configuration, during the upgrade to Istanbul the application parameter is automatically set to **ServiceMapping** for them.

-   IP range — limits operation of this MID Server to this IP range. Service Mapping does not choose this MID Server for a discovery request whose endpoint is outside this IP range.

In addition to the IP range, you can configure one of the MID Servers as the default server that Service Mapping uses. For operational information, see [Configure a default MID Server for Service Mapping for upgraded deployments](../task/config-default-mid-for-sm.md).

In upgraded deployments, Service Mapping selects a MID Server using a legacy algorithm:

-   Service Mapping chooses the MID Server whose application criteria is set to **ServiceMapping** or to **ALL**.
-   By default, Service Mapping selects the MID Server whose IP range matches the IP in the discovery request.
-   If Service Mapping cannot find a MID Server with the matching IP range and matching application, it assigns the discovery request to the default MID Server.
-   If there is no default MID Server and none of the MID Servers have IP ranges configured for them, Service Mapping uses a random MID Server.
-   If there is no default MID Server and no IP range matches the IP in the discovery request, Service Mapping cannot start the discovery process.

The new algorithm for selecting MID Servers uses an extra selection criteria: capability. It allows Service Mapping to take a network protocol into consideration. For information about updated selection criteria and the new MID Server selection algorithm, see [Choose MID Server selection algorithm](../task/choose-mid-selection-algorithm.md).

While by default Service Mapping uses the legacy algorithm in upgraded deployments, it can support both new and legacy algorithms for selecting a MID Server. If necessary, you can enable the new MID Server selection algorithm for your upgraded deployment. For more information, see [Choose MID Server selection algorithm](../task/choose-mid-selection-algorithm.md).

**Parent Topic:**[MID Server configuration for Service Mapping](configure-mid-service-mapping.md)

**Related topics**  


[Configure an IP address range for the MID Server](https://www.servicenow.com/docs/access?context=t_ConfigureMIDIPRange&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

