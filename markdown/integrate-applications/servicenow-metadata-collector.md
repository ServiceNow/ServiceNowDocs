---
title: ServiceNow metadata collector
description: Provides read-only access to metadata from a ServiceNow instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# ServiceNow metadata collector

Provides read-only access to metadata from a ServiceNow instance.

The collector harvests metadata from ServiceNow instances including system applications, application scopes, tables, fields, views, and Data Fabric tables. Catalogs ServiceNow Data Fabric metadata for virtualized data integration.

## Metadata cataloged

The collector catalogs the following information.

|Object|Information cataloged|
|------|---------------------|
|ServiceNow Instance|Instance URL, Connection metadata|
|System Application|App Name, Vendor, Version, Active status, Short Description, Source Table|
|Application Scope|Scope Name, Scope Identifier, Vendor, Version, Active status, Source Table|
|Table|Table Name, Is Extendable, sys\_updated\_on \(timestamp\), Source Table, Parent Table \(for table inheritance\)|
|Data Fabric Table|Inherits all Table properties, Plus: Association with external DatabaseTable|
|View|Inherits all Table properties, Plus: View Definition \(SQL definition including source tables and join conditions\)|
|Field|Field Name, Column Label, Internal Type, Max Length, Reference Table \(for reference fields\), Mandatory, Is Primary \(for Data Fabric fields\), SQL Type \(for Data Fabric fields\)|
|View Table Mapping|Maps To Table, WHERE clause conditions, Is Left Join, Variable Prefix, Mapping Order|
|Data Product|Data Product Name, Description, State \(lifecycle status\), Tags, Created By, Created On, Updated On, Source Table|
|Data Interfaces|Table Name, Is Extendable, sys\_updated\_on \(timestamp\), Source Table, Parent Table \(for table inheritance\)|

## Relationships between objects

Catalog pages show relationships between the following data asset types:

|Data asset page|Relationship|
|---------------|------------|
|ServiceNow Instance|Contains Application Scopes, System Applications, Tables, Data Interfaces|
|System Application|Contained within Application Scope|
|Application Scope|Contains System Applications and Tables \(via has scoped data asset\), Data Interfaces|
|Table|Contained within Application Scope, Has Fields, May extend another Table \(via extends table\), May be extended by child Tables|
|Data Fabric Table|Inherits all Table relationships, Plus: Derived from external DatabaseTable \(via prov:wasDerivedFrom\)|
|View|Inherits all Table relationships, Has View Table Mappings|
|Field|Belongs to a Table \(via has field\), May reference another Field \(for reference/foreign key fields\)|
|View Table Mapping|Belongs to a View \(via has view table mapping\), Maps To Table \(via maps to table\), Selects data from Table|
|Data Product|Contained within Application Scope, Has Data Content \(contains Tables and Views\)|
|Data Interface|Contained within Application Scope, Has Fields, May extend another Table \(via extends table\), May be extended by child Tables|

## Lineage for ServiceNow

The following lineage information is collected by the ServiceNow collector.

<table id="table_kzr_31y_13c"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

View

</td><td>

View Table Mappings show: -   JOIN conditions and WHERE clauses
-   Tables from which the view selects data
-   Variable prefixes and mapping order

</td></tr><tr><td>

Table

</td><td>

Table inheritance lineage: -   Parent table \(via extended table relationship\)
-   Child tables that extend this table

</td></tr><tr><td>

Field

</td><td>

Reference field lineage: -   Fields in other tables that this field references
-   Indicates foreign key relationships

</td></tr><tr><td>

Data Fabric Table

</td><td>

External data source lineage. External DatabaseTable from which data is virtualized \(via prov:wasDerivedFrom\)

</td></tr><tr><td>

Data Interfaces

</td><td>

Table inheritance lineage: -   Parent table \(via extended table relationship\)
-   Child tables that extend this table
-   The Tables whose structure and attributes this Data Interface governs

</td></tr></tbody>
</table>## ServiceNow version supported

Supports ServiceNow instances that expose the Table API. Tested with ServiceNow Zurich and Australia releases.

## Authentication supported

The collector authenticates to ServiceNow using Basic Authentication \(User name and Password\).

-   **[Prepare to run the ServiceNow collector](../task/prepare-to-run-servicenow-collector.md)**  
Create a ServiceNow user and configure permissions before running the collector.
-   **[Create a ServiceNow metadata collector](../task/create-servicenow-metadata-collector.md)**  
Create a collector to import metadata from ServiceNow.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

