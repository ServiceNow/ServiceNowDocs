---
title: Citrix NetScaler SDX discovery
description: The ServiceNow Discovery application can discover Citrix NetScaler SDX devices using the Citrix NetScaler SDX pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/citrix-netscaler-sdx-discovery.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 2
keywords: [Citrix NetScaler SDX, NetScaler SDX]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Citrix NetScaler SDX discovery

The ServiceNow Discovery application can discover Citrix NetScaler SDX devices using the Citrix NetScaler SDX pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The classification mechanism introduced in Quebec triggers the pattern. The classification mechanism prevents the whole probe from failing if a sub probe in a multi-probe fails.​

The classification mechanism includes a trigger\_probe\_m2m table, which defines which classification probe to trigger in relation to the relevant protocol. For this pattern, it triggers the Interactive Probe Shell over the `ssh` protocol.​

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following applications are up to date**
    -   CMDB CI Class Models
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Create SSH credentials**

    Create SSH credentials for the Citrix NetScaler SDX device. For more information, see [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md).

-   **Verify permissions for the following commands**

    Verify that the Discovery user has admin permissions and can run the following commands. The `show hardware` command requires shell access as well.

    |Command|Description|
    |-------|-----------|
    |`show vmdevice`|Get virtual machine \(VM\) instances.|
    |`show hardware`|Provides a quick overview of all configurable settings for the Citrix NetScaler SDX devices.|

    If the Discovery user doesn't have shell access or admin permissions, verify that the user can run the following read-only commands in the NetScaler CLI instead:

    |Command|Description|
    |-------|-----------|
    |`show systemstatus`|Retrieve the current system status of the SDX appliance, including serial number, build number, and product name.|
    |`show hostname`|Retrieve the hostname of the SDX appliance.|


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

\[Omitted image "citrix-netscaler-dependency.jpg"\] Alt text: Citrix NetScaler SDX dependency

## CI relationships

These relationships are created to support Citrix NetScaler SDX discovery:

|CI|Relationship|CI|
|---|------------|---|
|Citrix Netscaler \[cmdb\_ci\_lb\_netscaler\]|Registered on::Has registered|Citrix NetScaler SDX \[cmdb\_ci\_citrix\_netscaler\_sdx\]|

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

