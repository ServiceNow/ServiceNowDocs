---
title: How CIM Discovery works
description: This is the processing flow for classifying Common Information Model \(CIM\) storage systems.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Storage Discovery via SMI-S and CIM, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# How CIM Discovery works

This is the processing flow for classifying Common Information Model \(CIM\) storage systems.

## Processing flow

1.  The Shazzam probe launches the wbem port probe as part of network discovery.
2.  The wbem port probe detects activity on target ports SLP 427, CIM 5989 and 5988, and then examines the **Service Registry Queries** related list, at **Discovery Definition** &gt; **Port Probes**, for the SLP query. The base system provides this query to detect the service:wbem service type, which indicates the presence of an SLP server.
3.  The Shazzam probe launches a scanner for the WBEM service type. The scanner retrieves:
    -   The attributes of the service from the SLP server.
    -   The interop namespaces of CIM servers in the network.
4.  The scanner appends the namespace values it finds to the port probe results.
5.  The wbem port probe appends the SLP data it carries to the CIM Classify probes.
6.  The CIM Classify probe uses that information to explore the CIM servers.

    ![CIM Shazzam Processing Diagram](../image/CIMShazzamProcessingDiagram.png "CIM Shazzam Processing Diagram")


## The wbem port Probe

The **wbem** probe stores the data it retrieves in the CIM Classification `[discovery_classy_cim]` table. To view the wbem port probe, navigate to **Discovery Definition** &gt; **Port Probes**.

![wbem port probe record](../image/wbemPortProbe.png "wbem port probe record")

## SLP query

The SLP query detects the wbem service \(service:wbem\) on an SLP server and gathers the attributes of the service. To view the SLP Query record, open the wbem port probe record and select **SLP Query** from the **Service Registry Queries** related list.

![SLP Query record](../image/SLPQuery.png "SLP Query record")

## CIM - Classify probe

The wbem port probe appends the SLP data it carries, including namespaces, to the CIM - Classify probe before launching it. The CIM classification probe extracts VMware ESX serial numbers and connector relationships between the SAN and NAS components from CIM Servers in the network.

To access the CIM classification probe, navigate to **Discovery Definition** &gt; **Probes** and select **CIM - Classify** from the list of probes.

**Note:**

The mid.cim.interop.namespace system property defines four default storage namespaces:

-   interop
-   root/interop
-   root/pg\_interop
-   pg\_interop

If you’re using multiple storage vendors with custom namespaces not specified as one of the defaults, add the new namespaces to the comma-separated list in this property. If you intend to continue using any of the default namespaces, make sure to include them in the property.

![CIM - Classify probe record](../image/CIMClassifyProbe.png "CIM - Classify probe record")

## SMI-S and CIM probes and sensors

|Probe/Sensor|Description|
|------------|-----------|
|CIM - Identity|Identifies a system via CIM per SMI-S.|
|SMI - Array - Controllers|Retrieves controller information.|
|SMI - Array - Disks|Retrieves storage disk information.|
|SMI - Array - File Shares|Enumerates NAS file shares from a storage server.|
|SMI - Array - Pools|Retrieves storage pools.|
|SMI - Array - Ports|Retrieves storage ports.|
|SMI - Array - Volumes|Retrieves storage volumes.|
|SMI - Fabric|Retrieves SANs, fabrics, zone sets, zones, zone aliases, endpoints, and connections.|
|SMI - Fibre Channel Switch|Retrieves FC switches.|
|SMI - NAS Head - Component Systems|Retrieves all virtual file servers in a NAS head profile.|
|SMI - NAS Head - File Server IPs|Retrieves IP addresses for each NAS file server.|
|SMI - NAS Head - File Servers|Retrieves NAS file servers such as Common Internet File System \(CIFS\) and Network File System \(NFS\).|
|SMI - NAS Head - File Shares|Retrieves file shares for each NAS file server.|
|SMI - Storage Server|Retrieves SAN and NAS arrays and servers.|
|SMI - WBEM Service|Retrieves WBEM Service information such as profiles and SMI-S version.|

**Parent Topic:**[Storage Discovery via SMI-S and CIM](r_DataCollDiscoStorageviaSMISCIM.md)

