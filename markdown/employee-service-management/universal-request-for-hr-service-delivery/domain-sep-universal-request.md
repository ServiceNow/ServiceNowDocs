---
title: Domain separation and Universal Request
description: Domain separation is supported for ServiceNow Universal Request. Universal Request helps Help Desk agents to resolve cases across the enterprise for a better employee experience. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Domain separation and Universal Request

Domain separation is supported for ServiceNow Universal Request. Universal Request helps Help Desk agents to resolve cases across the enterprise for a better employee experience. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## How domain separation works in Universal Request

All configurations are strictly domain separated.

The Universal Request table is data-separated.

## Tables

Configuration tables \(strict domain separation\)

-   universal\_request\_service\_set
-   universal\_request\_service\_conf
-   universal\_request\_state\_mapping
-   universal\_request\_route\_conf
-   universal\_request\_transfer\_mapping
-   universal\_request\_transfer\_fields\_mapping

Data tables \(data separated\): universal\_request.

**Parent Topic:**[Setting up and configuring Universal Request](setup-configure-ur.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

