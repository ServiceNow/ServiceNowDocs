---
title: Cross tenant intelligence
description: A multi-tenant architecture is where you have a single instance serving multiple tenants. Data, metadata, business logic, and processing context for tenants is automatically handled with access to additional tenant data.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Segregating and securing data, Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Cross tenant intelligence

A multi-tenant architecture is where you have a single instance serving multiple tenants. Data, metadata, business logic, and processing context for tenants is automatically handled with access to additional tenant data.

## Single versus multiple tenants

-   **Single-tenant instance**

    You're a ServiceNow customer, you bought the licenses, and it's up to you to decide what services you want. You can upgrade when you want, see previews of all the great new features, and configure your instance right away. Being a single tenant has these benefits and restrictions:

    -   You have higher upfront costs and administrative overhead, but you have more freedom to remodel and expand.
    -   You have higher costs to obtain and maintain the instance and supply administration staff. Although you are free to build out the environment as required, you must comply with the ServiceNow recommended practices and standards.
-   **Multiple-tenant instance**

    Someone else owns the instance, possibly a service provider with multiple customers. They upgrade when they want and put new services on the instance when they want. If you are a customer of a service provider, you are most likely on their instance because you wanted what they offer. Multiple tenants have these benefits and restrictions:

    -   A centralized staff administers configurations, integrations, and upgrades.
    -   The instance owner provides added services.
    -   Domain tenants have lower upfront costs to use the ServiceNow platform, have lower monthly costs because they are sharing it with many tenants, and do not have to employ a staff to administer the environment.
    -   Benefits shared from requests or changes that are initiated by other tenants.

**Parent Topic:**[Segregating and securing data with domain separation](bp-segregate-secure.md)

