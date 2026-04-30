---
title: Domain separation and Third-party Risk Management
description: Domain separation is supported for TPRM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Domain separation and Third-party Risk Management

Domain separation is supported for TPRM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Domain separation overview

The ServiceNow® GRC: Third-party Risk Management \(TPRM\) application enables you to proactively identify, assess, and mitigate risks that are associated with your third-party relationships. TPRM provides a centralized process for managing your portfolio of third parties, assessing and scoring risk, and performing remediation. TPRM supports domain separation at the basic level \(level 0 or data level\). Your Managed Service Provider can configure TPRM at the process level of domain separation.

## How domain separation works in TPRM

-   All TPRM tables support the data level of domain separation. No special setup is needed except for adding the domain-related columns to form views or list views.
-   When TPRM is installed to an instance where domain separation is activated, all TPRM data is automatically domain-separated. See the platform domain separation documentation for details.

## Use cases

Tenant domains manage their own application data in the same way as data is managed on an instance.

## Domain-separated tables

There is no **Domain** column in TPRM application tables.

All TPRM tables support data-level domain separation with sys\_domain and sys\_domain\_path columns.

**Parent Topic:**[Third-party Risk Management reference](tprm-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

