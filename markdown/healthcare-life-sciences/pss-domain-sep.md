---
title: Domain separation and Patient Support Services
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Patient Support Services. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Domain separation and Patient Support Services

Domain separation is supported for Patient Support Services. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Patient Support Services overview

The Patient Support Services application includes domain separation for transactional data like enrollment cases and healthcare tasks including program tasks and program service tasks. The application is based on the [Healthcare and Life Sciences data model](hcls-serv-mgmt-core.md) that also includes domain separation.

## How domain separation works in Patient Support Services

For customers using the Patient Support Services application to raise enrollment requests, the domain is set from the logged-in user’s session, in the case and tasks created, and the associated healthcare data.

## Use cases

When healthcare providers have their healthcare data separated by domains, the healthcare requests and corresponding fulfillment tasks are associated with the respective customer domains.

**Parent Topic:**[Patient Support Services reference](../reference/pss-reference.md)

