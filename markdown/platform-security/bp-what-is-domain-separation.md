---
title: Domain separation explained
description: With domain separation, you can segregate application data, UI, and business logic, such as rules or workflows, in a single customer instance. Separating these elements into logically defined domains supports specific hierarchies for all customers using your applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain separation explained

With domain separation, you can segregate application data, UI, and business logic, such as rules or workflows, in a single customer instance. Separating these elements into logically defined domains supports specific hierarchies for all customers using your applications.

## Domain basics

Domain separation, also known as ServiceNow multitenant platform architecture, adds considerable overhead to the management of an instance. If you use domain separation correctly though, it can improve efficiency, add greater security, and increase the performance of your customers' instances.

You can't separate some global standards and properties, such as system properties and table schema, per tenant.

Before you start separating domains, read the following guidelines.

## What you can do with domain separation

-   Data separation: Enables tenants of the domain to see only data that they have permissions to see. Tenants can be granted access to other tenant data but can't query tenant data that they don't have access to.
    -   When you update data records, they do not generate Update Set records.
    -   Users, including the customer accounts that are used for integrations, see only the data in the domains they have permission to access.
    -   Customers, agents, and fulfillers see data that pertains to the customers and organizations that they support.
-   UI separation: Supports a tenant-specific experience for UI elements such as views, lists, labels, and so on.
    -   You can override the browser-based user interface, including application menus, lists, forms, and dashboards. You can also customize them for a specific domain or set of domains while preserving your basic process logic.
    -   Service providers can alter the displayed branding and UI elements to meet individual customer needs.
-   Business logic separation: Creates tenant-specific system policies such as email notifications, business rules, client scripts, UI policy, and UI actions.
-   Hierarchical modeling: Nests your multiple tenants so that parent tenants can access child tenant resources. Business logic for parent tenants runs automatically for child tenants, which you can override at any level.
-   Cross-tenant intelligence: Automatically handles data, metadata, business logic, and processing context for tenants with access to additional tenant data.

## Domain separation at a glance

The following graphic shows the division of data, process, and UI separation. These concepts are discussed in depth in the Recommended Practices section.

![Types of domain separation](../image/bp-ds-separations.png)

## Domain architecture

User records are assigned a domain value that represents the user’s home domain. Users have no access to data in parent domains, peer domains, or domains in other branches of the hierarchy.

See [Contains queries and domain access](bp-contains-domain-visibility.md) for advanced options to grant additional domain visibility.

The following diagram shows how the architecture process flows down to the child domains. ![Process flows down](../image/bp-architecture-down.png) ![Data rises up](../image/bp-architecture-up.png)

-   **[Domain separation value proposition](../reference/bp-dom-sep-value-prop.md)**  
With domain separation, service providers can have a multitenant instance architecture that delivers offerings efficiently and securely to their clients. Strong universal process standards, data-driven process design, strict governance, and centralized administration help to maximize these benefits.
-   **[Definition of domain separation](../reference/bp-dom-sep-definition.md)**  
With domain separation \(also known as the ServiceNow® Multitenant Platform Architecture\), you can segregate application data, UI, and business logic in a single customer instance that supports hierarchical modeling with cross-tenant \(customer\) intelligence.

**Parent Topic:**[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

**Related topics**  


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

[Slow queries and SQL debugging](bp-debug-sql.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)

