---
title: Domain separation and task outage
description: Domain separation is supported in task outage. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Task Outage
classification: task-outage
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Task Outage, IT Service Management]
---

# Domain separation and task outage

Domain separation is supported in task outage. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Task outage overview

Task-Outage Relationship \[cmdb\_ci\_outage\] is domain separated. Outages are now data separated, meaning they can be exposed to the appropriate personas without risk of data exposure. Fulfillers can view any Task-Outage Relationship records regardless of the domain that the records belong to. The Task-Outage Relationship table is installed when administrator activates the optional Task-Outage Relationship plugin.

**Parent Topic:**[Task Outage](task-outage.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

