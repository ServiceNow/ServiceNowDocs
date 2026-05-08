---
title: Domain separation and Coaching
description: Domain separation is supported in Coaching. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Coaching, IT Service Management]
---

# Domain separation and Coaching

Domain separation is supported in Coaching. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Domain Separation Overview



All tables including Coaching Opportunity, Coaching Assessment, Virtual Coach, and Trainings support domain separation so the coach and Coaching admin can view records within the \(tenant\) domain to which they belong.

## How domain separation works in Coaching

Domain separation is supported in Coaching with no setup or configuration required. You can create coaching opportunities and coaching assessments in separate domains, including the global domain.

Coaching assessments extend the platform Task \[task\] table.

When domain separation is implemented, coach and trainee users can view coaching assessments and trainings only in the domain assigned. The **Domain** and **Domain Path** columns are available for coaching opportunities, coaching assessments, virtual coaching, and trainings provided with the base system.

The **Domain** column contains the name of the domain to which the event or alert belongs, and the **Domain Path** column contains the unique domain identifier.

**Note:** If the domain column is not shown, select the **Update Personalized List** icon and add the required column. You can also add the domain path column, if desired.

## Domain-separated tables

-   Coaching Assessment \[sn\_coaching\_assessment\]
-   Coaching Opportunity \[sn\_coaching\_opportunity\]
-   Trainings \[sn\_coaching\_recommendation\]
-   Assigned Training \[sn\_coaching\_assessment\_recommended\_learning\]
-   Assigned Training \[sn\_coaching\_opportunity\_recommended\_learning\]
-   Virtual Coach \[sn\_coaching\_opportunity\_virtual\_coach\_m2m\]
-   Virtual Coaching \[sn\_coaching\_virtual\_coach\]

## Use cases

-   A Coaching admin that belongs to a parent domain creates a coaching opportunity at a parent domain level or at a child domain level. Coaching opportunities created at a parent level are available to view in all domains.
-   A Coaching admin has access to multiple domains but wants to update content in a record within a specific domain. The domain specified in the record drives the functionality of that record and reference fields.
-   A Coaching user that belongs to the Acme domain can view the coaching assessment task created in the Acme domain.
-   A Coaching user wants to associate an assigned training for an integrated application in the Acme domain. The user must belong to the domain of the integrated application from which a record is associated.
-   The trainee user of a parent domain can view a coaching assessment of the parent as well as of all child domains of that parent. A trainee user must belong to the Acme domain, its parent domain, or the global domain to view that coaching assessment.

**Parent Topic:**[Coaching reference](../reference/cf-coaching-reference.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

