---
title: OCI cloud hardware type pattern-based discovery
description: Discovery and Service Mapping Patterns finds OCI cloud hardware types \(called shapes in OCI\) in your Cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-hardware-type-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-22"
reading_time_minutes: 1
keywords: [Oracle OCI, Cloud Hardware Type, shapes, Oracle discovery, Oracle patterns]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI cloud hardware type pattern-based discovery

Discovery and Service Mapping Patterns finds OCI cloud hardware types \(called shapes in OCI\) in your Cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Cloud Hardware Type \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the shape.|
|Object ID \[object\_id\]|Name of the shape.|
|VCPUs \[vcpus\]|Number of virtual CPUs \(vCPU\) available to the shape.|
|Memory \(MB\) \[memory\_mb\]|Amount of memory available to the shape, in megabytes \(MB\).|
|Cores \[cores\]|Number of physical cores available to the shape.|
|Provider \[provider\]|Cloud provider, which is **OCI**.|

## CI relationships and references

The Oracle OCI - Cloud Hardware Type \(LP\) pattern creates the following relationships to support OCI cloud hardware type discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

