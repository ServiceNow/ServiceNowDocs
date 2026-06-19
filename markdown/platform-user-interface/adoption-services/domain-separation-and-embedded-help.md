---
title: Domain separation and Embedded Help
description: Domain separation is supported for Embedded Help. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/adoption-services/domain-separation-and-embedded-help.html
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Embedded Help reference, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Domain separation and Embedded Help

Domain separation is supported for Embedded Help. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Domain separation overview

The goal of Embedded Help is to enable your users to benefit from base system help topics, as well as to create your own custom help topics. If your organization uses domain separation, you can create custom embedded help for each domain.

## How domain separation works in Embedded Help

If your organization uses domain separation, you can create custom embedded help for each domain. To associate help content with a domain, the administrator configures the help content form to include the **Domain** field. When custom content is created, the author selects the domain to which the content applies.

**Note:**

-   Content with no specified domain is in the global domain.
-   If domain-specific content does not exist for a user in a domain, the user sees the global help content.
-   Users in the global domain only see global help content. An administrator who wants to test domain-specific help must impersonate a user in that domain.

**Parent Topic:**[Embedded Help reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/adoption-services/embedded-help-reference.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

