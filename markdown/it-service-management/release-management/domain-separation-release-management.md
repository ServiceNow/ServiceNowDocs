---
title: Domain separation and Release Management
description: This is an overview of domain separation and Release Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/release-management/domain-separation-release-management.html
release: zurich
product: Release Management
classification: release-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Release Management, IT Service Management]
---

# Domain separation and Release Management

This is an overview of domain separation and Release Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

**Parent Topic:**[Release Management v2 reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/release-management/reference-release-management.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

