---
title: How a database query works with domain separation
description: Using database queries with domain separation in your customers' applications help them protect their data. These queries then speed up the configuration and build processes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# How a database query works with domain separation

Using database queries with domain separation in your customers' applications help them protect their data. These queries then speed up the configuration and build processes.

## How domain separation protects data

In the following figure, the Incident table \[incident\] has a domain field that is inherited from the incident's task. When you see this domain field, you know that the records in the table can have domain assignments.

When users log in, their home domain appears with the set of domains they may access. This is known as the user’s session context. For more information about session contexts, see [Context and domain separation](bp-domain-sep-context.md).

## Database query with domain separation

![Database query with domain separation](../image/bp-db-query-with-ds.png)

1.  In a browser, the user from one of the companies, Acme, selects the Open Incidents module to view all incidents where active=true.
2.  The active=true filter is submitted to the application.
3.  The application then sends a query to the database by appending a WHERE clause to active=true. The WHERE clause limits the incident records that are returned to those records that are in the user's domain or the domains that the user may access. Only the records in these domains are returned to the application for processing.
4.  Contextual security is applied, further limiting the data that is returned to the user. The incident records appear in the Open Incidents list.

    **Note:**

    When you apply contextual security, you create limits to the data that are returned to the user. These limits protect other content that you may not want users to see.


To learn more about contextual security, see [Context and domain separation](bp-domain-sep-context.md).

**Note:** This processing logic applies for all queries to the database, including those queries that are triggered using integrations.

**Parent Topic:**[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](bp-what-is-domain-separation.md)

[Domain separation hierarchies](../reference/bp-domain-sep-hierarchies.md)

[Context and domain separation](bp-domain-sep-context.md)

[Segregating and securing data with domain separation](../reference/bp-segregate-secure.md)

[Alternatives to domain separation](../reference/bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](../reference/bp-evaluation-dom-sep.md)

[Benefits of domain separation](../reference/bp-advantages-dom-sep.md)

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

[Slow queries and SQL debugging](bp-debug-sql.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)

