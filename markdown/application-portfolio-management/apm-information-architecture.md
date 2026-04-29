---
title: Information portfolio
description: Use the information portfolio to capture information from the assets of your organization as information objects. You can categorize the information assets and determine its business application use. You can also connect the different layers where data exists and map the layers. Mapping helps to retrieve the information and track the information flow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Information portfolio

Use the information portfolio to capture information from the assets of your organization as information objects. You can categorize the information assets and determine its business application use. You can also connect the different layers where data exists and map the layers. Mapping helps to retrieve the information and track the information flow.

**Important:**

Starting with the Xanadu release, the legacy information portfolio module has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the legacy information portfolio module. If you’re a new activation user, the legacy information portfolio module isn’t available.

You can leverage the same feature by using the Enterprise Architecture Workspace. To learn more, see [Exploring the information portfolio](eaw-concept/eaw-information-portfolio.md).

## Information portfolio data model

The basic data model of information portfolio is in the introduction of two tables, which are Information Object and Data Domain.

-   Information object is a configuration item that displays information in an organized form. The purpose of the information object is to logically describe the type of data \(or the information\) that is interchanged between the application and the database. The database being the one that serves the application with data.
-   Data domain is to classify or categorize the information objects.

Enterprise Architecture integrates with information portfolio by relating a business application with the database. The database provides the information to the application using an intermediary cmdb CI class called information object \[cmdb\_ci\_information\_object\] table.

The business application is related with the information object by establishing Uses::Used by cmdb CI relationship. The information object, in turn, is linked to the database catalog and instances by establishing Depends on::Used by cmdb CI relationship.

Enterprise Architecture integrates with ServiceNow Discovery that finds database applications, database instances, and database catalog. The database catalog lists all the catalog objects, or databases, discovered for an instance of a database.

## Plugin activation procedure

CMDB plugin has the Information Object \(cmdb\_ci\_information\_object\) CI. When Enterprise Architecture plugin is activated, the data domain field gets added to the cmdb\_ci\_information\_object table. The data domain field references the Data Domain table, which is included in the Enterprise Architecture plugin.

**Related topics**  


[Create a data domain](../task/create-data-domain-info-architecture.md)

[Create an information object referencing a data domain](../task/create-information-object.md)

[Relate a business application to an information object](../task/relate-business-app-information-object.md)

[Relate the information object to the database catalog](../task/relate-info-object-database-catalog.md)

[Relate a business application to another business application](../task/relate-business-app-to-business-app.md)

