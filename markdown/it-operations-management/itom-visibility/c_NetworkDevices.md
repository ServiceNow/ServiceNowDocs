---
title: Network device discovery
description: Discovery identifies several network devices, including load balancers, routers, TCP connections, IP networks, and so on. It can find devices through traditional port probes, and then through identifications and exploration probes, or through patterns. It also supports discovery by identifying HTTP and TCP connections.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Network device discovery

Discovery identifies several network devices, including load balancers, routers, TCP connections, IP networks, and so on. It can find devices through traditional port probes, and then through identifications and exploration probes, or through patterns. It also supports discovery by identifying HTTP and TCP connections.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

-   **[Load balancer discovery](c_LoadBalancers.md)**  
Discovery can collect data about network routers, switches, and applications.
-   **[Layer 2 discovery](c_Layer2Discovery.md#)**  
Discovery can detect the physical connections, known as layer 2, between network devices.
-   **[TCP connection discovery](../reference/r_DataCollDiscoTCPConnections.md)**  
Discovery identifies and classifies information about TCP connections using the ADM and ADME probes.
-   **[IP address discovery](../reference/r_DataCollDiscoIPAddress.md)**  
Discovery identifies and classifies information about IP addresses.
-   **[IP network discovery](../reference/r_DataCollDiscoIPNetworks.md)**  
Discovery identifies and classifies information about IP networks.
-   **[Network printer discovery](../reference/r_DataCollDiscoNetworkPrinters.md)**  
Discovery identifies and classifies information about network printers.
-   **[Network switch and router discovery](../reference/r_DataCollDiscoNWRouteAndSwitch.md)**  
Discovery identifies and classifies information about network switches and routers.
-   **[IP service and daemon discovery](../reference/r_DataCollDiscoServicesAndDaemons.md)**  
Discovery identifies and classifies information about services and daemons.
-   **[Uninterruptible power supply \(UPS\) discovery](../reference/r_DataCollDiscoUnintPowerSupp.md)**  
Discovery identifies and classifies information about an uninterruptible power supply \(UPS\).
-   **[IBM WebSphere DataPower discovery](../reference/data-coll-datapower.md)**  
ITOM Visibility discovers IBM WebSphere DataPower. The Discovery feature uses the DataPower Server pattern for horizontal discovery. The Service Mapping feature uses the DataPower pattern for top-down discovery.
-   **[Cisco Unified Computing System \(UCS\)-HD device discovery](../reference/r-CiscoUCSHD.md)**  
Discovery and Service Mapping Patterns application uses the to find Cisco UCS equipment, including chassis and blades. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Dell Remote Assistant Card discovery](c_DRACDiscovery.md)**  
The Dell™ Remote Assistant Card \(DRAC\) and Integrated Remote Assistance Card \(iDRAC\) provide users with tools and functionality to monitor, troubleshoot, and repair servers. You can generate DNS URLs to access out-of-band devices when security prevents access from IP addresses.
-   **[HTTP device discovery](http-discovery.md)**  
Discovery can find devices that use the HTTP protocol.

**Parent Topic:**[Data collected by ITOM Visibility](../reference/data-collected-by-itom-visibility.md)

