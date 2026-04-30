---
title: View the network or storage path in classic Service Mapping
description: You can drill down to see objects behind a connection on a map for troubleshooting service performance or maintaining your network. This feature is not available for manually created services or for services on instances using Edge Encryption.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View the network or storage path in classic Service Mapping

You can drill down to see objects behind a connection on a map for troubleshooting service performance or maintaining your network. This feature is not available for manually created services or for services on instances using Edge Encryption.

## Before you begin

Role required: admin, service\_mapping\_admin or service\_mapping\_user

## About this task

Displaying a network or storage path allows you to see routers, switches, and host ports which are part of the connection. The following connection types exist:

-   **Network path**

    The infrastructure route between two CIs of the host type.

-   **Storage path**

    The infrastructure route between a CI of the host type and a CI of the storage type.


Service Mapping discovers and displays network devices located on your organization local network, not on WAN or the public cloud. When Service Mapping encounters a connection between two applications, it uses traceroute on the source host to figure out the path to the target host. Then Service Mapping use SNMP credentials to discover the devices it found on the path.

Service Mapping can show devices for storage paths using the following protocols:

-   Fiber Channel: Storage Area Network \(SAN\)
-   IP Ethernet: Internet Small Computer Systems Interface \(iSCSI\) or Network Attached Storage \(NAS\)

    **Note:** For storage paths using Fiber Channel, Service Mapping does not display Fiber Channel switches.


Between a host CI and a storage CI there may be two separate storage paths using different protocols: Fiber Channel and IP Ethernet. If so, the service instance map displays one connection line for both protocols.

You can see the change history for network and storage paths for application services. Checking path history for manual or technical services is not supported.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technical Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  On the map, right-click the connection for the network or storage path you want to see.

3.  Select **Show network path** or **Show storage path**.

4.  If necessary, select the type of protocol and click **Choose** in the Choose Protocol Type dialog box.

    The view showing the network or storage path opens in a new tab.

    ![View the network or storage path.](../image/MapStrgPathConnectors.png)

    If Service Mapping cannot discover all objects in a connection, the connector line on the network or storage path appears dotted as shown above.

5.  For storage paths, use the Storage Mapping tab at the bottom of the screen to view correlation between file systems on the host and the storage volume or the shared folder on the storage device.

6.  To view the change history for network paths, perform steps in [View the change history of application services in classic Service Mapping](t_ViewCIChanges.md).

7.  If you access the network or storage path map from Event Management, you can see the list of alerts related to this path appear at the bottom of the screen.


**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

**Related topics**  


[Application service maps in classic Service Mapping](../concept/c_UndestandMaps.md)

[SNMP-based queries](../reference/snmp-based-queries.md)

