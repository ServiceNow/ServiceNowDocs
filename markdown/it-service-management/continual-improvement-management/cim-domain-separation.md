---
title: Domain separation and Continual Improvement Management
description: Domain separation in Continual Improvement Management is configured to apply to all features of the application. Separation of data is configured along with separation of logic and process. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Overview, Continual Improvement Management, IT Service Management]
---

# Domain separation and Continual Improvement Management

Domain separation in Continual Improvement Management is configured to apply to all features of the application. Separation of data is configured along with separation of logic and process. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Domain separation overview



When an improvement opportunity is discovered within your organization, you can implement the improvement in a structured manner using Continual Improvement Management with domain separation.

Once an improvement initiative is created, the Improvement Manager uses the Improvement Register to review and prioritize the improvement, and assigns improvement tasks. CIM task owners are responsible to fulfill assigned tasks to the desired outcome of that improvement. Both Improvement Register and CIM Task tables support domain separation so the Improvement Requester, task owners, Improvement Coordinator, and Improvement Manager can view only the improvement initiatives and related tasks within the \(tenant\) domain to which they belong.

## How domain separation works in Continual Improvement Management

Domain separation is supported in Continual Improvement Management with no CIM setup or configuration required. Improvements can be created in separate domains, including the global domain.

Continual Improvement Management extends the platform Task \[task\] table.

When domain separation is implemented, CIM users can view and request improvements initiatives only in the domain assigned. **Domain** and **Domain Path** columns are available for two main CIM tables \(Improvement Register and CIM Tasks\) provided with the base system. The **Domain** column contains the name of the domain to which the event or alert belongs, and the **Domain Path** column contains the unique domain identifier.

|Table|Contents|
|-----|--------|
|\[sn\_cim\_register\]|Improvement Initiatives|
|\[sn\_cim\_task\]|CIM Tasks|

**Note:** If the domain column is not shown, click the **Update Personalized List** icon and add the required column. You can also add the domain path column, if desired.

Use cases:

-   An Improvement Requester that belongs to the Acme domain creates an improvement initiative and wants to view it.

    A user must belong to the Acme domain, its parent domain, or the global domain to view the improvement initiative.

-   An Improvement Manager that belongs to a parent domain tries to view an improvement initiative in a child domain.

    The user of a parent domain can view improvement initiatives of the parent as well as all child domains of that parent.

-   An Improvement Requester that belongs to Acme domain wants to create an improvement initiative on behalf of another user in the Acme domain.

    A user must belong to the same domain as the user for which the improvement initiative is created.

-   An Improvement Requester wants to associate a record for an integrated application in the Acme domain.

    A user must belong to the domain of the integrated application from which a record is associated.

-   An Improvement Manager has access to multiple domains, but wants to update a record with content within a specific domain.

    The domain specified for the current record drives the functionality of that record and reference fields.


**Parent Topic:**[Continual Improvement Management overview](get-started-cim.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

