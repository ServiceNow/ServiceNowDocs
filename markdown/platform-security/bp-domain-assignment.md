---
title: Domain assignments
description: How you assign a domain impacts the value of the sys\_domain field. The assignments contain designs and business properties that affect how the application functions in each domain.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain assignments

How you assign a domain impacts the value of the sys\_domain field. The assignments contain designs and business properties that affect how the application functions in each domain.

## Value of the sys\_domain field

The value of the **sys\_domain** field contains the domain that is assigned to the record by any of the following:

-   Company to which the user belongs
-   Business rule that is used when creating the record
-   Module that is used when creating the record
-   Form template that is used when creating the record
-   Domain of the parent record
-   Domain that is assigned to the User record
-   Domain of the user who creates it

Make sure that your domain assignment strategies and designs are well documented and tested so that you are creating records as those strategies and designs are inserted into the correct domain. That way you can see that the properties of each domain should you need to duplicate or modify them.

**Parent Topic:**[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](../concept/bp-what-is-domain-separation.md)

[Domain separation hierarchies](bp-domain-sep-hierarchies.md)

[Context and domain separation](../concept/bp-domain-sep-context.md)

[Segregating and securing data with domain separation](bp-segregate-secure.md)

[Alternatives to domain separation](bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](bp-evaluation-dom-sep.md)

[Benefits of domain separation](bp-advantages-dom-sep.md)

[How a database query works with domain separation](../concept/bp-db-query-with-ds.md)

[Domain separation levels of support](bp-domain-levels.md)

[Service provider reference architecture](bp-sp-reference-arch-ds.md)

[Domain separation terms](bp-terms-conditions.md)

[Domain-separate a custom table](bp-ds-custom-table.md)

[Customizing domain properties and themes](../concept/bp-domain-prop-themes.md)

[Managing domain separation for specific uses](../concept/bp-emails-catalog-users.md)

[Configuring domain separation with the domain picker](../concept/bp-domain-picker-config-process.md)

[Domain separation performance considerations](../concept/bp-performance-considerations.md)

[Setting up domain hierarchies](../concept/bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](../concept/bp-domain-logs.md)

[Importance of the Default domain](../concept/bp-default-domain.md)

[Contains queries and domain access](../concept/bp-contains-domain-visibility.md)

[Domain paths query method](../concept/bp-domain-query-method.md)

[Slow queries and SQL debugging](../concept/bp-debug-sql.md)

[Before Query business rules](../concept/bp-before-query-business-rules.md)

[Avoiding domain path in scripts](../concept/bp-no-domain-path-in-scripts.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](../concept/bp-ds-and-csm.md)

