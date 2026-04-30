---
title: Domain separation and Financial Services Card Operations
description: Domain separation is supported for Financial Services Card Operations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up Financial Services Card Operations, Financial Services Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Domain separation and Financial Services Card Operations

Domain separation is supported for Financial Services Card Operations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works in Financial Services Card Operations

All [FSO integrations](../../fso-common/concept/fso-overview.md) applications are built on top of and use many CSM tables. The key reference tables are the customer tables such as Consumer, Account, and Contact, and these tables are domain-separated.

## Tables

All tables added in Card Operations are domain-separated:

-   sn\_bom\_credit\_card\_service
-   sn\_bom\_credit\_card\_task
-   sn\_bom\_credit\_asmt\_task
-   sn\_bom\_document\_task
-   sn\_bom\_credit\_card

**Note:**

There are two system properties that are not domain-separated for Card Operations:

-   sn\_bom\_credit\_card.reserverd\_hours\_to\_unblock\_credit\_card
-   sn\_bom\_credit\_card.reserverd\_hours\_to\_update\_credit\_limit

## Use cases

-   **Credit Card Requests**

    There are six different ServiceNow base system request types for credit cards:

    -   -   New Credit Card Requests
-   Increase Credit Requests
-   Decrease Credit Requests
-   Block Credit Card Requests
-   Unblock Credit Card Requests
-   Close Credit Card Requests
    Customers create these requests from the Customer Service portal \(activated as a separate plugin\)

    Front office workers \(Branch workers, Call Center\) create these requests on behalf of their customers via the Service Catalog and customer interactions

    Each request type has a dedicated flow that triggers tasks from the parent credit card service case.

    -   Credit Card Service Cases are assigned to credit card agents, and used to track the overall credit card request and triggers all tasks.
    -   Credit Card Tasks are assigned to credit card agents, and used for follow-up tasks that are triggered from credit card service cases.
    -   Credit Assessment Tasks are assigned to credit assessment agents, and used in multiple workflows that go beyond credit cards, such as Loan Operations.
    -   Document Service Tasks are assigned to document service agents, and used in multiple workflows that go beyond credit cards, such as Loan Operations.

**Note:** Sometimes a ServiceNow® platform feature or application may be able to effectively support service provider use cases even though the domain framework is not being used. In this case, the application may be assigned Basic\*, Standard\*, or Enhanced\* for its domain support level, and include detailed use cases. For example: Before the New York release, Service Catalog had no domain support. But the instance owner was able to configure separate catalogs and items for each customer in a domain-separated instance. This allowed Service Catalog to be used at a **Standard** support level. To learn more, see domain separation [Application levels of support](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Parent Topic:**[Setting up Financial Services Card Operations](setting-up-fso-card-operations.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

