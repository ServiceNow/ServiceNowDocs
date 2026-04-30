---
title: Domain separation and Health and Safety Risk Management
description: Domain separation is supported for Health and Safety Risk Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Domain separation and Health and Safety Risk Management

Domain separation is supported for Health and Safety Risk Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Domain-separated tables overview

All tables in the Health and Safety Risk Management can be domain-separated and include the required domain separation field.

## How domain separation works in Health and Safety Risk Management

-   Each table in Health and Safety Risk Management includes the domain separation fields **Domain** and **Domain path**.
-   Customers can use these fields to configure domain separation in their implementation of Health and Safety Risk Management.

**Parent Topic:**[Health and Safety Risk Management reference](hs-risk-mgmt-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

