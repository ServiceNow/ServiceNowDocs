---
title: Domain paths query method
description: You can create effective queries with domain paths.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain paths query method

You can create effective queries with domain paths.

Use domain paths instead of domain spooling \(`sys_domain`\) or domain numbering. Queries that use domain paths are much faster than spooling or numbering.

Domain paths is the default query method for instances that have enabled domain separation.

If you want to verify the query method on your instance, look for the following system properties in the admin dashboard:

-   **If domain path is enabled**: In the System Properties table, you see `glide.sys.domain.provider=domain_paths` and `glide.sys.domain.paths.installed=true`.
-   **If domain path is not enabled**: In the System Properties table, you see `glide.sys.domain.provider != domain_paths,glide.sys.domain.paths.installed=false`

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

[Slow queries and SQL debugging](bp-debug-sql.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)

