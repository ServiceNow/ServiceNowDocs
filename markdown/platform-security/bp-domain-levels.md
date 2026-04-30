---
title: Domain separation levels of support
description: Choose from three categories for domain separation of an application for your customers' organizations.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain separation levels of support

Choose from three categories for domain separation of an application for your customers' organizations.

Applications that support domain separation may support the separation of data and data routing only, have advanced business logic separation, or support tenant \(customer\) level administration of the application. These definitions delineate the support levels from the perspective of actual use cases and the people who implement them.

## Incremental ServiceNow support levels

![Domain separation support levels](../image/ds-support-levels.png)

<table id="table_ucy_nd2_rhb"><thead><tr><th>

Level

</th><th>

Type

</th><th>

Summary

</th></tr></thead><tbody><tr><td>

No support

</td><td>

 

</td><td>

-   The domain field may exist on data tables, but no business logic exists to manage the data.
-   This level isn’t considered domain-separated.

</td></tr><tr><td>

Basic

</td><td>

Customer data management

</td><td>

-   Business logic: Ensures that data goes into the proper domain for the application’s service provider use cases.
-   In the application, user interface, cache keys, reporting, rollups, aggregations, and so on, all consider the properties of the domain at run time.
-   Your instance owners must be able to set up the application to function normally across multiple tenants.

 Use case: When a service provider uses chat to respond to a customer’s message, the client must be able to see the response.

</td></tr><tr><td>

Standard

</td><td>

Customer process management

</td><td>

-   Includes the Basic level
-   Business logic: Processes can be created or modified per customer by the service provider. The use cases reflect how the application is used by multiple service provider customers in a single instance.
-   Your instance owners must be able to configure minimum viable product \(MVP\) business logic and data parameters per customer for the specific application.

 Use case: Admin must be able to make comments required when a record closes for one customer, but not for another customer.

</td></tr><tr><td>

Enhanced

</td><td>

Customer self-managed configuration

</td><td>

-   Includes Basic and Standard levels
-   Enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer can’t affect another customer.
-   The instance customers must be able to configure MVP business logic and data parameters themselves.

 Use case: Customer of a shared environment must be able to make changes according to impact, urgency, or priority within a domain.

</td></tr><tr><td>

Effective domain\*

</td><td>

 

</td><td>

In some cases, a platform feature or application may support service provider use cases even if the domain framework isn’t being used. The use cases must be detailed to support domain separation. An asterisk \(\*\) after the support level indicates this kind of configuration.

 Use case: Before the New York release, Service Catalog had no domain support but the instance owners could configure separate catalogs and items for each tenant in a domain-separated instance by using user criteria. The result was that each tenant could use Service Catalog at a Standard level.

</td></tr></tbody>
</table>To view all applications listed by their support level see [Application support for domain separation](domain-separated-apps.md).

## Summary

Domain separation is a framework that you must use to make your applications aware of its customers.

Consider the domain framework capabilities, your applications' business use cases, what the personas are, and how they use the application before you can use the framework to make your application supportable.

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

