---
title: OCI active datacenter pattern-based discovery
description: Discovery and Service Mapping Patterns finds the datacenters \(regions\) that your tenancy is subscribed to in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-active-datacenter-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-10-28"
reading_time_minutes: 2
keywords: [Oracle OCI - Active Datacenters \(LP\), OCI Active Datacenter, OCI discovery, Oracle patterns]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI active datacenter pattern-based discovery

Discovery and Service Mapping Patterns finds the datacenters \(regions\) that your tenancy is subscribed to in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the REST API permissions**

    Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Active Datacenters \(LP\) pattern.

<table id="table_oci_dc_datacenter"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the region that the tenancy is subscribed to. For example: us-phoenix-1.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the datacenter, which is the region name.

</td></tr><tr><td>

Region \[region\]

</td><td>

Name of the region where the datacenter is located.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is **Installed**.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is **Operational**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|Identifier of the cloud account used for discovery.|
|Datacenter Type \[datacenter\_type\]|Type of datacenter that the account belongs to.|
|Datacenter URL \[datacenter\_url\]|URL of the datacenter used for discovery.|
|Discovery credentials \[discovery\_credentials\]|Credentials used to discover the account.|
|Object ID \[object\_id\]|Unique identifier of the cloud account.|
|Organization Id \[organization\_id\]|Oracle Cloud ID \(OCID\) of the tenancy.|

## CI relationships

The Oracle OCI - Active Datacenters \(LP\) pattern creates the following relationship to support OCI active datacenter discovery.

|CI|Relationship|CI|
|---|------------|---|
|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

