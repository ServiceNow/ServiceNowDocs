---
title: Domain separation and Service Observability
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Service Observability. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Domain separation and Service Observability

Domain separation is supported for Service Observability. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Domain separation and Service Observability overview

Domain separation is present in all aspects of the synthetic monitoring application. Users belonging to a specific domain see only the data existing in their own domain.

## How domain separation works in Service Observability

When data is separated by domains in Service Observability, users can only configure and see the observability data in their own domain. By default, all users and records are set to the parent domain unless the admin assigns them to a specific domain.

You define the domain-separated environment when you configure your data inputs. All relevant records and data processing in the Service Observability program flow reside in the same domain as the data input. The domain name of a data input appears in the Domain column that is displayed in the tables in your instance.

Service Observability manages all aspects of the data, such as the data mappings and the data displayed on dashboards. When a property is changed, the new value affects new sources only in the specific domain.

**Parent Topic:**[Service Observability reference](service-observability-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

