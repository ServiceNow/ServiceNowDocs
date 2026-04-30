---
title: Extend classes and rules
description: Extend and update CMDB CI Class Models store app classes and rules when using third-party integration tools.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Extend classes and rules

Extend and update CMDB CI Class Models store app classes and rules when using third-party integration tools.

When using a third-party tool to integrate with ServiceNow apps, gaps can occur between the integration and different CIs. Some of the integrated tables and classes may be missing classes and rules not included with the CMDB CI Class Models store app.

The classes and rules in the following table enable you to add and extend the CMDB CI Class Models store app for integrations:

<table id="table_usq_ttl_fnb"><thead><tr><th>

Table

</th><th>

Extends

</th><th>

Rules and related entries

</th></tr></thead><tbody><tr><td rowspan="3">

Postgresql Schema

 cmdb\_ci\_postgresql\_schema

</td><td rowspan="3">

cmdb\_ci\_db\_catalog

</td><td>

Containment rule:cmdb\_ci\_db\_postgresql\_instance-&gt;Contains:Contained By-&gt;cmdb\_ci\_postgresql\_schema

</td></tr><tr><td>

Identification Rule:

 Dependent, Attributes: name

</td></tr><tr><td>

Related Entries \(cmdb\_related\_entry\):

 -   Identifier: cmdb\_ci\_postgresql\_schema
-   Related table: cmdb\_key\_value
-   Referenced field: configuration\_item

</td></tr><tr><td rowspan="2">

Information Object

 cmdb\_ci\_information\_object

</td><td rowspan="2">

cmdb\_ci

</td><td>

Identification rule:Independent, attributes: name

</td></tr><tr><td>

Related Entries \(cmdb\_related\_entry\):

 -   Identifier: cmdb\_ci\_information\_object
-   Related table: cmdb\_key\_value
-   Referenced field: configuration\_item

</td></tr><tr><td>

Oracle Catalog

 cmdb\_ci\_db\_ora\_catalog

</td><td>

cmdb\_ci\_db\_catalog

</td><td>

Related Entries \(cmdb\_related\_entry\):-   Identifier: cmdb\_ci\_db\_ora\_catalog
-   Related table: cmdb\_key\_value
-   Referenced field: configuration\_item

</td></tr><tr><td rowspan="3">

MySQL Catalog

 cmdb\_ci\_db\_mysql\_catalog

</td><td rowspan="3">

cmdb\_ci\_db\_catalog

</td><td>

Containment rule:cmdb\_ci\_db\_mysql\_instance-&gt;Contains:Contained By-&gt;cmdb\_ci\_db\_mysql\_catalog

</td></tr><tr><td>

Identification rule:

 Dependent, attributes: name

</td></tr><tr><td>

Related Entries \(cmdb\_related\_entry\):

 -   Identifier: cmdb\_ci\_db\_mysql\_catalog
-   Related table: cmdb\_key\_value
-   Referenced field: configuration\_item

</td></tr><tr><td>

MS SQL Database

 cmdb\_ci\_db\_mssql\_database

</td><td>

cmdb\_ci\_db\_instance

</td><td>

Related Entries \(cmdb\_related\_entry\):-   Identifier: cmdb\_ci\_db\_mssql\_database
-   Related table: cmdb\_key\_value
-   Referenced field: configuration\_item

</td></tr><tr><td rowspan="3">

Sybase Catalog

 cmdb\_ci\_db\_syb\_catalog

</td><td rowspan="3">

cmdb\_ci\_db\_catalog

</td><td>

Containment rule:cmdb\_ci\_db\_syb\_instance-&gt;Contains:Contained By-&gt;cmdb\_ci\_db\_syb\_catalog

</td></tr><tr><td>

Identification rule:

 Dependent, attributes: name

</td></tr><tr><td>

Related Entries \(cmdb\_related\_entry\):

 -   Identifier: cmdb\_ci\_db\_syb\_catalog
-   Related table: cmdb\_key\_value
-   Referenced field: configuration\_item

</td></tr><tr><td rowspan="3">

DB2 Catalog

 cmdb\_ci\_db\_db2\_catalog

</td><td rowspan="3">

cmdb\_ci\_db\_catalog

</td><td>

Containment rule:cmdb\_ci\_db\_db2\_instance-&gt;Contains:Contained By-&gt;cmdb\_ci\_db\_db2\_catalog

</td></tr><tr><td>

Identification rule:

 Dependent, attributes: name

</td></tr><tr><td>

Related Entries \(cmdb\_related\_entry\):

 -   Identifier: cmdb\_ci\_db\_db2\_catalog
-   Related table: cmdb\_key\_value
-   Referenced field: configuration\_item

</td></tr></tbody>
</table>For the list of CMDB classes in a base system, including ones that this store app is extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

