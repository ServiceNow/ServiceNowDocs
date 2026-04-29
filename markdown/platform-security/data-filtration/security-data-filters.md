---
title: Security data filters
description: Security data filters restrict access to records based on role, or security-attribute related assertions.
locale: en-US
release: australia
product: Data Filtration
classification: data-filtration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Access Management]
---

# Security data filters

Security data filters restrict access to records based on role, or security-attribute related assertions.

## Exploring security data filters

Security data filters enable access restriction to records based on a users' role, or other security attribute related assertions. Security data filters ensure only authorized users can view records regardless of how data is accessed.

Security data filters are applied before a query is executed so restricted data never leaves the database. In contrast [conditional ACLs](../../contextual-security/concept/access-control-rules.md) filter data after a query is executed possibly leaking data.

**Note:** Pair security data filters with [Deny-Unless ACL](../../contextual-security/concept/acl-denial-behavior.md) to ensure consistent security

## Features of security data filters

The key features of security data filters are:

-   Security data filters are applied in-query.
-   Security data filter conditions `AND` to the query on the target table and with each other.
-   Security data filters are not checked by `canRead`. See [When to use security data filters](security-data-filters.md#section_dqx_2c1_b2c) for more details
-   Data filter scoping rules are based on the scope of the table, data filters do not follow ScopeMaster or sys\_scope scope rules

## Security data filter application and enforcement

Generally security data filters are applied after absolute ACLs \(also called table-level ACLs\), and after row ACLs. Security data filters are applied by default, and impact system behavior if not used carefully. See [Default security filters](../reference/default-security-filters.md) for a list of the default security data filters.

Security data filters are applied only to GlideRecordSecure, GlideRecordSandbox and GlideAggregateSandbox queries by default. There are two new GlideRecord APIs `enableSecurityFeature` and `disableSecurityFeature` that can be used in both Java and server-side scripts to enable or disable data filters for a specific query.

**Important:** You should explicitly enable data filters for user-facing queries that are not using GlideRecordSecure.

## When to use security data filters

Security data filters are best suited to:

-   Prevent sensitive data from leaving the database
-   Suppress the "rows hidden by security" message
-   Prevent sensitive data from leaking through reports

## When not to use security data filters

Security data filters should not be used:

-   As visibility control
-   As replacement for ACLs
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

See the diagram below for a visual representation of this example:

![A Venn Diagram showing how multiple data filters combine in conjunction.](../image/secdf-logic.png)

One important difference in how security data filters and ACLs are applied is, data filters on a child table do not apply to the parent table when data is queried from the parent table. Add a data filter on both child and parent tables to restrict access to records in the parent table. The diagram below highlights the hierarchy:![The diagrams displays how data filters on child tables do not apply to their parent tables](../image/secdf-hierarchy.png)

**Note:** A common solution for this is to add a data filter on the parent that completely hides child records in the parent table.

Data filters are applied with scoping rules similar to ACLs, but with some key differences because data filters apply before-query.![Data filters applied to scopes](../image/secdf-scope.png)

