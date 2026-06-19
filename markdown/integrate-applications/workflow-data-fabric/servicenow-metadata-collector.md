---
title: ServiceNow metadata collector
description: Provides read-only access to metadata from a ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/servicenow-metadata-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# ServiceNow metadata collector

Provides read-only access to metadata from a ServiceNow instance.

The collector harvests metadata from ServiceNow instances including system applications, application scopes, tables, fields, views, and Data Fabric tables. Catalogs ServiceNow Data Fabric metadata for virtualized data integration.

## Metadata cataloged

The collector catalogs the following information.

<table id="table_a3t_fzx_13c"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

ServiceNow Instance

</td><td>

Instance URL, Connection metadata

</td></tr><tr><td>

System Application

</td><td>

App Name, Vendor, Version, Active status, Short Description, Source Table

</td></tr><tr><td>

Application Scope

</td><td>

Scope Name, Scope Identifier, Vendor, Version, Active status, Source Table

</td></tr><tr><td>

Table

</td><td>

Table Name, Is Extendable, sys\_updated\_on \(timestamp\), Source Table, Parent Table \(for table inheritance\)

</td></tr><tr><td>

Data Fabric Table

</td><td>

Inherits all Table properties, Plus: Association with external DatabaseTable

</td></tr><tr><td>

View

</td><td>

Inherits all Table properties, Plus: View Definition \(SQL definition including source tables and join conditions\)

</td></tr><tr><td>

Field

</td><td>

Field Name, Column Label, Reference Table \(for reference fields\), Mandatory, Is Primary \(for Data Fabric fields\), SQL Type \(for Data Fabric fields\)Enhanced metadata: Field type, Field size, Max length, Nullable \(true/false\), Default value, Internal Type

</td></tr><tr><td>

View Table Mapping

</td><td>

Maps To Table, WHERE clause conditions, Is Left Join, Variable Prefix, Mapping Order

</td></tr><tr><td>

Data Product

</td><td>

Data Product Name, Description, State \(lifecycle status\), Tags, Created By, Created On, Updated On, Source Table

</td></tr><tr><td>

Data Interfaces

</td><td>

Table Name, Is Extendable, sys\_updated\_on \(timestamp\), Source Table, Parent Table \(for table inheritance\)

</td></tr><tr><td>

Vault Data Classification

</td><td>

Classification Name, Description, Classification Type, Parent Classification \(for hierarchical relationships\), Source Table

</td></tr><tr><td>

Dashboard

</td><td>

Name, Description, Active, Certified, UI Generation \(Next Experience or Core UI\), Workspace Visible In, Categories, Users Granted To, Owner, Created By, Last Modified By, Requested By, Created At, Last Modified At

</td></tr><tr><td>

Visualization

</td><td>

Name, Description, Active, Certified, UI Generation, Created By, Last Modified By, Created At, Last Modified At, Granted To, Requested By, Owner

</td></tr><tr><td>

Indicator

</td><td>

Name, Description, Active, Type \(Automated/Formula/Manual/External\), Collection Frequency, Unit, Granted To, Created By, Modified By, Created At, Last Modified At

</td></tr><tr><td>

Indicator Source

</td><td>

Name, Description, Facts Table, Conditions, Collection Frequency, Created By, Last Modified By, Created At, Last Modified At

</td></tr><tr><td>

Dashboard Tab

</td><td>

Name, Display Order, UI Generation

</td></tr><tr><td>

Breakdown

</td><td>

Name, Description, Type \(Automated/Manual/External\), Created By, Last Modified By, Created At, Last Modified At

</td></tr><tr><td>

Breakdown Source

</td><td>

Name, Active, Conditions, Facts Table, Facts Field, Created By, Last Modified By, Created At, Last Modified At

</td></tr><tr><td>

Data Collection Job

</td><td>

Name, Description, Active, Run Type, Run Time, Collect Scope \(scores only, text indexes only, or both\), Created By, Modified By, Created At, Last Modified At

</td></tr></tbody>
</table>## Relationships between objects

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

</td></tr><tr><td>

Vault Data Classification

</td><td>

May have Parent Classification \(via parent classification\), May have Child Classifications, Classifies Fields and Tables \(via has classification\)

</td></tr><tr><td>

Dashboard

</td><td>

Contained within Application Scope, Tabs contained in the Dashboard

</td></tr><tr><td>

Dashboard Tab

</td><td>

Dashboard the Tab is contained within

</td></tr><tr><td>

Data Collection Job

</td><td>

Contained within Application Scope, Indicators the Data Collection Job collects

</td></tr><tr><td>

Indicator

</td><td>

Contained within Application Scope, Data Collection Jobs that collect this Indicator

</td></tr><tr><td>

Indicator Source

</td><td>

Contained within Application Scope

</td></tr><tr><td>

Visualization

</td><td>

Contained within Application Scope

</td></tr><tr><td>

Breakdown

</td><td>

Contained within Application Scope

</td></tr><tr><td>

Breakdown Source

</td><td>

Contained within Application Scope

</td></tr></tbody>
</table>## Lineage for ServiceNow

The following lineage information is collected by the ServiceNow collector:

<table id="table_asy_kyn_33c"><thead><tr><th>

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

Table inheritance lineage: -   Parent table \(via extends table relationship\)
-   Child tables that extend this table

</td></tr><tr><td>

Field

</td><td>

Reference field lineage: -   Fields in other tables that this field references
-   Indicates foreign key relationships

</td></tr><tr><td>

Data Fabric Table

</td><td>

External data source lineage: -   External DatabaseTable from which data is virtualized \(via prov:wasDerivedFrom\)

</td></tr><tr><td>

Data Interfaces

</td><td>

Table inheritance lineage: -   Parent table \(via extends table relationship\)
-   Child tables that extend this table
-   The tables whose structure and attributes this Data Interface governs

</td></tr><tr><td>

Dashboard

</td><td>

Visualizations embedded in the Dashboard, Tables and Fields the Dashboard uses data from, Indicators the Dashboard uses

</td></tr><tr><td>

Dashboard Tab

</td><td>

Visualizations embedded in the Dashboard Tab

</td></tr><tr><td>

Indicator

</td><td>

Indicator Sources the Indicator uses data from, Fields or Tables the Indicator uses data from, Indicators the Indicator calculates values from, Breakdowns that segment Indicator values, Dashboards that use the Indicator, Visualizations that use the Indicator

</td></tr><tr><td>

Indicator Source

</td><td>

Indicators that use the Indicator Source, Table the Indicator Source sourced data from

</td></tr><tr><td>

Breakdown

</td><td>

Breakdown Sources that define segment values for the Breakdown, Tables and Fields the Breakdown segments its values from, Indicators whose values are segmented by the Breakdown

</td></tr><tr><td>

Visualization

</td><td>

Dashboards that embed the Visualization, Dashboard Tabs that embed the Visualization, Indicators the Visualization uses data from, Tables or Fields the Visualization uses data from

</td></tr><tr><td>

Breakdown Source

</td><td>

Breakdowns which the Breakdown Source defines segment values for, Fields it derives elements from

</td></tr></tbody>
</table>## ServiceNow version supported

Supports ServiceNow instances that expose the Table API. Tested with ServiceNow Zurich and Australia releases.

## Authentication supported

The collector authenticates to ServiceNow using Basic Authentication \(User name and Password\).

-   **[Prepare to run the ServiceNow collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-servicenow-collector.md)**  
Create a ServiceNow user and configure permissions before running the collector.
-   **[Create a ServiceNow metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/create-servicenow-metadata-collector.md)**  
Create a collector to import metadata from ServiceNow.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-metadata-collectors-dc.md)

