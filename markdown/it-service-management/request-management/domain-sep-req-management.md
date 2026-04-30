---
title: Domain separation in Request Management
description: This is an overview of domain separation in Request Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Request Management
classification: request-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Request Management, IT Service Management]
---

# Domain separation in Request Management

This is an overview of domain separation in Request Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Activation information

The Domain Support - Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\) should be activated to enable domain separation for Request Management. For information on how you can request for this plugin activation, see [Request domain separation](https://www.servicenow.com/docs/access?context=t_ActivateDomainSeparation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## How domain separation works in Request Management

Fulfillers see only requests, requested items, and catalog tasks that have been created within the \(tenant\) domain for which the fulfiller has the visibility. For information on visibility in domain hierarchies, see [Visibility domains and Contains domains](https://www.servicenow.com/docs/access?context=c_DomainVisibility&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Domain separated tables

-   Request \[sc\_request\]
-   Requested Item \[sc\_req\_item\]
-   Catalog Task \[sc\_task\]

## Use cases

-   A user belonging to “Initech” domain, submits a request. Only those fulfillers belonging to “Initech” domain or global domain can see this request.
-   A fulfiller belonging to a parent domain can see requests, requested items, and catalog tasks of all its child domains as well.
-   A fulfiller belonging to a specific domain can create requests only on behalf of the domains that they have access to.
-   If a user has access to multiple domains, the domain specified on the current record drives the functionality of that record and reference fields.

**Parent Topic:**[Request Management reference](../../request-management/concept/request-management-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

