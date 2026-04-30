---
title: Domain separation and Problem Management
description: Domain separation is supported in Problem Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Domain separation and Problem Management

Domain separation is supported in Problem Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Domain separation in Problem Management - Overview

-   Problem Management is about eliminating the root cause of a service interruption.
-   The problem and problem task tables support domain separation. Therefore a Problem user sees only problems or problem tasks that have been created within the \(tenant\) domain that they belong to.
-   Only Problem users can create and access Problems and problem tasks.
-   Problem and problem task tables both support domain separation. Therefore, a Problem user sees only problems and problem tasks that have been created within the \(tenant\) domain that they belong to.

## How domain separation works in Problem Management

Problem users see only problems and problem tasks that have been created within the \(tenant\) domain that they belong to.

Problem users can use Problems and problem tasks within the tenant domains. Problem users can create and update problems and problem tasks of their domain, any child domains, and the global domain.

## Known Issues

Task-Outage Relationship `[cmdb_ci_outage]` is not domain separated.

If installed, the Task-Outage Relationship table is not domain separated. Therefore Fulfillers or Problem users can view any Task-Outage Relationship records regardless of the domain that the records belong to.

The Task-Outage Relationship table is installed when administrator activates the optional Task-Outage Relationship plugin.

**Parent Topic:**[Reference section for Problem Management](reference-section-for-problem-management.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

