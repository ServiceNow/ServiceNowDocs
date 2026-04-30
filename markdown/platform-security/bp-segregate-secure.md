---
title: Segregating and securing data with domain separation
description: You can segregate and secure data on the ServiceNow platform in multiple ways, depending on your customer's needs. 
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Segregating and securing data with domain separation

You can segregate and secure data on the ServiceNow platform in multiple ways, depending on your customer's needs. 

## Segregating data in multiple ways

The following diagram shows four ways that you can segregate data. You can use separate instances, domain separation, contextual security and business rules, and the reference architecture itself as ways to segregate data.

![Four methods of segregating data, business rules, processes, and instances](../image/bp-multiple-ways.png)

You can segregate data in these four ways:

1.  Customizing the [reference architecture](bp-sp-reference-arch-ds.md) with qualifiers and filters so that departments and groups within a company can focus on their own work. By segregating the data between these departments or groups, a department or group can't see another department or group's records.
2.  Adding contextual security and Before Query business rules as additional layers of security to guard against data breaches. See [Context and domain separation](../concept/bp-domain-sep-context.md) and [Before Query business rules](../concept/bp-before-query-business-rules.md) to learn more about domain separation and business rules.
3.  Adding another level of security in a company by using domain separation. The data from every database query is limited to the data that is visible in a domain before contextual security and business rules are executed.
4.  Using separate instances to segregate the data at the database and application layer.

Separate instances, domain separation, contextual security and business rules, and the reference architecture are ways to segregate data. These four ways relate to each other as indicated by the Comprehensiveness of need arrow in the diagram. How each layer interacts with the other layers depends on how you set up your domain separation configuration.

Not all organizations require domain separation. You might find other alternatives, such as separate instances or a single instance without a domain. To learn more about these alternatives, see [Evaluating the need for domain separation](bp-evaluation-dom-sep.md).

-   **[Cross tenant intelligence](bp-dom-sep-how-it-works.md)**  
A multi-tenant architecture is where you have a single instance serving multiple tenants. Data, metadata, business logic, and processing context for tenants is automatically handled with access to additional tenant data.

**Parent Topic:**[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](../concept/bp-what-is-domain-separation.md)

[Domain separation hierarchies](bp-domain-sep-hierarchies.md)

[Context and domain separation](../concept/bp-domain-sep-context.md)

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

[Domain assignments](bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](../concept/bp-ds-and-csm.md)

