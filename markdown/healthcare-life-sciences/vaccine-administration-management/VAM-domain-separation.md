---
title: Domain separation and Vaccine Administration Management
description: Domain separation is supported for Vaccine Administration Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Domain separation and Vaccine Administration Management

Domain separation is supported for Vaccine Administration Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

The Vaccine Administration Management application includes domain separation for transactional data like vaccination programs and vaccination appointments. The application is based on the [Healthcare and Life Sciences data model](../../healthcare-life-sciences/concept/hcls-serv-mgmt-core.md) that also includes domain separation.

## How domain separation works in Vaccine Administration Management

For customers using the Vaccine Administration Management application to register for vaccination programs and book appointments, the domain is set from the logged-in user’s session, in the record created, and the associated healthcare data.

## Use cases

When healthcare providers have their healthcare data separated by domains, the healthcare requests and corresponding fulfillment tasks are associated with the respective customer domains.

