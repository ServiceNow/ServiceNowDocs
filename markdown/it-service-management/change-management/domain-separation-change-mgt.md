---
title: Domain separation and Change Management
description: Change Management supports domain separation. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/domain-separation-change-mgt.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Reference, Change Management, IT Service Management]
---

# Domain separation and Change Management

Change Management supports domain separation. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Domain separation in Change Management overview

Change Management provides a systematic approach to controlling the life cycle of all changes, facilitating beneficial changes with minimum disruption to IT services.

## How domain separation works in Change Management

Change management involves the management of change requests. A change request enables you to implement a controlled process for the addition, modification, or removal of approved and supported configuration items \(CIs\). The request records the detailed information about the change, such as the reason for the change, the priority, the risk, the type of change, and the change category.

-   The Change Request table extends the Task table. Records are created in the session domain of the user who creates the task.
-   All change properties are global, meaning they are the same for every application that uses the System Property \[sys\_properties\] table. This table isn't domain-separated, so any changes affect all domains.

**Domain separated tables**

Change Request \[change\_request\].

**Use case**

A user with the itil role in the ACME domain logs in and creates a change request. The change request is created in the domain that the user has selected.

## How domain separation works in Change Advisory Board \(CAB\) Workbench

-   CAB meetings synchronize with the CAB Definition table if the meeting was generated from a definition, or the meeting was created manually and has the CAB Definition field populated.
-   CAB meetings are created in the domain of the user if the meeting is created manually without an associated CAB definition.
-   Meeting records in a different domain from the associated definition aren't supported.
-   All other CAB records have their domain master set to the associated CAB Meeting record.

**Domain separated tables**

-   CAB Definition \[cab\_definition\]
-   CAB Meeting \[cab\_meeting\]

**Domain tables \(linked to domain of its associated cab\_meeting\)**

-   CAB Attendee \[cab\_attendee\]
-   CAB Agenda Item \[cab\_agenda\_item\]
-   CAB Runtime State \[cab\_runtime\_state\]

**Use cases**

-   A CAB manager creates a new CAB definition and generates 20 meetings while in the ACME domain. Result: Both the definition and meetings are created within the ACME domain.

-   A CAB manager creates an ad-hoc CAB meeting from the related list on the CAB definition form. Result: The meeting is created in the domain of the CAB meeting.
-   All other use cases behave in the same way as when domain separation is not enabled.

## How domain separation works in Change Schedules

-   Change Schedule definitions encapsulate all the configuration options and related records used to display a given Change Schedule.
-   Records are created in the domain of the current user.
-   Ancillary records are created in the domain of the Change Schedule definition.

**Domain separated tables**

-   Change Schedule Definition \[chg\_soc\_definition\]
-   Related Definition \[chg\_soc\_definition\_child\]
-   Style Rule \[chg\_soc\_definition\_style\_rule\]
-   Style Rule \[chg\_soc\_style\_rule\]
-   Style Rule \[chg\_soc\_def\_child\_style\_rule\]

**Use cases**

A user with the itil role in the ACME domain logs in and navigates to the Change Schedule landing page. The user can view the Change Schedules in both their current domain and the global domain.

**Parent Topic:**[Reference section for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/reference-change-management.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

