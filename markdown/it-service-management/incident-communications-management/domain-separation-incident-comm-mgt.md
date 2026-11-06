---
title: Domain separation and Incident Communications Management
description: Incident Communications Management supports domain separation. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/domain-separation-incident-comm-mgt.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident Communications Management reference, Incident Communications Management, IT Service Management]
---

# Domain separation and Incident Communications Management

Incident Communications Management supports domain separation. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Incident Communications Management purpose

-   The Incident Communications Management application enables organizations to create and manage communications related to major business issues or incidents. Incident communication plan administrators can bring together all involved users during these events and establish quick and easy communication within this group.
-   Typically, an incident communication plan administrator or a major incident manager creates incident communication plans for an existing incident. You can create multiple incident communication plans for the same incident.
-   The incident communication plan and incident communication task tables support domain separation. Fulfillers see only incident communication plans or incident communication tasks that have been created within the \(tenant\) domain that they belong to.

## How domain separation works in Incident Communications Management

Fulfillers see only incident communication plans and incident communication tasks that have been created within the \(tenant\) domain that they belong to.

## Domain separated tables

-   Incident Communication Plan \[incident\_alert\]
-   Incident Communication Task \[incident\_alert\_task\]

## Use cases

An incident communication plan administrator or a major incident manager can view only the incidents in domains they have access to. They can create incident communication plans only for those incidents.

**Parent Topic:**[Incident Communications Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/reference-section-inci-comm-mngmt.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

