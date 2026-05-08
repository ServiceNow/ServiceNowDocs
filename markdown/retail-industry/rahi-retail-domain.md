---
title: Domain Separation in Retail Core
description: Domain separation is supported for Retail Core. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Retail]
---

# Domain Separation in Retail Core

Domain separation is supported for Retail Core. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic

-   Business logic: Verify that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response. For more information on support levels, see Application support for domain separation.

## Retail use case

-   For the retail case, the domain column is inherited from the customer service case.
-   For retail organization, the 'domain\_master' attribute receives information from the Organization Core.

**Parent Topic:**[Retail reference](../concept/rahi-retail-operations-reference.md)

