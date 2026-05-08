---
title: Domain separation and Investment Funding
description: Domain separation is supported in Investment Funding. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Investment Funding
classification: investment-funding
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investment Funding, Strategic Portfolio Management]
---

# Domain separation and Investment Funding

Domain separation is supported in Investment Funding. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Handling domain separation for Financials in Workspace

Defining funding entity is an important configuration to create Investment Object \(IO\) for any entity. The accessibility of the Funding entity definition configuration record is important to determine whether IO can be created for the entity. Let's consider example of Project as entity. Similar process is applicable for any entities configured through Funding Entity definition.

1.  Define funding entity in Global domain.

    This helps users to access projects from any specific domain or global domain.

2.  If a project is required to access from a specific domain to meet your organization requirements, define the funding entities in that specific domain only.
3.  Always create Investment Object in the same domain of the respective Project’s domain.

When a user in a parent domain accesses the financials of a project in a child domain, the system creates the investment object in the child domain. This ensures that users in the child domain can access the financials and the investment object.

**Parent Topic:**[Investment Funding](investment-funding-overview.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

