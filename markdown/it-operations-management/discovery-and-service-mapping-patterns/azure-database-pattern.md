---
title: Azure Database pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure databases, including SQL Server, MySQL, PostgreSQL, Redis, and Azure Cosmos DB, in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-database-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 5
keywords: [Azure Database, Azure discovery, Azure SQL, Azure patterns, Database pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Database pattern-based discovery

Discovery and Service Mapping Patterns finds Azure databases, including SQL Server, MySQL, PostgreSQL, Redis, and Azure Cosmos DB, in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/setup-azure-service-accounts.md).

-   **Verify requirements for Azure SQL Managed Instance license discovery**

    Required plugins and applications:

    -   Software Asset Management Professional for Microsoft
    -   Visibility Content

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure DataBase \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the database that you created in Azure.|
|Object ID \[object\_id\]|The identification name of the database.|
|Fully qualified domain name \[fqdn\]|The FQDN that Azure assigned to your database.|
|Type \[type\]|The type of database you created.|
|Version \[version\]|The version of the database.|
|State \[state\]|The state of the database: whether it's Available or Terminated.|
|Vendor \[vendor\]|The vendor name is Azure.|
|Operational status \[operational\_status\]|The operational status of the database, derived from its Azure provisioning state.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Category \[category\]\*|The stock keeping unit \(SKU\) family.|

\* Populated only by the Azure SQL Managed Instance license pattern extension.

|Field|Description|
|-----|-----------|
|Netmask \[netmask\]|Netmask of the Azure database.|

<table id="table_database"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the database in the following format: `<database name>@<server name>`.

</td></tr><tr><td>

Type \[type\]

</td><td>

Database engine type. Possible values: -   Microsoft SQL Server
-   MySQL
-   Postgres SQL
-   Redis
-   DocumentDB

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Unique identifier of the database.

</td></tr><tr><td>

Life Cycle Stage \[life\_cycle\_stage\]

</td><td>

Life cycle stage of the database, derived from its Azure status. For example: Operational or End of Life.

</td></tr><tr><td>

Life Cycle Stage Status \[life\_cycle\_stage\_status\]

</td><td>

Life cycle stage status of the database, derived from its Azure status. For example: In Use or Retired.

</td></tr></tbody>
</table><table id="table_hardware_type"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the hardware type, based on the database SKU.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the hardware type, based on the database SKU name.

</td></tr><tr><td>

vCPUs \[vcpus\]

</td><td>

Number of virtual CPUs, extracted from the SKU name.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

Cloud provider of the hardware type. The value is set to **AZURE**.This field is only populated in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

</td></tr></tbody>
</table>**Note:** When using the Hardware Type \[cmdb\_ci\_compute\_template\] table to store the hardware types, you may notice an unusually large number of records. To avoid this issue, you can store the discovered hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. For more information, see [Enable the Cloud Hardware Type class extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/enable-hardware-type-class-extension.md).

Discovery populates the data in the CMDB when running the Azure SQL Managed Instance license pattern extension.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Object ID of the Azure cloud database.|
|Name \[name\]|SKU name.|
|Cloud Vendor \[cloud\_vendor\]|Cloud vendor of the serverless hardware: **MS Azure**.|
|CPU core count \[cpu\_core\_count\]|Number of virtual cores \(vCores\).|
|CPU core thread \[cpu\_core\_thread\]|Number of vCores.|
|CPU count \[cpu\_count\]|Number of vCores.|
|Category \[category\]|vCore purchasing model.|
|Subcategory \[subcategory\]|SKU tier.|
|Host Type \[host\_type\]|Host type: **PaaS**.|

## CI relationships and references

The Azure DataBase \(LP\) pattern creates the following relationships and references to support Azure database discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Contains::Contained by|Database \[cmdb\_ci\_database\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Database \[cmdb\_ci\_database\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Database \[cmdb\_ci\_database\]|

The Azure SQL Managed Instance license pattern extension creates the following relationships.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Runs on::Runs|Serverless Hardware \[cmdb\_ci\_serverless\_hardware\]|
|Serverless Hardware \[cmdb\_ci\_serverless\_hardware\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## Azure Tag discovery

The Collect Azure DataBase Tags \(LP\) pattern extension collects tags from database servers and databases, and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table \(for server-level tags\) or the Database \[cmdb\_ci\_database\] table \(for database-level tags\).|

## Azure SQL Managed Instance license discovery

The Azure SQL Managed Instance license pattern extension populates the license type in the Key Value \[cmdb\_key\_value\] table.

<table id="table_key_value_license"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

**SQL\_Server\_PaaS\_Managed\_Instance\_License\_Type\_automatic**

</td></tr><tr><td>

Value \[value\]

</td><td>

License type. The following maps the Azure portal license to ServiceNow values: -   Azure Hybrid Benefit: **BYOL**
-   Pay as you go: **License Included**
-   Hybrid Failover rights: **Hybrid Failover**

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.

</td></tr></tbody>
</table>## Connections found by Service Mapping during top-down discovery

The Azure DataBase TD pattern discovers the following connections during top-down discovery: SQL Server, MySQL, PostgreSQL, Redis, and Cosmos DB \(DocumentDB\).

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)

