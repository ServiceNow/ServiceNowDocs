---
title: Domain separation and Event Management
description: Domain separation is supported in Event Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/domain-separation-event-management.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Domain separation and Event Management

Domain separation is supported in Event Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## How domain separation works in Event Management

When domains are separated in Event Management, users can only see and manage alerts and events in their own \(tenant\) domain.

A domain column is present for Event Management tables that are provided in the base system. The column displays the name of the domain to which the event or alert belongs.

**Note:**

If the domain column does not display in the list, click \[Omitted image "update-personalized-list.png"\] Alt text: Update Personalized List \(Update Personalized List\) and add the required column. In addition, you can add a column that displays the domain path.

For information about domain separation limitations in Event Management, see [Configure Event Management domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMConfigureDomainSeparation.md).

**Related topics**  


[bundle-psec.domain-sep-landing-page]

