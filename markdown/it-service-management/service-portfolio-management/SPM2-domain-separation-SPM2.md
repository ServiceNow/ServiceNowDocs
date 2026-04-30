---
title: Domain separation and Service Portfolio Management
description: Domain separation is supported in Service Portfolio Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Portfolio Management reference, Service Portfolio Management, IT Service Management]
---

# Domain separation and Service Portfolio Management

Domain separation is supported in Service Portfolio Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic\*

The support level is Basic but has some exceptions or special conditions.

-   Business logic: Ensure that data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   The user interface, cache keys, reporting, rollups, and aggregations all use the domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

Sample use case: When an SP uses chat to respond to a tenant-customer’s message, the client must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

\*All components of Service Portfolio Management \(SPM\) and Service Owner Workspace \(SOW\) are domain-separated in releases of New York and forward. If using Financial Management for the SPM plugin for estimated spend, there can be only one fiscal calendar defined per instance. When this plugin is activated, there can be only one approach for service offering cost modeling per instance \(using either the Financial Management engine or local data. Different domains cannot choose their own spend model.

**Parent Topic:**[Service Portfolio Management reference](../reference/SPM2-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

