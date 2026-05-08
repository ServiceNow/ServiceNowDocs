---
title: Domain separation and Incident Communications Management
description: Domain separation is supported in Incident Communications Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Incident Communications Management reference, Incident Communications Management, IT Service Management]
---

# Domain separation and Incident Communications Management

Domain separation is supported in Incident Communications Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see Application support for domain separation.

## Incident Communications Management overview

-   The Incident Communications Management application enables organizations to create and manage communications related to major business issues or incidents. Incident communication plan administrators can bring together all involved users during these events and establish quick and easy communication within this group.

-   Typically, Incident Communication Plan Admin or Major Incident Manager creates incident communication plans for an existing incident. Multiple incident communication plans can be created against the same incident.

-   The incident communication plan and incident communication task tables support domain separation. Therefore, an Itil/Fulfiller sees only incident communication plans or incident communication tasks that have been created within the \(tenant\) domain that they belong to.


## How domain separation works in Incident Communications Management

Fulfillers see only incident communication plan and incident communication plan tasks that have been created within the \(tenant\) domain that they belong to.

## Domain separated tables

-   Incident Communication Plan \[incident\_alert\]
-   Incident Communication Task \[incident\_alert\_task\]

## Use cases

An Incident Communication Plan Admin or Major Incident Manager is able to view incidents only of those domains that they have access to. They can create incident communication plans against only those incidents.

**Parent Topic:**[Incident Communications Management reference](../reference/reference-section-inci-comm-mngmt.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

