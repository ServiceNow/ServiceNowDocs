---
title: Domain separation and synthetic monitoring
description: Domain separation is supported for synthetic monitoring. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Domain separation and synthetic monitoring

Domain separation is supported for synthetic monitoring. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Domain separation and synthetic monitoring overview

Domain separation is present in all aspects of the synthetic monitoring application. Users belonging to a specific domain see only the data existing in their own domain.

## How domain separation works in synthetic monitoring

When data is separated by domains in synthetic monitoring, users can only configure and see the monitoring data in their own domain. By default, all users and records are set to the parent domain unless the admin assigns them to a specific domain.

You define the domain-separated environment when you configure your data inputs. All relevant records and data processing in the synthetic monitoring program flow reside in the same domain as the data input. The domain name of a data input appears in the Domain column that is displayed in the tables in your instance.

Using domain separation in your instance is transparent to synthetic monitoring. The application manages all aspects of the data, such as the monitor configurations and results. When a property is changed, the new value affects new sources only in the specific domain.

When setting up Agent Client Collector \(ACC\) for non-hosted synthetic checks, each domain that supports non-hosted synthetics requires its own ACC cluster and MID Server. The ACC cluster and MID Server must be created in a leaf domain.

**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

