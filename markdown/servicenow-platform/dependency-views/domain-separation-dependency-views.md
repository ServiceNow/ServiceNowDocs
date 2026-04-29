---
title: Domain separation and Dependency Views
description: Domain separation is unsupported in Dependency Views. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Dependency Views

Domain separation is unsupported in Dependency Views. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## How domain separation works in Dependency Views

Dependency views are generated using both Configuration Item \[cmdb\_ci\] and CI Relationship \[cmdb\_rel\_ci\] tables. The \[cmdb\_ci\] table is domain separated, but the \[cmdb\_rel\_ci\] table is not. You can create relationships only by selecting two CIs. They should be in the same domain for you to be able to see them.

To be successful with domain separation in Dependency Views, make sure that relevant CIs are visible for the current domain. If the instance is domain separated, ServiceNow domain separation rules apply \(see Related information link below\).

Tenant domains will be able to see only their domain and global CIs.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

