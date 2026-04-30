---
title: Security data filters
description: Security data filters restrict access to records based on role, or security-attribute related assertions.
locale: en-US
release: yokohama
product: Data Filtration
classification: data-filtration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Access Management]
---

# Security data filters

Security data filters restrict access to records based on role, or security-attribute related assertions.

## Exploring security data filters

Security data filters enable access restriction to records based on a users' role, or other security attribute related assertions. Security data filters ensure only authorized users can view records regardless of how data is accessed. Security data filters are applied before a query is executed.

## Features of security data filters

The key features of security data filters are:

-   Security data filters are applied in-query.
-   Security data filter conditions `AND` to the query on the target table and with each other.
-   Security data filters are not checked by `canRead`. See [Security data filter uses](security-data-filters.md#section_dqx_2c1_b2c) for more details
-   Data filter scoping rules are based on the scope of the table, data filters do not follow ScopeMaster or sys\_scope scope rules

## Security data filter application and enforcement

Generally security data filters are applied after absolute ACLs \(also called table-level ACLs\), and before row ACLs. Security data filters are applied by default, and impact system behavior if not used carefully. See [Locations of default security filters](../reference/default-security-filters.md) for a list of the default security data filters.

Security data filters are applied only to GlideRecordSecure, GlideRecordSandbox and GlideAggregateSandbox queries by default. There are two new GlideRecord APIs `enableSecurityFeature` and `disableSecurityFeature` that can be used in both Java and server-side scripts to enable or disable data filters for a specific query.

**Important:** You should explicitly enable data filters for user-facing queries that are not using GlideRecordSecure.

## Security data filter uses

Security data filters are best suited to:

-   Prevent sensitive data from leaving the database
-   Suppress the "rows hidden by security" message
-   Prevent sensitive data from leaking through reports

Exercise caution when using security data filters:

-   As visibility controls
-   With a large number of filter conditions
-   On unindexed columns

## Security data filter behavior

Multiple security data filters combine together for evaluation, like an `AND` combines operands. As an example,given three security data filters:

-   Filter 1: \`active=true
-   Filter 2: `priority=1`
-   Filter 3: `state=open`

And an initial query:

```
SELECT * FROM task WHERE state != closed AND active = true AND
        priority = 1
```

The final query is:

```
SELECT * FROM task WHERE state != closed
          AND active = true AND priority = 1 AND state = open
```

One important difference in how security data filters and ACLs are applied is, data filters on a child table do not apply to the parent table when data is queried from the parent table. Add a data filter on both child and parent tables to restrict access to records in the parent table.

**Note:** A common solution for this is to add a data filter on the parent that completely hides child records in the parent table.

## Security data filters performance considerations

Security data filters may impact system performance, slowing query and page load times, if not used carefully. There are three primary factors in query execution:

-   Number of filters applied
-   Complexity of user query
-   Complexity of conditionally applied filters

These factors determine the compute cost of a query. A high compute cost will affect instance responsiveness.

Some examples of use that increase compute cost are:

-   Querying unindexed columns
-   Using the `contains` operator
-   Full table scans

When creating a security data filter, use the [Security data filter performance analysis tool](security-data-filter-performance-analysis-tool.md) to gauge performance impact and ensure you are responsibly applying security data filters.

