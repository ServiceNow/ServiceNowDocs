---
title: Domain separation and ServiceNow Voice
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for ServiceNow Voice. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and ServiceNow Voice

Domain separation is supported for ServiceNow Voice. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Domain-separated tables

-   CTI Instance \[sn\_cti\_instance\]
-   CTI Component Logging Configuration \[sn\_cti\_log\_cfg\]
-   Operation Handler \[sn\_cti\_operation\_handler\]
-   Provider Component \[sn\_cti\_provider\_component\]
-   Provider Configuration \[sn\_cti\_provider\_config\]
-   Provider Message Transformer \[sn\_cti\_provider\_msg\_transformer\]
-   CTI user \[sn\_cti\_user\]
-   AWS Resource \[sn\_cti\_aws\_resource\]
-   Amazon Connect Instance \[sn\_cti\_connect\_instance\]

**Parent Topic:**[Setting up ServiceNow Voice](ccc-setup.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

