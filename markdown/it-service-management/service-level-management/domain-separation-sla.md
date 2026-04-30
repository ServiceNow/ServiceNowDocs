---
title: Domain separation and Service Level Management
description: Domain separation is supported in Service Level Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Service Level Management, IT Service Management]
---

# Domain separation and Service Level Management

Domain separation is supported in Service Level Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Service Level Management overview

-   Service Level Management helps customers monitor, measure, and report on agreed service level agreements \(SLAs\); SLA definitions encapsulate these agreements.
-   Users can see only content in the domain to which they have access.

## How domain separation works in Service Level Management

The intention of SLM is to provide customers with an expectation of service within a known timescale and the ability to monitor when service levels are not being met. To learn specific terms and definitions see [Service Level Management concepts](service-level-management-concepts.md).

-   SLA definitions and task SLAs have domain fields. However, task SLAs are created only in the domain of its attached task record.
-   SLA definitions must be defined in a tenant domain \(or global\) in order for task SLAs to be created and attached to a given task \(or extensions\).
-   Task SLAs attach to a task if an SLA definition exists in the task records domain or in an ancestor domain.
-   Task SLAs always inherit the domain of its attached task record, which includes the workflow running on the task SLA record. If a task record ever flips, the task SLA also slips.
-   If an SLA definition exists in an ancestor’s domain, the definition can be overridden in a sub-domain \(delegated administration\).

## Service Level Management domain-separated tables

-   SLA definition \[contract\_sla\]
-   Task SLA \[task\_sla\]

## Service Level Management use cases

-   An ESS user in the ACME domain logs in and creates an incident, at which point an SLA is attached. The SLA is created in the domain of the associated task record \(incident\), which is the ACME domain. The ESS user is not able to read SLA records. These are restricted to the following roles:
    -   Administrator
    -   ITIL
    -   SLA Administrator
    -   SLA Manager
-   An ITIL user in the Acme domain logs in and creates an incident. The process above is the same except that the ITIL user can read the SLA record attached to the incident.
-   If an SLA definition exists in the Acme domain and doesn’t meet the needs of an Acme sub-domain \(Acme child\) an SLA Administrator can remediate. SLA Administrators can navigate to the ACME SLA definition when their session domain is ACME child, make the relevant changes, and save them. The SLA Administrator is alerted that an override has been created.
-   An ITIL user sets the session domain to Acme child and creates an incident. The task SLA is created using the SLA definition from Acme child.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

