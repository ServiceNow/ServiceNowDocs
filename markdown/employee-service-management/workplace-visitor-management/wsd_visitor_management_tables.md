---
title: About visit-related tables
description: The Workplace Visitor Management application uses three interconnected tables to track everything that happens during a visit from the invitation to the departure. Knowing what each table does helps you configure the application, troubleshoot issues, and know where to look when you have to audit visit activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-visitor-management/wsd\_visitor\_management\_tables.html
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: concept
last_updated: "2026-04-13"
reading_time_minutes: 4
breadcrumb: [Reference, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# About visit-related tables

The Workplace Visitor Management application uses three interconnected tables to track everything that happens during a visit from the invitation to the departure. Knowing what each table does helps you configure the application, troubleshoot issues, and know where to look when you have to audit visit activity.

When someone plans a visit to your workplace, the application records information in the following tables:

-   Visits
-   Invitations
-   Visitor Registrations

## Visits \(sn\_wsd\_visitor\_visit\)

A Visit record is the parent container for a workplace visit and captures the core logistics for the visit.

A Visit record contains the following information:

-   Name of the host, who is the employee creating the visit.
-   Names of the co-hosts, who are additional employees sharing hosting responsibilities.
-   Expected arrival and departure times, as well as the actual arrival and departure times once the visit is underway.
-   The organization the visitors are coming from, if applicable.
-   Any remarks the host wants to note about the visit.
-   Any recurring pattern for visits that repeat on a schedule.

Every invitation and visitor registration in the application is linked to a Visit record. Canceling a visit at this level affects all the invitations and registrations associated with it.

## Invitations \(sn\_wsd\_visitor\_invitation\)

An Invitation record is created for individual attendees of a Visit.

An Invitation record contains the following details:

-   A link to the Visit record it belongs to.
-   Whether the invitee is an internal employee or an external visitor.
-   The visitor type \(for example, client, contractor, or other\).
-   The current state of the invitation, like sent, accepted, or cancelled.
-   A title field for the invitation record itself.

The application automatically sends email notifications when an invitation is created, updated, or cancelled. The emails go directly to the visitor and include details about the visit and the location. An invitation can't be permanently deleted, it can only be made inactive, which preserves a full history of who was invited.

## Visitor Registrations \(sn\_wsd\_visitor\_visitor\_registration\)

A Visitor Registration record includes a visitor's details, check-in status, and any required services.

A Visitor Registration record has the following details:

-   The visitor's name, email address, and phone number.
-   The location the visitor is coming to, and their arrival and departure times.
-   Whether the visitor is flagged as a VIP.
-   Parking details like the parking type and license plate number.
-   Whether the visitor requires Wi-Fi access.
-   A photo of the visitor, which can be uploaded in advance or captured at check-in.
-   The visitor's consent status and the date consent was given, for data privacy compliance.
-   A link to the Invitation that prompted the registration.
-   The current state of the registration, like planned, checked in, checked out, or cancelled.
-   Whether the registration was created by the visitor themselves through self-registration, or on their behalf by a host or receptionist.

Visitor Registration records drive the day-to-day activity in the Receptionist Portal. Actions like checking a visitor in or out, printing a badge, and recording a no-show are all performed on this record. Email notifications are sent to the visitor when their registration is created, updated, or cancelled, and to the host when the visitor checks in.

## How the three records work together

The three records follow a sequence that mirrors the lifecycle of a visit:

1.  A host creates a Visit, establishing the date, time, and location of the event.
2.  The application creates one Invitation for each person invited to that Visit. Notification emails are sent at this point.
3.  As each invitee confirms or registers, a Visitor Registration record is created. This record tracks the visitor from pre-check tasks through to check-out.

A single Visit can have multiple Invitations, and each Invitation can result in one Visitor Registration. If a visit is cancelled, the linked invitations and registrations are updated accordingly and visitors are notified automatically.

**Note:** Records in all three tables are retained even after a visit ends and can't be permanently deleted, which supports audit and compliance requirements. Visitors can opt to anonymize their data, which replaces personal data in the instance with random values.

**Parent Topic:**[Workplace Visitor Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-visitor-management/workplace-visitor-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Visitor Management]()

[Properties installed with Workplace Visitor Management]()

[Kiosk Check-in Flow Configuration form]()

[Kiosk Check-out Flow Configuration form]()

[Kiosk Page Configuration form]()

[Kiosk Page Customizations]()

[Location Policy form]()

[New visit form]()

[Additional requirement form]()

[Differences between Workplace Visitor Management versions]()

