---
title: Exploring CMDB Query Builder
description: The CMDB Query Builder enables you to build complex infrastructure and service queries that span multiple CMDB classes, non-CMDB tables, and that involve many CIs that are connected by different relationships.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring CMDB Query Builder

The CMDB Query Builder enables you to build complex infrastructure and service queries that span multiple CMDB classes, non-CMDB tables, and that involve many CIs that are connected by different relationships.

The CMDB Query Builder provides a canvas into which you drag the CI classes that you want to include in a query. Then you add relationships, AND/OR operators between the CI classes, and define the relationship properties to query for. You can use saved queries to populate a CMDB group with CIs, and then use scriptable APIs to retrieve the CI list and apply actions collectively to all the CIs in the group.

There are two query types: CMDB Query and a Service Mapping query, which you can use separately or in combination to create queries such as:

-   All hardware in my service offering that has Windows installed.
-   All CIs of a certain type in an application service. For example, all Apaches/Web Servers/Linux servers per service.
-   All virtual servers and the physical servers that host them.
-   All servers that are not mapped to any application service.
-   All application services and their associated servers and the cost of each server. This query helps evaluate the cost of technology for each application service.

Starting node: The starting point of the query which is labeled as **STARTING NODE** on the Query Builder canvas. The first class that you drag to the canvas becomes automatically the starting node of the query and you cannot select a different starting node. In a complex query, the starting node must always be the only node connected to an AND/OR operator. If you try to connect a second node to an operator that the starting node is connected to, the query fails to run and a prompt to select a different starting node appears.

## Additional information

For a webinar, see [CMDB Query Builder Queries and Reporting - Platform Analytics Academy](https://www.servicenow.com/community/performance-analytics-blog/platform-analytics-academy-october-19th-2022-cmdb-query-builder/ba-p/2351259) blog post in the ServiceNow Community.

## Intelligent Search for CMDB integration

By default, [Intelligent Search for CMDB](intelligent-search-cmdb.md) functionality is integrated into the CMDB Query Builder. When opening the Query Builder, you can use the Intelligent Search search box which appears above the Query Builder canvas. Intelligent Search lets you use everyday natural language query \(NLQ\) to build a query. Intelligent Search parses, resolves any ambiguities in table names and relationship types, and then converts your search string into a valid query. The query appears fully constructed on the Query Builder canvas where you can run or continue and develop the query.

The integration of Intelligent Search for CMDB with the CMDB Query Builder is controlled by the system property **glide.cmdb.query.nlq.activated**, which is set to **true** by default. If you set the property to **false**, Intelligent Search for CMDB will not be available within the Query Builder.

## AI Search and CMDB

NLQ Genius Results for [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) use natural language queries to find CMDB tables that match your search without leaving a portal or workspace. For more information, see [NLQ Genius Results](https://www.servicenow.com/docs/access?context=genius-result-nlq-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** AI Search is a complementary search experience that allows you to surface CMDB records in your normal flow of work, without having to access the CMDB Query Builder. It doesn't replace intelligent Search for CMDB, which is purpose-built and integrated into CMDB Query Builder.

## Query types

There are several types of CMDB queries:

-   **CMDB Query**

    A query type that queries the infrastructure for CI classes and the relationships and references that connect them. You can optionally add the context of non-CMDB tables to a CMDB query.

    You can include [Application services](application-services.md) in a CMDB query, to find, for example:

    -   All critical application services in your database.
    -   All infrastructure in a particular application service.
    -   All incidents for a particular CI in an application service, or all incidents for all the CIs of an application service.
    -   All application services with a pattern of a service connected to a database, and where the database has incidents.
    The list of available non-CMDB tables includes a subset of tables within the system, which have a reference to the Configuration Item \[cmdb\_ci\] class or its children. The list of non-CMDB tables, includes tables such as Asset, Task, and Problem. You can use the system property [glide.cmdb.query.non\_cmdb.black\_listed\_tables](../reference/cmdb-querybldr-sysproprties.md) to narrow down the list of non-CMDB tables to choose from.

-   **Service Mapping Query**

    A query type that queries application services. The query is framed within an application service map. You define a pattern, and query for application service maps that have that pattern in their definition. The relationships in Service Mapping queries are matched by single-level direct relationships which is similar to the CMDB queries, and in addition, they are also matched by multi-level indirect relationships if they exist. A query for a relationship between two CI classes is satisfied even if the two CI classes are connected by intermediate CI classes that are not specified in the query.

-   **Combination Query**

    You can combine the two query types by incorporating a saved Service Mapping query into a CMDB query. For example, create a CMDB query for Windows Servers that are connected to Tomcat WAR. Then connect the Tomcat WAR CI class to a Service Mapping query. The query changes to find Windows Servers that are connected to Tomcat WAR which is included in the services that returned by the Service Mapping query. You can inverse that query by choosing **Does Not Belong To Service**. This changes the query to find Windows Servers that are connected to Tomcat WAR that is not included in services returned by the Service Mapping query.


**Related topics**  


[CMDB groups](cmdb-groups.md#)

