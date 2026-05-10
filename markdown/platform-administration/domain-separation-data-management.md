---
title: Domain separation and Data Management
description: Domain separation is supported in Data Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Domain separation and Data Management

Domain separation is supported in Data Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic

-   There is business logic to ensure data goes into the proper domain for the application’s service provider use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all consider domain at run time.
-   The owner of the instance needs to be able to set up the application to function normally across multiple tenants.

Use case: As a service provider when I use chat to respond to a tenant-customer’s message, the client must be able to see my response.

## Overview

Data archiving supports [Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md). For example, incidents that belong to a domain keep their domain designation even after they are archived.

**Parent Topic:**[Data Management reference](../reference/data-management-reference.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

