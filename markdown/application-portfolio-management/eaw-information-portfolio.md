---
title: Exploring the information portfolio
description: Use the information portfolio to capture information from the assets of your organization as information objects. You can categorize the information assets and determine its business application use. You can also connect the different layers where data exists and map the layers. Mapping helps to retrieve the information and track the information flow.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploring Portfolio list view, Explore, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exploring the information portfolio

Use the information portfolio to capture information from the assets of your organization as information objects. You can categorize the information assets and determine its business application use. You can also connect the different layers where data exists and map the layers. Mapping helps to retrieve the information and track the information flow.

## Information portfolio data model

The basic data model of information portfolio is in the introduction of two tables, which are Information Object and Data Domain.

-   Information object is a configuration item that displays information in an organized form. The purpose of the information object is to logically describe the type of data \(or the information\) that is interchanged between the application and the database. The database being the one that serves the application with data.
-   Data domain is to classify or categorize the information objects.

Enterprise Architecture integrates with information portfolio by relating a business application with the database. The database provides the information to the application using an intermediary CMDB CI class called information object \[cmdb\_ci\_information\_object\] table.

The business application is related with the information object by establishing Uses::Used by CMDB CI relationship. The information object, in turn, is linked to the database catalog and instances by establishing Depends on::Used by CMDB CI relationship.

Enterprise Architecture integrates with ServiceNow Discovery that finds database applications, database instances, and database catalog. The database catalog lists all the catalog objects, or databases, discovered for an instance of a database.

## Plugin activation procedure

CMDB plugin has the Information Object \(cmdb\_ci\_information\_object\) CI. When the Enterprise Architecture plugin is activated, the data domain field gets added to the cmdb\_ci\_information\_object table. The data domain field references the Data Domain table, which is included in the Enterprise Architecture plugin.

-   **[Exploring data domains](eaw-data-domains.md)**  
A data domain is a collection of information objects. A data domain categorizes information objects.
-   **[Exploring information objects](eaw-information-objects.md)**  
An information object captures the logical data for a business application. It also describes the type of data that is interchanged between the application and the database.
-   **[Exploring architectural artifacts](eaw-managing-architectural-artifacts.md)**  
Architectural artifacts are created to describe a system, solution, or state of an enterprise. The goal of architectural artifacts in Enterprise Architecture is to enable enterprise architects to create and manage artifacts in their organization.
-   **[Exploring architectural decision records \(ADR\)](eaw-managing-arch-decision-records.md)**  
Use the Architectural Decision Records \(ADR\) to explain your infrastructure. ADR is a type of artifact that helps you to understand the background of a specific architectural decision.

**Parent Topic:**[Exploring Portfolio list view](../portfolio-list-view.md)

**Related topics**  


[Working with information portfolio](eaw-work-with-info-portfoliodita.md)

