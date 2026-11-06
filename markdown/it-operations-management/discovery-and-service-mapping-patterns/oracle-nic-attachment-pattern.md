---
title: OCI NIC attachment pattern-based discovery
description: Discovery and Service Mapping Patterns finds OCI virtual network interface cards \(VNICs\) attachment records in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-nic-attachment-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-07-12"
reading_time_minutes: 2
keywords: [Oracle OCI NIC Attachment, Oracle discovery, OCI NIC Attachment patterns, VNIC Attachment discovery]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI NIC attachment pattern-based discovery

Discovery and Service Mapping Patterns finds OCI virtual network interface cards \(VNICs\) attachment records in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the REST API permissions**

    Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - NIC Attachment \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|VNIC attachment identifier, set to the attachment ID.|
|Object ID \[object\_id\]|Unique identifier, allocated by OCI for this resource.|
|Install Status \[install\_status\]|Install status of the resource. Default value is **Installed**.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is **Operational**.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique identifier, allocated by OCI for this resource.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Subnet identifier, set to the subnet ID.|
|Object ID \[object\_id\]|Unique identifier, allocated by OCI for this resource.|

## CI relationships

The Oracle OCI - NIC Attachment \(LP\) pattern creates the following relationships to support OCI NIC attachment discovery.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Subnet Endpoint \[cmdb\_ci\_endpoint\_subnet\]|
|Subnet Endpoint \[cmdb\_ci\_endpoint\_subnet\]|Implement End Point To::Implement End Point From|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

