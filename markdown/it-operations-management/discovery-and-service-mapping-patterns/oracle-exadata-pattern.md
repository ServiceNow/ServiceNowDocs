---
title: Oracle Exadata cloud as a service pattern-based discovery
description: Discovery and Service Mapping Patterns finds Oracle Exadata resources in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-exadata-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 2
keywords: [Oracle OCI - Exadata \(LP\), Exadata database, OCI discovery, Oracle patterns]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Exadata cloud as a service pattern-based discovery

Discovery and Service Mapping Patterns finds Oracle Exadata resources in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the REST API permissions**

    Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Exadata \(LP\) pattern.

<table id="table_exadata_cloud_database"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the database.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Oracle Cloud Identifier \(OCID\) of the database.

</td></tr><tr><td>

Vendor \[vendor\]

</td><td>

Vendor of the database. The value is set to **ORACLE**.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of the database. The value is **Oracle Exadata - &lt;workload type&gt;**, where the workload type is the database workload returned by the Oracle Database Service.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of the Oracle Database software.

</td></tr><tr><td>

State \[state\]

</td><td>

Current state of the database.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. The default value is **Installed**.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. The default value is **Operational**.

</td></tr><tr><td>

Comments \[comments\]

</td><td>

Account ID and identifier of the pattern, separated by an underscore.

</td></tr></tbody>
</table>## CI relationships and references

The Oracle OCI - Exadata \(LP\) pattern creates the following relationships and references to support OCI Exadata discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Uses::Used by|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## OCI tag discovery

The pattern extension section collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

