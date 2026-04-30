---
title: Domain separation in Agile Development 2.0
description: This is an overview of domain separation and how it works with Agile Development 2.0. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Agile Development 2.0, Strategic Portfolio Management]
---

# Domain separation in Agile Development 2.0

This is an overview of domain separation and how it works with Agile Development 2.0. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## How domain separation works in Agile Development 2.0

-   The entities in Agile 2.0 extend the functions of task, so they inherit the domain behavior of tasks. The new entries you create go into the domain of the user currently logged in.
-   [Agile Board](../../sdlc-scrum/concept/agile-board.md) honors domain separation and lists the groups that the user belongs to for Sprint Planning and Sprint Tracking pages. The backlog entries that display are in the same domain as those that the current user owns or shares with other users. The stories that display in Agile Board are limited to the domain of the current logged-in user.

**Parent Topic:**[Agile Development 2.0 reference](../reference/agile-development-2-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

