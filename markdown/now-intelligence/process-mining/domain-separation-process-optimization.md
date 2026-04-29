---
title: Domain separation and Process Mining
description: Domain separation is supported in Process Mining. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Process Mining, Platform Analytics]
---

# Domain separation and Process Mining

Domain separation is supported in Process Mining. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview of Process Mining

Process Mining provides a way to​ generate business process flows from monitoring audit trails and analyzing effectiveness, so you can quickly discover inefficiencies in your processes. This allows in-depth analysis of business processes for improving outcomes.

## How domain separation works in Process Mining

A project is configured to generate the process flow. All entities related to a process model definition, such as activity definitions, breakdown definitions, child table definitions, extract data logs, filter sets, notes, and CIM initiatives are created in the same domain as the process model definition.

When you create a new project definition, you set up its domain in the current user’s domain. Since you place all related entities for a model definition so they reside in the same domain, when you then create a related entity for a domain separated project definition, the entity is assigned to the project definition’s domain.

You can share a project with its own domain or with global domain users.

A Process Mining scheduled Job can include project definitions within the corresponding job’s domain only.

A project definition launched from Performance Analytics KPI is created in the current user’s domain.

A new CIM initiative added from a Process Mining workspace is created in the project definition’s domain.

## Use cases

1.  Project definition created in the ACME domain: A user belonging to the ACME domain, its parent, or the global domain, can view the project definition.
2.  A Process Mining scheduled job created in the ACME domain: A user belonging to the ACME domain, its parent, or the global domain, can view the Process Mining scheduled job.
3.  A Process Mining scheduled job created in the ACME domain: A user can include only a project definition belonging to the ACME domain.

    **Note:** Cascade domain changes are not supported.


**Parent Topic:**[Process Mining reference](process-mining-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

