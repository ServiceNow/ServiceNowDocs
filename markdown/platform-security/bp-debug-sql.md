---
title: Slow queries and SQL debugging
description: Debugging SQL and slow queries can help you resolve slowness issues in an instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Slow queries and SQL debugging

Debugging SQL and slow queries can help you resolve slowness issues in an instance.

When you debug an instance, you can either enable SQL debugging to look for slow queries or you can look for slow queries by checking the Slow Queries \[sys\_query\_pattern\] table by navigating to **System Diagnostics &gt; Stats &gt; Slow Queries**. This table stores all the slow queries in the instance.

When you search the table, look for queries that contain `domain_path` to determine if any slow queries are due to the domain path in your instance.

If you do find slow queries, try to analyze why they are slow.

## Common reasons for slow queries

-   A query has too many OR conditions \(for more information, see [Contains queries and domain access](bp-contains-domain-visibility.md)\). In the domain hierarchy, place the user or a domain at a hierarchy level where contains or visibility is not needed.
-   The query method is not the domain path query method \(for more information, see [Domain paths query method](bp-domain-query-method.md)\): If you are not using the domain path query method, contact Customer Service and Support.
-   A query needs a database to be indexed so you can see what is in the database quickly. If you can identify the slow query, run the "explain plan" to see if there are options for indexing available. The "explain plan" is a function of SQL that shows the query and what is going on with it.

**Parent Topic:**[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](bp-what-is-domain-separation.md)

[Domain separation hierarchies](../reference/bp-domain-sep-hierarchies.md)

[Context and domain separation](bp-domain-sep-context.md)

[Segregating and securing data with domain separation](../reference/bp-segregate-secure.md)

[Alternatives to domain separation](../reference/bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](../reference/bp-evaluation-dom-sep.md)

[Benefits of domain separation](../reference/bp-advantages-dom-sep.md)

[How a database query works with domain separation](bp-db-query-with-ds.md)

[Domain separation levels of support](../reference/bp-domain-levels.md)

[Service provider reference architecture](../reference/bp-sp-reference-arch-ds.md)

[Domain separation terms](../reference/bp-terms-conditions.md)

[Domain-separate a custom table](../reference/bp-ds-custom-table.md)

[Customizing domain properties and themes](bp-domain-prop-themes.md)

[Managing domain separation for specific uses](bp-emails-catalog-users.md)

[Configuring domain separation with the domain picker](bp-domain-picker-config-process.md)

[Domain separation performance considerations](bp-performance-considerations.md)

[Setting up domain hierarchies](bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](bp-domain-logs.md)

[Importance of the Default domain](bp-default-domain.md)

[Contains queries and domain access](bp-contains-domain-visibility.md)

[Domain paths query method](bp-domain-query-method.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)

