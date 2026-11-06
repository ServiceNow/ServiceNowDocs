---
title: OCI storage attachment pattern-based discovery
description: Discovery and Service Mapping Patterns finds storage attachments \(volume attachments\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-storage-attachment-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-10-28"
reading_time_minutes: 2
keywords: [Oracle OCI - Storage Attachment \(LP\), Storage Attachment, volume attachment, OCI discovery, Oracle patterns]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI storage attachment pattern-based discovery

Discovery and Service Mapping Patterns finds storage attachments \(volume attachments\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the REST API permissions**

    Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Storage Attachment \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Oracle Cloud Identifier \(OCID\) of the attached block volume.|
|Object ID \[object\_id\]|OCID of the attached block volume.|
|Host \[host\]|OCID of the instance that the block volume is attached to.|
|Install Status \[install\_status\]|Install status of the resource. Default value is **Installed**.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is **Operational**.|

## CI relationships

The Oracle OCI - Storage Attachment \(LP\) pattern creates the following relationships to support OCI storage attachment discovery.

|CI|Relationship|CI|
|---|------------|---|
|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|Implement End Point To::Implement End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

