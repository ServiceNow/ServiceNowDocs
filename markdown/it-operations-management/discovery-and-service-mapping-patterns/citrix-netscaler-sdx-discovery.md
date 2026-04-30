---
title: Citrix NetScaler SDX discovery
description: The ServiceNow Discovery application can discover Citrix NetScaler SDX devices using the Citrix NetScaler SDX pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Citrix NetScaler SDX, NetScaler SDX]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Citrix NetScaler SDX discovery

The ServiceNow Discovery application can discover Citrix NetScaler SDX devices using the Citrix NetScaler SDX pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

You can use this pattern on the ServiceNow AI Platform® starting from the Quebec release.

The new classification mechanism introduced in Quebec triggers the pattern. The classification mechanism prevents the whole probe from failing if a sub probe in a multi-probe fails.​

The classification mechanism includes a new trigger\_probe\_m2m table, which defines which classification probe to trigger in relation to the relevant protocol. For this pattern, it triggers the Interactive Probe Shell over the `ssh` protocol.​

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following applications are installed**
    -   CMDB CI Class Models \(version 1.0.20\)
    -   Discovery and Service Mapping Patterns \(version 1.0.72\)
-   **Create SSH credentials**

    Create SSH credentials for the Citrix NetScaler SDX device. For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   **Verify permissions for the following commands**

    Verify that the Discovery user added in the ServiceNow AI Platform instance can run the following commands:

    |Command|Description|
    |-------|-----------|
    |`show vmdevice`|Get virtual machine \(VM\) instances.|
    |`show hardware`|Provides a quick overview of all configurable settings for the Citrix NetScaler SDX devices.|


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Citrix NetScaler SDX pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Citrix NetScaler SDX device.|
|Serial number \[serial\_number\]|The serial number of the Citrix NetScaler SDX device.|
|IP Address \[ip\_address\]|The IP address of the Citrix NetScaler SDX device.|
|Object ID \[object\_id\]|The CI identifier of the Citrix NetScaler SDX device, which includes the serial\_number and ip\_address​.|
|Description \[short\_description\]|The description of the Citrix NetScaler SDX device.|
|OS Version \[os\_version\]|The version of the Citrix NetScaler SDX device.​|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Citrix NetScaler load balancer​.|
|Serial number \[serial\_number\]|The serial number of the Citrix NetScaler load balancer.|
|IP Address \[ip\_address\]|The IP address of the Citrix NetScaler load balancer​.|

On the Dependency Views map you can see all discovered Citrix NetScaler SDX resources in your organization, and the relationships between them.

![Citrix NetScaler SDX dependency](../image/citrix-netscaler-dependency.jpg)

## CI relationships

These relationships are created to support Citrix NetScaler SDX discovery:

|CI|Relationship|CI|
|---|------------|---|
|Citrix Netscaler \[cmdb\_ci\_lb\_netscaler\]|Registered on::Has registered|Citrix NetScaler SDX \[cmdb\_ci\_citrix\_netscaler\_sdx\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

