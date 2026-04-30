---
title: Domain separation and Project Portfolio Management
description: Domain separation is supported in Project Portfolio Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: PPM Collaboration
classification: ppm-collaboration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Project Portfolio Management, Strategic Portfolio Management]
---

# Domain separation and Project Portfolio Management

Domain separation is supported in Project Portfolio Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level - Basic\*

-   There is business logic to ensure data goes into the proper domain for the application’s service provider use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all consider domain at run time.
-   The owner of the instance needs to be able to set up the application to function normally across multiple tenants.

Use case: As a service provider when I use chat to respond to a tenant-customer’s message, the client must be able to see my response.

## How domain separation works in Project Portfolio Management

Project Portfolio Management is domain separation-compliant with the following limitations:

-   All PPM entities such as ideas, project, demand, resource plan, and allocations are expected to be in the same domain. A project entity having tasks or resources from multiple domains is not supported.
-   A parent entity and all child entities, such as a project record and its project tasks, are expected to be in the same domain.
-   When you change the domain of a parent record, for example a project record, the domain of the child records are not changed.
-   Only users belonging to the same domain, parent domain, or the top domain have the visibility into PPM entities of a domain.
-   All system properties are in the global domain and are not specific to a domain. Planning console settings, however, are still domain-specific.

**Parent Topic:**[Project Portfolio Management reference](../reference/project-portfolio-management-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

