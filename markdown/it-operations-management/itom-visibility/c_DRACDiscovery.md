---
title: Dell Remote Assistant Card discovery
description: The Dell Remote Assistant Card \(DRAC\) and Integrated Remote Assistance Card \(iDRAC\) provide users with tools and functionality to monitor, troubleshoot, and repair servers. You can generate DNS URLs to access out-of-band devices when security prevents access from IP addresses.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-11"
reading_time_minutes: 2
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Dell Remote Assistant Card discovery

The Dell™ Remote Assistant Card \(DRAC\) and Integrated Remote Assistance Card \(iDRAC\) provide users with tools and functionality to monitor, troubleshoot, and repair servers. You can generate DNS URLs to access out-of-band devices when security prevents access from IP addresses.

To identify the DRAC, Discovery uses the **SNMP – DRAC** probe. This probe uses SNMPv1 and SMNPv2c. Out-of-band devices have a dedicated management channel for device maintenance. System administrators can remotely monitor and manage devices with the dedicated management channel, including hardware sensor monitoring, access to local media drives, or adjusting BIOS settings. DNS URLs can be generated for out-of-band devices to access the out-of-band device page when the SSL certificate forbids navigating through the IP address.

## Prerequisites

-   **Create SNMP credentials**

    SNMP credentials are required to discover DRAC devices. For more information, see [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Run network discovery**

    For information on configuring and running network discovery to discover DRAC devices, see [Run network Discovery](c_NetworkDiscovery.md#).


## Data collected

|Label|Table|Name|Command|
|-----|-----|----|-------|
|Firmware version|cmdb\_ci\_outofband\_device|firmware\_version|SNMP walk: drsFirmwareVersion \(racFirmwareVersion for iDRAC7\)|
|Host \*|cmdb\_ci\_outofband\_device|host|SNMP walk: drsSystemServiceTag \(systemServiceTag for iDRAC7\)|
|IP Address|cmdb\_ci\_outofband\_device|ip\_address|DNS probe|
|Name|cmdb\_ci\_outofband\_device|name|SNMP Identity probe|
|Product version|cmdb\_ci\_outofband\_device|product\_version|SNMP walk: drsProductVersion \(racVersion for iDRAC7\)|
|Type|cmdb\_ci\_outofband\_device|type|SNMP walk: drsProductType \(racType for iDRAC7\)|
|URL|cmdb\_ci\_outofband\_device|url|SNMP walk: drsProductURL \(racURL for iDRAC7\)|

\* **Host** is a reference to the cmdb\_ci\_computer table via the serial number. For the cmdb\_ci\_outofband\_device.host field to be populated correctly, the host machine must be discoverable or exist within the CMDB with the appropriate serial number.

## Out-of-band devices

A **DNS URL** is generated for configuration items in the **Out-Of-Band Device** list if the configuration item has a **Name** and **DNS Domain**. The **DNS URL** enables you to access the out-of-band device page when the SSL certificate forbids navigating through the **IP URL**. The **DNS URL** has the format `https://Name.DNS_Domain`. If either the **Name** or **DNS Domain** field is empty, the **DNS URL** contains the value in the **URL** field.

**Parent Topic:**[Network device discovery](c_NetworkDevices.md)

