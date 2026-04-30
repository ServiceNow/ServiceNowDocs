---
title: Domain separation and Financial Services Card Operations
description: Domain separation is supported for Financial Services Card Operations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Financial Services Card Operations, Card Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Domain separation and Financial Services Card Operations

Domain separation is supported for Financial Services Card Operations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## How domain separation works in Financial Services Card Operations

All [Financial Services Operations \(FSO\)](../../fso-common/concept/fso-overview.md) applications are built on top of and use many CSM tables. The key reference tables are the customer tables such as Consumer, Account, and Contact, and these tables are domain-separated.

## Tables

All tables added in Card Operations are domain-separated:

-   sn\_bom\_credit\_card\_base
-   sn\_bom\_credit\_card\_cardholder\_dispute\_intake
-   sn\_bom\_credit\_card\_case
-   sn\_bom\_credit\_card\_disputes\_related\_transaction
-   sn\_bom\_credit\_card\_disputes\_service
-   sn\_bom\_credit\_card\_disputes\_task
-   sn\_bom\_credit\_card\_disputes\_transaction
-   sn\_bom\_credit\_card\_dispute\_intake
-   sn\_bom\_credit\_card\_service
-   sn\_bom\_credit\_card\_task

## Use cases

-   **Credit Card Requests**

    There are several different ServiceNow base system request types for credit cards, such as:

    -   New credit card requests
    -   Increase/decrease credit card limit
    -   Block/unblock credit card
    -   Close credit card
    -   Dispute card transactions
    Customers create requests from the Customer Service portal \(activated as a separate plugin\).

    Front office workers \(Branch workers, Call Center\) create these requests on behalf of their customers via the Service Catalog and customer interactions.

    Each request type has a dedicated flow that triggers tasks from the parent credit card service case. Examples include:

    -   Credit Card Service Cases are assigned to credit card agents, and used to track the overall credit card request and triggers all tasks.
    -   Credit Card Tasks are assigned to credit card agents, and used for follow-up tasks that are triggered from credit card service cases.
    -   Credit Assessment Tasks are assigned to credit assessment agents, and used in multiple workflows that go beyond credit cards.
    -   Document Verification Tasks are assigned to document processor agents, and used in multiple workflows that go beyond credit cards.
    -   Card Disputes Tasks are created for disputed transactions and assigned to card dispute agents, and are used to track the resolution progress for the dispute.

**Note:** Sometimes a ServiceNow® platform feature or application may be able to effectively support service provider use cases even though the domain framework is not being used. In this case, the application may be assigned Basic\*, Standard\*, or Enhanced\* for its domain support level, and include detailed use cases. For example: Before the New York release, Service Catalog had no domain support. But the instance owner was able to configure separate catalogs and items for each customer in a domain-separated instance. This allowed Service Catalog to be used at a **Standard** support level. To learn more, see domain separation [Application levels of support](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

