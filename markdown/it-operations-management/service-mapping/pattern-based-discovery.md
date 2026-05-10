---
title: Pattern-based discovery in Service Mapping
description: Pattern-based discovery is the main method of Service Mapping collecting data about devices and applications used in application services. After Service Mapping collects data, it then creates a map of application services and stores the collected data in the CMDB.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Pattern-based discovery in Service Mapping

Pattern-based discovery is the main method of Service Mapping collecting data about devices and applications used in application services. After Service Mapping collects data, it then creates a map of application services and stores the collected data in the CMDB.

ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

Service Mapping uses patterns to discover and map CIs. A pattern is a sequence of commands designed to detect attributes of a CI and its outbound connections. A typical Service Mapping pattern consists of two types of algorithms for identifying CIs and finding CI connections.

The starting point of any discovery process is an entry point. An entry point is a point where clients access a service instance. For example, to map your electronic mailing service instance, define an IP address or host name of the email server as an entry point. The discovery and mapping process begins from Discovery performing the horizontal discovery to identify the host. Once the host discovery is complete, Service Mapping starts the top-down discovery to find and map applications running on this host.

Service Mapping uses MID Servers to communicate with CIs in your organization. MID Servers are located inside your organization network and Service Mapping can communicate with them without traversing firewalls.

**Note:** Currently, pattern operations do not support multi-languages. If values returned from pattern operations are not in English, the returned data cannot be parsed properly and the pattern discovery will fail.

The discovery and mapping process consists of the following interactions:

1.  An administrator defines an service instance with an entry point for an application CI.

    Service Mapping creates a record for the new service instance in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table.

2.  The device hosting the application is identified.

    1.  Service Mapping checks if the device hosting this application CI exists in the CMDB.
    2.  If the device hosting this application CI does not exist, Service Mapping triggers Discovery to detect host.

        ![Service Mapping checks the CMDB and triggers the horizontal discovery.](../image/DiscoDiscoveryFlowStage1.png)

    3.  Discovery creates the first set of probes for port discovery, referred to as Shazzam probes, and places them as a discovery request in the External Communication Channel \(ECC\) queue.
    4.  The MID Server checks the ECC queue and retrieves the discovery request assigned to it.
    5.  The MID Server runs the probes against the host and discovers open ports.

        ![Discovery uses the ECC Queue to run probes by the MID Server.](../image/DiscoDiscoveryFlowStage2.png)

    6.  The MID Server passes information on the host ports to the ECC queue.
    7.  Discovery checks the ECC queue and receives information on the host ports.

        ![The MID Server passes the information to the ECC queue for Discovery to collect.](../image/DiscoDiscoveryFlowStage3.png)

    8.  These steps are repeated for other types of probes: classification, identification, and exploration.
    9.  Discovery adds the host to the CMDB.

        ![Discovery adds the host to the CMDB.](../image/DiscoDiscoveryFlowStage4.png)

    10. During the host discovery using probes, Service Mapping checks the ECC queue if this process is complete. When the host discovery is complete, Service Mapping checks whether this host exists in the CMDB.
    **Note:** For the detailed description of the horizontal discovery flow, refer to [Horizontal discovery process flow with probes and sensors](../../discovery/concept/c_DiscoProcessFlows.md).

3.  Once the host is found in the CMDB, Service Mapping discovers the application running on this host.
    1.  Service Mapping creates an application discovery request for the IP address of the entry point. It then writes the request in the ECC queue and assigns a MID Server to the request.
    2.  The MID Server checks the ECC queue and retrieves the discovery request assigned to it.
    3.  The MID Server starts running identification sections of the patterns associated with the classifier to find the match for the entry point. When the identification section matches the entry point, the pattern discovers a CI.

        ![Service Mapping places patterns to run by the MID Server.](../image/SMDiscoveryFlowStage2.png)

    4.  The MID Server starts running connectivity sections of the pattern to find outgoing connections of the newly discovered CI.
    5.  The MID Server passes information on the discovered CI, its attributes, and connections to the ECC queue.
    6.  Service Mapping checks the ECC queue and receives information on the newly discovered CI.

        Whenever Service Mapping checks the ECC queue and receives information on a discovered CI, it checks these tables for any data on outbound connections related to the CI: the cmdb\_tcp and sa\_flow\_connection tables. If these two tables contain unique data that patterns did not discover, Service Mapping enriches the information about the CI connections and adds them to the map.

    7.  Service Mapping writes the information into the CMDB and adds this CI to the service instance map.

        ![Service Mapping pulls the information about a CI from the ECC queue and writes it into the CMDB.](../image/SMDiscoveryFlowStage3.png)

    8.  Service Mapping creates the discovery requests for all applications to which the newly discovered CI connects. Mapping is complete after Service Mapping maps a CI that either does not have any outbound connections or is marked as a boundary. A boundary makes Service Mapping stop discovery from this point and not follow outgoing connections.
4.  The system regularly runs the service recomputation to query the CMDB for the latest CI changes, add data for network and storage paths, and apply CI impact rules.

**Related topics**  


[Service instances \(Application services\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/application-services.md)

[The ECC queue for Discovery](../../discovery/reference/r_DiscoveryStatusECCQueue.md)

[Horizontal discovery process flow with probes and sensors](../../discovery/concept/c_DiscoProcessFlows.md)

[Traffic-based discovery in Service Mapping](traffic-based-discovery.md)

