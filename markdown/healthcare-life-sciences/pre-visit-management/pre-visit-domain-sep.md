---
title: Domain separation and Pre-Visit Management
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Pre-Visit Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Pre-Visit Management
classification: pre-visit-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Pre-Visit Management reference, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Domain separation and Pre-Visit Management

Domain separation is supported for Pre-Visit Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Overview

The Pre-Visit Management application includes domain separation for transactional data like procedure request cases. The application is based on the [Healthcare and Life Sciences data model](hcls-serv-mgmt-core.md) that also includes domain separation.

## How domain separation works in Pre-Visit Management

For customers using the Pre-Visit Management application to raise procedure requests, the domain is set from the logged-in user’s session, in the case created, and the associated healthcare data.

## Use cases

When healthcare providers have their healthcare data separated by domains, the healthcare requests and corresponding fulfillment tasks are associated with the respective customer domains.

**Parent Topic:**[Pre-Visit Management reference](../reference/pre-visit-reference.md)

