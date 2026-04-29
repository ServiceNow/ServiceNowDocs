---
title: CMDB Query Builder engine execution modes
description: The CMDB Query Builder engine uses two execution modes to run queries. By default, the system is configured to use the enhanced mode V2 which is designed for performance optimization. V2 is supported for most queries and enables running complex queries significantly quicker and process larger result sets without performance degradation.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Query Builder engine execution modes

The CMDB Query Builder engine uses two execution modes to run queries. By default, the system is configured to use the enhanced mode V2 which is designed for performance optimization. V2 is supported for most queries and enables running complex queries significantly quicker and process larger result sets without performance degradation.

The CMDB Query Builder can be set with the following engine execution modes for running queries:

-   **V2**

    An enhanced query execution engine designed for improved performance and scalability. This is the default execution engine. In V2 mode, compared to V1 mode, the CMDB Query Builder engine is capable of running complex queries significantly quicker and process larger result sets without performance degradation.

    However, some query structures aren't supported for the V2 mode, in which case such queries will automatically run using the legacy mode \(V1\).

-   **V1**

    Legacy execution engine which is used when the system is explicitly configured to use V1. This mode is also used even if the system is configured to run in V2 mode, to run queries with a structure that isn't supported for the V2 mode.


## Considerations for the 'OR' operator

Setting the execution mode for queries that contain 'OR' operators, such as the sample query below, require some special considerations:

![Query with 'OR' structure](../image/QueryOR.png)

Running a query with 'OR' structures can be significantly faster in V2 mode than in V1, but the results are presented differently between V1 and V2 execution modes. The difference is because 'OR' operator nodes generate coalesced and cross-product result sets. In V2 mode, related results are merged into a single result item. In V1, the same results are represented by separate result items.

!['OR' results in V1 execution mode](../image/QueryV1ORResults.png "Results for a query with an 'OR' structure, in V1 execution mode")

!['OR' results in V2 execution mode](../image/QueryV2ORResults.png "Results for a query with an 'OR' structure, in V2 execution mode")

In some situations, it might be important to run a query with an 'OR' structure, using the V1 engine mode to retain the legacy format of the results in support of existing organizational reports. You can use the **glide.cmdb.query.or\_execution\_mode** system property as described below to control execution mode for queries with 'OR' structures.

## Settings

The system uses the following settings of execution mode to determine which execution mode to use to run a query:

-   Query-level setting:

    The **Query Execution Mode** attribute in the Saved Queries \[qb\_saved\_query\] table sets the engine mode for the respective query. For more information about this setting, see [Set execution mode for running a query](../task/config-query-builder-engine-mode.md).

    The query-level setting has precedence over system property settings.

-   Global setting:

    System property **glide.cmdb.query.execution\_mode** sets the system-wide default mode to use when a query's mode isn't set at the query level.

-   Global setting:

    System property **glide.cmdb.query.or\_execution\_mode** sets the system-wide default execution engine mode for queries that contain at least one logical OR condition. Because the results of a query with an 'OR' structure are formatted differently between V1 and V2 mode, this property setting also affects which format is used for the results.

    This property has precedence over the **glide.cmdb.query.execution\_mode** system property.


For more information about the engine mode system properties, see [Property settings for CMDB Query Builder](../reference/cmdb-querybldr-sysproprties.md).

## Unsupported query structures for V2 mode

The following query structures aren't supported in V2 and therefore are executed using V1 mode even if the system is configured to use V2 mode:

-   Queries with filters containing related list conditions.
-   No relationships combined with a filter containing configuration item conditions: Node that has no relationships configured and the target node's filter has configuration item conditions.

    For example: `Server NOT connected to Router WHERE Router.status = Active`.

-   Service Mapping query with related edges \(Applicative flow, Not Applicative flow, Belongs To, Not belongs to\). Service Mapping query with service query properties set to **Find Related CIs** or **Find Unrelated CIs**, or a combination query in which a service query connection property is set to **Does Not Belong to Service**.

## Decision flow

The system uses a decision flow that checks all relevant settings and the query structure to determine which execution mode to use for running a query. First, the system checks the query-level and the system-level settings. Then, if the settings are configured for using V2 to run a query, the system checks the query structure to determine if the V2 execution mode supports the query's structure. If the query contains a structure that isn't supported in V2, execution automatically falls back to using V1 mode even though the settings are configured to using V2. This automatic fallback mechanism supports a successful execution of all queries while maximizing performance benefits where possible.

Using default settings, if a query structure is supported by the V2 execution mode, the query executes using V2 mode.

The following decision flow examines settings and query structures, to determine whether a query runs in V1 or V2 engine execution mode:

1.  Check the setting in the **Query Execution Mode** attribute in the query record in the Saved Queries \[qb\_saved\_query\] table:
    -   If '**V1**': Use V1
    -   If '**V2**': Skip to step \#4 — Perform V2 support check
    -   If '**None**': Check system properties as described in the next step
2.  Check system property **glide.cmdb.query.execution\_mode**:
    -   If not set: Use V2 pending support check
    -   If '**V1**': Use V1
    -   If '**V2**':
        -   If no logical OR conditions: Skip to step \#4 — Perform V2 support check
        -   If one or more logical OR conditions: Perform 'OR'-specific check as described in the next step
3.  Check the value of **glide.cmdb.query.or\_execution\_mode**:
    -   If '**V1**': Use V1
    -   If '**V2**': Skip to step \#4 — Perform V2 support check
    -   If empty: Use V2
4.  Perform V2 support check:
    -   If the query contains a structure that isn't supported in V2: Use V1
    -   If query structure is supported in V2: Use V2

The **Query Execution Mode** attribute in table Query Status \[qb\_query\_status\] shows the execution mode assigned to each query.

