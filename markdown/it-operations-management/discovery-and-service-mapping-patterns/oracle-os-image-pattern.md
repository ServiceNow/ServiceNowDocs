---
title: OCI OS image pattern-based discovery
description: Discovery and Service Mapping Patterns finds OCI OS images on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/oracle-os-image-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-07-12"
reading_time_minutes: 2
keywords: [Oracle OCI - Image \(LP\), Oracle OCI - Cloud OS Image \(LP\), Oracle OS image, Oracle OCI discovery, Oracle patterns]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI OS image pattern-based discovery

Discovery and Service Mapping Patterns finds OCI OS images on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern overview

Discovery uses the Oracle OCI - Image \(LP\) pattern to discover OCI OS images from your Oracle account.

When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. When enabled, Discovery launches the Oracle OCI - Cloud OS Image \(LP\) pattern, which populates the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/enable-cloud-os-image-discovery-pattern.md).

## Pattern-based discovery and mapping requirements

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the OCI OS image patterns.

<table id="table_mkf_2hc_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the image resource.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier, allocated by Oracle Cloud Infrastructure for this resource.

</td></tr><tr><td>

Guest OS \[guest\_os\]

</td><td>

Operating system type of the image.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of the operating system.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **OCI**. This field is only populated in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>## CI relationships and references

The OCI OS image patterns create the following relationships and references to support OCI OS image discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|

## OCI Tag discovery

The OCI OS image patterns collect tags and populate them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

