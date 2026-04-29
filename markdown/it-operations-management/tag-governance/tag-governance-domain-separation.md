---
title: Domain separation and Tag Governance
description: Domain separation is supported in Tag Governance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tag Governance reference, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Domain separation and Tag Governance

Domain separation is supported in Tag Governance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Domain separation

You can identify CIs or cloud resources that are inconsistent and do not comply with the policies that you configure to govern tag data. In Tag Governance, domain separation targets tenant domain requester use cases in an application. The application has been designed to support requester activities within tenant domains. Logic is in place to route data to tenant domains, based on applicable use cases. The owner of the instance must be able to set up the application to function normally across multiple tenants. The application handles data routing to domains.

All tables in Tag Governance support data separation only; delegated domain separation is not supported.

To ensure that domain-sensitive information is not available at a global domain, ensure that you create policies at a domain level and not at a global level. While managing service providers, create policies at the service provider level. If you create policies at a global level instead, when you run the audit, the "run" findings are created in the Global domain instead of respective domains.

**Parent Topic:**[Tag Governance reference](reference-tag-governance.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

