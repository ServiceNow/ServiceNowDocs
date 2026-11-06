---
title: OCI Autonomous DB pattern-based discovery
description: Discovery and Service Mapping Patterns finds Autonomous Databases \(DB\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-autonomous-db-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-10-28"
reading_time_minutes: 2
keywords: [Oracle OCI - Autonomous DB \(LP\), OCI Autonomous DB, OCI discovery, Oracle patterns]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI Autonomous DB pattern-based discovery

Discovery and Service Mapping Patterns finds Autonomous Databases \(DB\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the REST API permissions**

    Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Autonomous DB \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the database in the format **&lt;database name&gt;@&lt;display name&gt;**.|
|Object ID \[object\_id\]|Unique identifier of the Autonomous Database.|
|Version \[version\]|Version of the database.|
|Type \[type\]|Type of the database in the format **Oracle Autonomous - &lt;workload type&gt;**.|
|Vendor \[vendor\]|References the Company \[core\_company\] table.|
|State \[state\]|State of the database, based on its lifecycle state in OCI. The value is either **available** or **terminated**.|
|Comments \[comments\]|Account ID, datacenter name, and pattern ID, separated by underscores.|
|Install Status \[install\_status\]|Install status of the database, based on its lifecycle state in OCI.|
|Operational status \[operational\_status\]|Operational status of the resource. The default value is **Operational**.|

## CI relationships and references

The Oracle OCI - Autonomous DB \(LP\) pattern creates the following relationships and references to support OCI Autonomous DB discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Vendor \[vendor\]|Company \[core\_company\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## OCI tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

