---
title: CI relationships and Knowledge Graph
description: CI Relationships \(Rel CI\) enable the Knowledge Graph to answer natural language questions about service dependencies and infrastructure topology by storing typed parent-child relationships between CMDB configuration items.
locale: en-US
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 3
keywords: [CI relationships, Rel CI, Knowledge Graph, CMDB, configuration items]
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# CI relationships and Knowledge Graph

CI Relationships \(Rel CI\) enable the Knowledge Graph to answer natural language questions about service dependencies and infrastructure topology by storing typed parent-child relationships between CMDB configuration items.

The **CMDB\_REL\_CI** table stores relationships between configuration items \(CIs\) in the ServiceNow CMDB. Each relationship connects a parent CI to a child CI through a defined relationship type, enabling the Knowledge Graph to understand and traverse the topology of your IT environment.

Rel CI support in the Knowledge Graph allows users to ask natural language questions about how services, servers, databases, and other CIs relate to one another without writing queries or navigating CMDB tables directly.

## How CI relationship data is stored

Each record in the Rel CI table represents a directional relationship between two CIs. Relationships are two-way and are described by a relationship type that consists of a parent descriptor and a child descriptor, separated by double colons:

`<parent descriptor>::<child descriptor>`

This means every relationship can be read in two directions:

-   Parent → child: read using the parent descriptor
-   Child → parent: read using the child descriptor

For example, a record in the Rel CI table has Bond Trading \(**cmdb\_ci\_service**\) as the parent, lnux100 \(**cmdb\_ci\_linux\_server**\) as the child, and a relationship type of `Depends on::Used by`. This relationship is read as:

-   Bond Trading depends on lnux100
-   lnux100 is used by Bond Trading

**Note:** The direction of the relationship affects how you phrase queries to the Knowledge Graph. Parent-to-child queries \(for example, "depends on"\) return more reliable results than child-to-parent queries \(for example, "used by"\).

## Knowledge Graph support for CI relationships

The Knowledge Graph can answer questions about CI relationships when the query clearly specifies all three of the following:

-   The class of the parent CI \(for example, service\)
-   The relationship direction — either the parent descriptor or child descriptor \(for example, depends on\)
-   The class of the child CI \(for example, Linux server\)

## Class hierarchy inheritance

When you define a relationship between two CI classes, the Knowledge Graph automatically extends that relationship to all classes higher up in the CI class hierarchy. This means users can query at a more general class level and still get results across all matching subclasses.

For example, a relationship defined between service and linux server also applies to server, which is a parent class of Linux server in the hierarchy. Querying for servers rather than Linux servers returns results across all server subclasses — including Linux server, windows server, UNIX server, and others.

**Note:** If a query returns fewer results than expected, try using a broader parent class in the hierarchy \(for example, "server" instead of "Linux server"\) to include all inherited CI types.

## Supported query patterns

The following table shows examples of queries the Knowledge Graph can answer using Rel CI data. Each query specifies a parent class, a relationship descriptor, and a child class.

|Scenario|Example Query|
|--------|-------------|
|Service that depends on a specific Linux server|Which services depend on 'lnux100' Linux server?|
|Servers that a specific service depends on|'Bond Trading' service depends on which UNIX server?|
|All server types a service depends on \(using hierarchy\)|'Bond Trading' service depends on which server?|
|Computers connected to a database|Which databases are connected by computers?|
|Multi-hop relationship across three CI types|What database runs on UNIX server that connects to 'nc6500-a01' network gear?|

## Unsupported query patterns

The following query types are not currently supported. Use the recommended alternatives to get the results you need.

|Limitation|Unsupported Query|Recommended Alternative|
|----------|-----------------|-----------------------|
|Negation of a relationship|Which business capabilities have no related business applications?|Rephrase to ask for what does exist rather than what does not.|
|Unspecified relationship type|Show me services related to Linux servers.|Show me services depending on Linux servers.|
|Skipping steps in a multi-hop path|Show me servers in New York.|Show me servers in racks present in datacenters located in New York.|

## Enabling Rel CI for Knowledge Graph

Rel CI support for the Knowledge Graph is inactive by default. Set both of the following system properties to true to enable it:

|System Property|Purpose|
|---------------|-------|
|**sn\_kg.description\_generation.enable\_cmdb\_rel\_ci**|Enables description generation for Rel CI data|
|**sn\_kg.query.enable\_cmdb\_rel\_ci**|Enables Knowledge Graph querying against Rel CI data|

**Note:** After enabling both properties, allow time for Rel CI data to be fully indexed before running queries. Results may be incomplete until indexing is complete.

