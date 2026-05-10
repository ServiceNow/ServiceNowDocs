---
title: Domain separation and Contract Management Pro
description: Domain separation is supported for Contract Management Pro. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Domain separation and Contract Management Pro

Domain separation is supported for Contract Management Pro. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview of Contract Management Pro domain separation

Contract Management Pro supports domain separation at a basic level, enabling organizations to separate contract data between domains within a single ServiceNow instance. This capability is useful for global enterprises that require data separation across business units, or regions while continuing to use shared platform services and global configurations.

With basic domain separation support, all Contract Management Pro data tables are domain-separated, and data visibility follows the standard domain hierarchy rules.

## How domain separation works in Contract Management Pro

When a user who belongs to a specific domain creates a contract request in Contract Management Pro, the record is created in the domain of the user. Contract users and fulfillers can access only the records that exist within their domain or within child domains, based on the basic domain separation rules.

Domain separation in Contract Management Pro is enabled through the Domain Separation plugin. For more information, see [Request domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_ActivateDomainSeparation.md).

All Contract Management Pro data tables support domain separation.

Because Contract Management Pro supports basic domain separation, workflows and business logic are not domain-separated. Workflows are shared across domains and are configured globally.

Contract templates, clauses, e-signature provider configurations, external storage integrations, and other advanced configurations are created in the TOP domain and can be reused across domains.

## Use cases

-   A managed service provider uses a single ServiceNow instance to manage contracts for multiple customers. Each customer’s contract requests and contract data are created in separate domains, ensuring that users can access only the data relevant to their customer.
-   A global enterprise uses domains to separate contract data by region or subsidiary. Contract managers work only with contracts created within their domain, while administrators in parent domains maintain visibility across multiple domains.

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

