---
title: Importance of the Default domain
description: Organizing your domains is a crucial part of the domain separation process. If you don't set a default domain, new tasks and user records go to the global domain. Anyone can see the records in the global domain, which means that data can be seen when it is not supposed to.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Importance of the Default domain

Organizing your domains is a crucial part of the domain separation process. If you don't set a default domain, new tasks and user records go to the global domain. Anyone can see the records in the global domain, which means that data can be seen when it is not supposed to.

When you set the default domain, its records are not visible to any user other than an admin.

**Note:** The defaults access can be changed by granting users visibility to the default domain or the parent domain.

You should always set one default domain for the domain records on your instance. The default domain is where the system automatically assigns task and user records that are not already assigned to a domain.

When you create a default domain from the Domain Administration screen, add the name Default in the **Name** field to differentiate it from other domains. Check the **Default** check box for the record.

Maintain regularly the records that you create in the default domain and move them to the correct domains. If records show up often in the default domain, you may need to investigate why. Ideally, you should make sure that all records are created in their appropriate domains \(not global or default domains\).

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

[Contains queries and domain access](bp-contains-domain-visibility.md)

[Domain paths query method](bp-domain-query-method.md)

[Slow queries and SQL debugging](bp-debug-sql.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)

