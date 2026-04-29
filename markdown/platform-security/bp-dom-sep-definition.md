---
title: Definition of domain separation
description: With domain separation \(also known as the ServiceNow Multitenant Platform Architecture\), you can segregate application data, UI, and business logic in a single customer instance that supports hierarchical modeling with cross-tenant \(customer\) intelligence.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Domain separation explained, Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Definition of domain separation

With domain separation \(also known as the ServiceNow® Multitenant Platform Architecture\), you can segregate application data, UI, and business logic in a single customer instance that supports hierarchical modeling with cross-tenant \(customer\) intelligence.

## Properties of domain separation

Domain-separated ServiceNow applications are defined with the following properties:

-   **Data separation**

    Enables customers to see only the data that they have permissions to see. Customers can be granted access to other customer data but cannot query customer data if they don't have access.

-   **UI separation**

    Supports a customer-specific experience for UI elements such as views, lists, labels, and so on.

-   **Business logic separation**

    Supports customer-specific system policies such as email notifications, business rules, client scripts, UI policy, and UI actions.

-   **Hierarchical modeling**

    Supports nested-multitenancy so parent tenants \(customers\) can access child customer resources. The business logic for parent customers runs automatically for child customers and can be overridden at any level.

-   **Cross-customer intelligence \(domain scope\)**

    Handles automatically the data, metadata, business logic, and processing context for tenants that have access to additional tenant data.


**Parent Topic:**[Domain separation explained](../concept/bp-what-is-domain-separation.md)

