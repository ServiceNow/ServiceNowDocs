---
title: Domain separation and Financial Services Document Processor
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.Domain separation is supported for Financial Services Document Processor. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Domain separation and Financial Services Document Processor

Domain separation is supported for Financial Services Document Processor. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works in Financial Services Document Processor

All [FSO integrations](fso-overview.md) applications are built on top of Customer Service Management \(CSM\) and use many CSM tables. The key reference tables are the customer tables such as Consumer, Account, and Contact, and these tables are domain-separated.

## Tables

All new tables added in Document Processor are domain-separated:

-   -   sn\_doc\_processor\_category
-   sn\_doc\_processor\_type
-   sn\_doc\_processor\_m2m\_category\_type
-   sn\_doc\_processor\_attribute
-   sn\_doc\_processor\_list
-   sn\_doc\_processor\_list\_item
-   sn\_doc\_processor\_verification\_task
-   sn\_doc\_processor\_extracted\_value
-   sn\_doc\_processor\_document

## Use cases

-   Ability to use in any workflow in Financial Services Operations applications to collect and validate customer documents
-   Ability to request deferment or exception of a document.
-   When integrated with Document Intelligence, ability to extract and store document data attributes.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

