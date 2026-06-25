---
title: Domain separation explained
description: With domain separation, you can segregate application data, UI, and business logic, such as rules or workflows, in a single customer instance. Separating these elements into logically defined domains supports specific hierarchies for all customers using your applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-what-is-domain-separation.html
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

\[Omitted image "bp-ds-separations.png"\] Alt text: Types of domain separation

## Domain architecture

User records are assigned a domain value that represents the user’s home domain. Users have no access to data in parent domains, peer domains, or domains in other branches of the hierarchy.

See [Contains queries and domain access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-contains-domain-visibility.md) for advanced options to grant additional domain visibility.

The following diagram shows how the architecture process flows down to the child domains. \[Omitted image "bp-architecture-down.png"\] Alt text: Process flows down \[Omitted image "bp-architecture-up.png"\] Alt text: Data rises up

-   **[Domain separation value proposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-dom-sep-value-prop.md)**  
With domain separation, service providers can have a multitenant instance architecture that delivers offerings efficiently and securely to their clients. Strong universal process standards, data-driven process design, strict governance, and centralized administration help to maximize these benefits.
-   **[Definition of domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-dom-sep-definition.md)**  
With domain separation \(also known as the ServiceNow® Multitenant Platform Architecture\), you can segregate application data, UI, and business logic in a single customer instance that supports hierarchical modeling with cross-tenant \(customer\) intelligence.

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation hierarchies]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

[Evaluating the need for domain separation]()

[Benefits of domain separation]()

[How a database query works with domain separation]()

[Domain separation levels of support]()

[Service provider reference architecture]()

[Domain separation terms]()

[Domain-separate a custom table]()

[Customizing domain properties and themes]()

[Managing domain separation for specific uses]()

[Configuring domain separation with the domain picker]()

[Domain separation performance considerations]()

[Setting up domain hierarchies]()

[Checking domain logs for errors and warnings]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()

