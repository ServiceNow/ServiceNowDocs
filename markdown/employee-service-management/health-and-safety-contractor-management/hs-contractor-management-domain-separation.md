---
title: Domain separation and Health and Safety Contractor Management
description: Domain separation is supported for Health and Safety Contractor Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Health and Safety Contractor Management
classification: health-and-safety-contractor-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Health and Safety Contractor Management, Health and Safety, Employee Service Management]
---

# Domain separation and Health and Safety Contractor Management

Domain separation is supported for Health and Safety Contractor Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Domain-separated tables overview

All tables in the Health and Safety Contractor Management can be domain-separated and include the required domain separation field.

## How domain separation works in Health and Safety Contractor Management

-   Each table in Health and Safety Contractor Management includes the domain separation fields **Domain** and **Domain path**.
-   Customers can use these fields to configure domain separation in their implementation of Health and Safety Contractor Management.

**Parent Topic:**[Health and Safety Contractor Management reference](hs-contractor-management-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

