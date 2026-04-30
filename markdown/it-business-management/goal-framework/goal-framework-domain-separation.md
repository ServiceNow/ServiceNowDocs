---
title: Domain separation and Goal Framework
description: Domain separation is supported for Goal Framework and Goal Framework for SPM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Domain separation and Goal Framework

Domain separation is supported for Goal Framework and Goal Framework for SPM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works in Goal Framework and Goal Framework for SPM

After you enable domain separation on your ServiceNow instance, the Goal Framework and Goal Framework for SPM data is automatically domain separated. The goals and targets data of portfolio plans for different domains are visible to only those users who have access to these domains.

**Parent Topic:**[Goal Framework and Goal Framework for SPM reference](../reference/goal-framework-reference.md)

