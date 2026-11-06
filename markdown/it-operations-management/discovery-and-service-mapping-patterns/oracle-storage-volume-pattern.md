---
title: OCI storage volume pattern-based discovery
description: Discovery and Service Mapping Patterns finds OCI storage volumes in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-storage-volume-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-07-12"
reading_time_minutes: 2
keywords: [Oracle OCI Storage Volume, Oracle discovery, Oracle patterns, storage volume pattern]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI storage volume pattern-based discovery

Discovery and Service Mapping Patterns finds OCI storage volumes in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the REST API permissions**

    Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Storage Volume \(LP\) pattern.

<table id="table_mkf_2hc_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Display name of the storage volume.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier, allocated by OCI for this resource.

</td></tr><tr><td>

Volume ID \[volume\_id\]

</td><td>

Unique identifier for the storage volume.

</td></tr><tr><td>

Size \[size\]

</td><td>

Size of the storage volume, in gigabytes.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

Size of the storage volume, in bytes.

</td></tr><tr><td>

State \[state\]

</td><td>

Current state of the storage volume. For example: available or terminated.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is **Installed**.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is **Operational**.

</td></tr></tbody>
</table>## CI relationships and references

The Oracle OCI - Storage Volume \(LP\) pattern creates the following relationships and references to support OCI storage volume discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Storage Volume \[cmdb\_ci\_storage\_volume\]|

## OCI tag discovery

The Oracle OCI - Storage Volume \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Storage Volume \[cmdb\_ci\_storage\_volume\] table.|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

