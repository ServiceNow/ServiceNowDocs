---
title: Storage Discovery via SMI-S and CIM
description: Discovery can explore storage devices that contain a Storage Management Initiative Specification \(SMI-S\) provider that is a specialized Common Information Model \(CIM\) server.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Storage discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Storage Discovery via SMI-S and CIM

Discovery can explore storage devices that contain a Storage Management Initiative Specification \(SMI-S\) provider that is a specialized Common Information Model \(CIM\) server.

To see the current list of vendors and products conforming to SMI-S as tested by SNIA, see the [SNIA website](https://www.snia.org/ctp/conforming_providers).

Other types of storage, such as storage that is attached via a host, VM storage that is available on VMware ESX servers, and storage for Kernel VM \(KVM\), use a separate set of probes and sensors.

Discovery collects information about storage area networks \(SAN\) and network-attached storage \(NAS\) from specialized devices, such as storage arrays and Fibre Channel \(FC\) switches. Discovery collects and creates CIs in the CMDB for the following information items:

-   Array disks, pools, and volumes
-   Fibre Channel HBAs, ports, and controllers
-   FC exports
-   Fabrics, including endpoints, zoning, and switches
-   Dependencies between storage sub-components

**Note:** For more information on storage discovery and using the CIM Query tool for troubleshooting, see the knowledge article [KB0782305](https://support.servicenow.com/kb_view.do?sysparm_article=KB0782305).

## Requirements

-   A CIM server using SMI-S 1.4 or later.
-   One or more CIM server per storage vendor.
-   NAS and SAN systems from major vendors such as EMC, Hitachi, HP, and NetApp. SAN storage devices must use FC.
-   FC switches from major vendors such as Brocade and Cisco.
-   The [CIM credentials](https://www.servicenow.com/docs/access?context=r_CIMCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) must be available for SMI-S configuration. The CIM credentials can be different than the credentials for the system hosting the CIM server.
-   Ensure that SMI-S is enabled for your storage product.
-   Ensure the connectivity between the MID Server and CIM server.
-   New CIM credentials need to be configured in the instance. CIM server credentials could be different from the system hosting the prerequisite CIM server.

**Note:** Because the SMI-S Provider caches storage device information, the Discovery query to the provider does not affect storage device performance.

## SMI-S Discovery architecture

![SMI-S Discovery](../image/SMI-S_DiscoveryDiagram.png)

## CIM architecture

CIM probes can explore any device based on the Common Information Model \(CIM\) by querying a CIM server, also referred to as a CIMOM - Common Information Model Object Manager. By default, Discovery uses CIM probes to explore storage systems as well as to get the serial numbers of ESX servers.

Discovery queries SMI-S compliant storage devices using CIMIQL queries.

The following components are part of CIM:

-   Common Information Model \(CIM\): CIM allows multiple parties to exchange information about managed elements. CIM represents these managed elements and the management information, while providing the mechanism to actively control and manage the elements.
-   Storage Management Initiative Specification \(SMI-S\): SMI-S is a standard of use that describes methods for storage discovery on the vendor's side. ServiceNow uses SMI-S to determine how to discover CIM. SMI-S is based on the Common Information Model \(CIM\) and the Web-Based Enterprise Management \(WBEM\) standards, which define management functionality via HTTP. The main objective of SMI-S is to enable management of dissimilar storage products. ServiceNow supports SMI-S version 1.4 or higher.

    ![CIM SMI-S Standard Diagram](../image/CIMSMISStandardDiagram.png "CIM SMI-S Standard Diagram")

-   Web-Based Enterprise Management \(WBEM\): WBEM defines a particular implementation of CIM, including protocols for discovering and accessing each CIM implementation.
-   Service Location Protocol \(SLP\): SLP is an ad hoc protocol for retrieving and associating configuration information about CIM servers, such as default paths, capabilities, and the exact interop namespace. Discovery retrieves the interop namespace of a CIM server via SLP and passes that information to the CIM Classify probe. SLP, referred to here as the SLP server, uses service agents \(SA\) to gather and disseminate information about a CIM server on a subnet. A subnet can have multiple service agents.

    **Note:**

    The mid.cim.interop.namespace system property defines four default storage namespaces:

    -   interop
    -   root/interop
    -   root/pg\_interop
    -   pg\_interop
    If you’re using multiple storage vendors with custom namespaces not specified as one of the defaults, add the new namespaces to the comma-separated list in this property. If you intend to continue using any of the default namespaces, make sure to include them in the property.

    ![CIM Agents Diagram](../image/CIMAgentsDiagram.png "CIM Agents Diagram")


## SLP and WBEM support

SLP is required for CIM Discovery as it is part of the Storage Management Initiative Specification \(SMI-S\) stack. Some storage devices may support the WBEM protocol, but may not support SLP.

You can manually register the WBEM services on SLP using a common Linux tool like **slptool**. This tool has a command line interface that you can use to make SLPv2 User Agent \(UA\) requests, which usually come with the SLP daemon package. To register a service, provide a URL and list of attributes. An example can be extracted from a working SLP server by using the same tool.

## Storage Discovery table schema

This diagram displays the disk hierarchical schema for storage Discovery.

![Disk hierarchical schema](../image/StorageSchemaFuji.png "Disk hierarchical schema")

## Storage Discovery tables and probes

Discovery uses the following tables and probes to gather information about storage devices that are managed by a SMI-S provider.

|Table|Probe|
|-----|-----|
|Disk \[cmdb\_ci\_disk\]|SMI 1.5 - Storage Server|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|SMI 1.5 - Storage Server|
|Fibre Channel Port \[cmdb\_ci\_fc\_port\]|SMI 1.5 - Storage Server|
|SAN Export \[cmdb\_ci\_san\_export\]|SMI 1.5 - Storage Server|
|Storage Controller \[cmdb\_ci\_storage\_controller\]|SMI 1.5 - Storage Server|
|Storage Export \[cmdb\_ci\_storage\_export\]|SMI 1.5 - Storage Server|
|Storage File Share \[cmdb\_ci\_storage\_fileshare\]|SMI - Array - File Shares|
|Storage Pool \[cmdb\_ci\_storage\_pool\]|SMI 1.5 - Storage Server|
|Storage Server \[cmdb\_ci\_storage\_server\]|CIM - Identity|
|Storage Switch \[cmdb\_ci\_storage\_switch\]|CIM - Identity|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|SMI 1.5 - Storage Server|
|Storage Device \[cmdb\_ci\_storage\_device\]|SMI 1.5 - Storage Server|
|Storage Area Network \[cmdb\_ci\_san\]|SMI - Fabric|
|SAN Connection \[cmdb\_ci\_san\_connection\]|SMI - Fabric|
|SAN Endpoint \[cmdb\_ci\_san\_endpoint\]|SMI - Fabric|
|SAN Fabric \[cmdb\_ci\_san\_fabric\]|SMI - Fabric|
|SAN Zone \[cmdb\_ci\_san\_zone\]|SMI - Fabric|
|SAN Zone Alias \[cmdb\_ci\_san\_zone\_alias\]|SMI - Fabric|
|SAN Zone Alias Member \[cmdb\_ci\_san\_zone\_alias\_member\]|SMI - Fabric|
|SAN Zone Member \[cmdb\_ci\_san\_zone\_member\]|SMI - Fabric|
|SAN Zone Set \[cmdb\_ci\_san\_zone\_set\]|SMI - Fabric|

These probes are available but not currently used:

-   SMI - Storage Server
-   SMI - Array - Controllers
-   SMI - Array - Disks
-   SMI - Array - Pools
-   SMI - Array - Ports
-   SMI - Array - Volumes

-   **[Discovery of storage area networks \(SAN\)](storage-area-networks.md)**  
Discovery collects information about storage area networks from specialized devices, such as storage arrays and Fibre Channel \(FC\) switches, and creates specific references between the tables in the SAN schema.
-   **[How CIM Discovery works](r_HowCIMDiscoveryWorks.md)**  
This is the processing flow for classifying Common Information Model \(CIM\) storage systems.
-   **[Configure SMI-S Provider for storage Discovery](../task/t_ConfigDiscoForStandaloneStorage.md)**  
Use this procedure for configuring a standalone storage device with the required SMI-S Provider for Discovery.
-   **[Data collected by Discovery on storage devices](r_DataCollDiscoStorageDevices.md)**  
Discovery identifies and classifies information about storage devices.

**Parent Topic:**[Storage discovery](../concept/c_Storage.md)

