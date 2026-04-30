---
title: Managing domain separation for specific uses
description: You can set up separate domains for email notifications and customize the properties of catalog, tables, users, groups, and views. This enables you to provide more specific behavior in each domain, giving your customers more flexibility.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Managing domain separation for specific uses

You can set up separate domains for email notifications and customize the properties of catalog, tables, users, groups, and views. This enables you to provide more specific behavior in each domain, giving your customers more flexibility.

## Emails

You can use separate domains for email notifications and overrides. When you use separate domains for notifications, you can do an override that is based on the domain of just the attached record, not the user’s whole domain.

## Service Catalog

The Service Catalog is now domain-separated so that your customers can see and access the catalog. Items are processed as OR conditions when multiple items are used. Service providers should administer the categories and Items themselves so they fit their own criteria specifically.

## Users and groups

Only use admin accounts in the global domain because admins need access to all domains. Do all your application testing from an actual domain, not in the global domain. Overrides don't process properly in the global domain. Admins should also be given user accounts in production if they are to use the application.

## Working with fields

There are several points to consider when you work with fields. Pay close attention to these fields because they can have many variations that affect your configurations.

-   **Lists**

    There are personal, global, and domain lists, as well as multiple views of each.

-   **Forms**

    There are global and domain lists as well as multiple views of each.

-   **One database**

    Any fields that you create exist for all users, in one database. Consider the global impact before you create one.


**Note:** ACL scripts cannot keep a field from being viewed in a list because they do not run. You can add a READ ACL to hide a field from users if the ACL is only role-based.

## Creating tables

When you create a table, you should add a `sys_domain` or an `sys_overrides` field. Any table that contains data that your instance users need to access, needs the `sys_domain` field. Tables that extend or support processes and that need to flow down to children domains also need the `sys_domain` field.

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

