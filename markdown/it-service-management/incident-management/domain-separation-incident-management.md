---
title: Domain separation and Incident Management
description: Domain separation is supported in Incident Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference section for Incident Management, Incident Management, IT Service Management]
---

# Domain separation and Incident Management

Domain separation is supported in Incident Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see Application support for domain separation.

## Incident Management overview

-   The goal of Incident Management is to restore normal service operation as quickly as possible, while minimizing impact to business operations and ensuring quality is maintained.

-   Typically, end users log incidents when a service they are using is impacted or not available. ITIL / Fulfiller users in your organization classify these incidents, route them as appropriate and work on resolving the incident.

-   The incident and incident task tables support domain separation. Therefore, a Fulfiller sees only incidents or incident tasks that have been created within the \(tenant\) domain that they belong to.


## How domain separation works in Incident Management

Fulfillers see only incidents and incident tasks that have been created within the \(tenant\) domain that they belong to.

## Incident Management domain separated tables

-   Incident \[incident\]
-   Incident Task \[incident\_task\]

## Incident Management use cases

-   An ESS user belonging to “Initech” domain, creates an incident. Only those ITIL users belonging to “Initech” domain or global domain can see this incident.
-   An ITIL user belonging to a parent domain can see incidents of all its child domains as well.
-   An ITIL user belonging to a specific domain can create incidents only on behalf of the domains that they have access to.
-   An ITIL user can associate child incidents only of those domains that they have access to.
-   If a user has access to multiple domains, the domain specified on the current record drives the functionality of that record and reference fields.

**Parent Topic:**[Reference section for Incident Management](../reference/reference-section-for-incident-management.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

