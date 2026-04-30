---
title: Domain separation and Service Exchange
description: Domain separation is supported for Service Exchange. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Exchange reference, Service Exchange]
---

# Domain separation and Service Exchange

Domain separation is supported for Service Exchange. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

The Provider Task and Remote Task tables have domain separation available. When data is added to these tables, Service Exchange inserts them into the domain of the parent task if available, or the connected instance based on the associated company by default. If necessary, the instance admin can apply their own business rule to redirect the data after the Service Exchange default rule has been applied. However, this should only be done by setting a different company on the records before inserting them.

## How domain separation works in Service Exchange

-   The Provider Task and Remote Task tables in the application are domain-separated.
-   Make sure that the consumer company and account tables are associated to the right domain for the domain separation logic to work.

## Use cases

When providers have their consumer data separated by domains, the provider tasks, remote tasks, and the corresponding parent tasks are associated with the respective customer domains.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

