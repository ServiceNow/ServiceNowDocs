---
title: Data collected by ITOM Visibility
description: ITOM Visibility collects unique data for each type of device and stores it in dedicated tables, fields, and relationships.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 12
breadcrumb: [ITOM Visibility, IT Operations Management]
---

# Data collected by ITOM Visibility

ITOM Visibility collects unique data for each type of device and stores it in dedicated tables, fields, and relationships.

## Operating system

<table id="table_hms_x3x_2bb"><tbody><tr><td align="left">

![](../image/ComputersServers.png)

</td><td>

[Operating system](../concept/c_Computers.md)

 Find servers and computers based on the machine's operating system:

-   [Windows](r_DataCollDiscoWindowsComputers.md)
-   [Solaris](r_DataCollDiscoSolarisComputers.md)
-   [Linux](r_DataCollDiscoLinuxComputers.md)
-   [Mac \(OS/X\) discovery](r_DataCollDiscoMacOSXComputers.md)
-   [HP-UX](r_DataCollDiscoHPUXComputers.md)
-   [AIX](r_DataCollDiscoAIXComputers.md)

</td></tr></tbody>
</table>## Virtualization

<table id="table_nqj_1lj_lnb"><tbody><tr><td>

![](../image/OperatingSystemLevelVirtualization.png)

</td><td>

[Virtualization](../concept/c-oslv-discovery.md)

 Collect information on deployments that include virtualization:

-   [Hyper-V discovery](r_DiscoveryForHyperV.md#)
-   [IBM Virtualization](../../service-mapping/reference/ibm-hmc-discovery.md)
-   [Red Hat Virtualization](../../service-mapping/reference/red-hat-virtualization-discovery.md)
-   [Nutanix Acropolis](../../service-mapping/reference/nutanix-pattern.md)
-   [VMware vCenter](r_VCenterDataCollected.md)
-   [OpenStack Virtualization](../../service-mapping/reference/openstack-discovery.md)

</td></tr></tbody>
</table>## Cloud

<table id="table_zvp_5kj_lnb"><tbody><tr><td>

![](aaa434f74ca9d21636447cfbf7b0cb8749eb4ec8.png)

</td><td>

[Cloud](../concept/cloud-discovery-wizard.md)

 -   [Data collected for Amazon AWS Cloud Discovery](cloud-disco-aws-data-collected.md)
-   [Microsoft Azure](../concept/azure-cloud-discovery.md)
-   [Google Cloud Platform \(GCP\)](../../service-mapping/reference/google-gcp-discovery-pattern.md)
-   [IBM cloud](../concept/ibm-cloud-discovery.md)
-   [VMware cloud](../concept/vmware-cloud-discovery.md)

</td></tr></tbody>
</table>## Containers

<table id="table_gj4_5kj_lnb"><tbody><tr><td>

![](../image/Containers.png)

</td><td>

Containers

 -   [Kubernetes and OpenShift](../../service-mapping/concept/kubernetes-discovery.md)
-   [Amazon ECS resource discovery](../../service-mapping/reference/aws-ecs-fargate-discovery.md)
-   [Pivotal Cloud Foundry discovery](../../service-mapping/concept/pivotal-cloud-foundry.md)

</td></tr></tbody>
</table>## Software

<table id="table_azl_5kj_lnb"><tbody><tr><td>

![](../image/Software.png)

</td><td>

[Software](../concept/c_Software.md)

 Find a variety of software, including:

-   [Apigee Edge](../../service-mapping/concept/apigee-edge-discovery.md)
-   [ColdFusion](../../service-mapping/concept/cold-fusion-discovery.md)
-   [HP Operations Manager](r-HPOP.md)
-   [IBM Websphere DataPower](data-coll-datapower.md)
-   [JBOSS on Windows and Linux](../concept/c_DataCollDiscoJBossServers.md)
-   Web and email servers, including [Microsoft IIS](r_DataCollDiscoMicrosoftIISServers.md), [Apache](r_DataCollDiscoApacheWebServers.md#), [Tomcat](r_DataCollDiscoTomcatServers.md), [Exchange mailbox](r-ExchangeMailBox.md)
-   [Puppet automation](../concept/c_PuppetAutomationSoftwareDiscovery.md) software
-   [Red Hat JBoss Fuse](../../service-mapping/concept/jboss-fuse-discovery.md)
-   [SAP applications](../../service-mapping/concept/sap-discovery.md#)
-   [WebLogic](../concept/c_DataCollDiscoWebLogicServers.md) and [WebSphere](../concept/c_DataCollDiscoWebSphereServers.md) servers
-   [General software](r_DataCollDiscoGenSWPkg.md)

</td></tr></tbody>
</table>## Clustered applications

<table id="table_c4b_5kj_lnb"><tbody><tr><td>

![](../image/Clusters.png)

</td><td>

[Clustered applications](../concept/c_ClusteredAppDiscoveryOnWindows.md#)

 -   [IBM PowerHA Cluster \(HACMP\)](../../service-mapping/reference/ibm-powerha-hamcp-discovery.md)
-   [Linux Red Hat cluster](../concept/red-hat-cluster-discovery.md)
-   [Veritas Cluster Server discovery](../../service-mapping/concept/veritas-cluster-server-discovery.md)
-   [Windows server cluster](r_WindowsServerClusterDiscovery.md)

</td></tr></tbody>
</table>## Databases

<table id="table_xfr_rkj_lnb"><tbody><tr><td>

![](../image/NewDatabase.png)

</td><td>

[Databases](../concept/database-discovery.md)

 Discover databases, including:

-   [Oracle](../concept/c_OracleDatabaseDiscovery.md)
-   [MySQL](../concept/c_MySQLDiscovery.md)
-   [Microsoft SQL](mssql-data-collected-pattern.md#)
-   [MongoDB](r_DiscoverMongoDBInstances.md)
-   [SAP HANA](../../service-mapping/concept/sap-discovery.md#)
-   [PostgreSQL](r_DiscoverPostgreSQLInstances.md)
-   [Sybase](r-Sybase.md)
-   [Amazon DynamoDB](../../service-mapping/concept/aws-dynamoDB-discovery.md)
-   [Oracle Database 12c](../../service-mapping/reference/oracle-cdb-pdb-discovery.md)

</td></tr></tbody>
</table>## Network devices

<table id="table_qf5_pkj_lnb"><tbody><tr><td>

![](../image/NetworkDevices.png)

</td><td>

[Network devices](../concept/c_NetworkDevices.md)

 -   [Routers and switches](r_DataCollDiscoNWRouteAndSwitch.md)
-   [Load balancers:](../concept/c_LoadBalancers.md)
    -   [A10](r_DataCollDiscoA10LoadBalancers.md)
    -   [F5 BIG-IP](../concept/c_LoadBalancerF5BIGIP.md)
    -   [Cisco GSS](../concept/c_LoadBalancerGSS.md)
    -   [Cisco CSS](../concept/c_LoadBalancerCSS.md)
    -   [Citrix NetScaler](../concept/c_LoadBalancerCitrixNetscaler.md)
    -   [HAProxy](../concept/c_LoadBalancerHAProxy.md)
    -   [NGINX](../concept/c_LoadBalancerNGINX.md)
    -   [Alteon](../concept/alteon-load-balancer-discovery.md)
    -   [ACE](../concept/ace-load-balancer-discovery.md)
    -   [Radware-appDirector](../concept/radware-appdirector.md)
    -   [AWS application ELB Service discovery](../../service-mapping/reference/aws-application-elb-service-discovery.md)
-   Firewalls
    -   [Cisco firewall](../../service-mapping/reference/cisco-fw-discovery.md)
    -   [Fortinet firewall](../../service-mapping/reference/fortinet-fw-discovery.md)
    -   [Juniper firewall](../../service-mapping/reference/juniper-fw-discovery.md)
    -   [Palo Alto firewall](../../service-mapping/reference/palo-alto-fw-discovery.md)
-   [IP networks](r_DataCollDiscoIPNetworks.md) and [specific IP addresses](r_DataCollDiscoIPAddress.md)
-   [Cisco UCS devices](r-CiscoUCSHD.md)
-   [Cisco Switch Wireless Access Point \(WAP\)](../../service-mapping/reference/cisco-waps-discovery.md)
-   [Printers](r_DataCollDiscoNetworkPrinters.md) and [power supplies](r_DataCollDiscoUnintPowerSupp.md)
-   [IP services and daemons](r_DataCollDiscoServicesAndDaemons.md)

 You can also find devices based on [TCP connections](r_DataCollDiscoTCPConnections.md) and [Layer-2, SNMP-level](../concept/c_Layer2Discovery.md#) discovery.

</td></tr></tbody>
</table>## Storage

<table id="table_dtq_lkj_lnb"><tbody><tr><td>

![](../image/NewStorage.png)

</td><td>

[Storage](../concept/c_Storage.md)

 Discover these types of storage devices:

-   [Pure Storage FlashBlade](../../service-mapping/concept/pure-storage-discovery.md)
-   [NetApp server](../concept/netapp-discovery.md)
-   [Discovery of storage area networks \(SAN\)](r_DataCollDiscoStorageDevices.md)
-   [Direct Attached Storage \(DAS\)](r_DataCollDiscoStorageDevices.md)
-   [Network Attached Storage \(NAS\)](r_DataCollDiscoStorageDevices.md)
-   [Host bus adapters \(HBA\)](r_DataCollDiscoStorageViaHost.md)
-   [EMC Isilon](../../service-mapping/concept/emc-isilon-discovery.md)

</td></tr></tbody>
</table>