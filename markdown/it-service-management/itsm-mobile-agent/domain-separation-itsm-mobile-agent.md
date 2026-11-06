---
title: Domain separation for ITSM Mobile Agent
description: Domain separation enables you to separate data, processes, and administrative tasks in ITSM Mobile Agent into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/domain-separation-itsm-mobile-agent.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Mobile Agent reference, ITSM Mobile Agent, IT Service Management]
---

# Domain separation for ITSM Mobile Agent

Domain separation enables you to separate data, processes, and administrative tasks in ITSM Mobile Agent into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Basic support level

-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. This includes domain separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the client must be able to see the SP's response.

## Domain separation support in ITSM Mobile Agent

The mobile platform supports domain separation for all native clients. The mobile UI design clearly indicates the domain that a record is associated with.

Before extending the domain separation functionality to mobile, the feature must be enabled on the platform web-based interface. For further information on configuration, see [Domain separation setup and administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparationSetup.md).

## Domain separation behavior on mobile

You can use the company or account fields to display appropriate records by domain. These fields are available in tables when the domain separation plugin is activated. Each company or account is linked to a single domain. When you create a record, use these fields to specify the target domain.

After the feature has been set up through the platform web-based interface, a two-part process is required to further extend the domain separation functionality on mobile. For additional information about configuring domain separation on mobile devices, contact Customer Service and Support.

## Domain separated tables

-   Incident \[incident\]
-   Incident Task \[incident\_task\]

## Use cases

-   An employee self-service \(ESS\) user in the Initech domain creates an incident. Only ITIL users in the Initech domain or the global domain can see this incident.
-   An ITIL user belonging to a parent domain can see incidents of all its child domains as well.
-   An ITIL user belonging to a specific domain can create incidents only on behalf of the domains that they have access to.
-   An ITIL user can associate child incidents only of those domains that they have access to.
-   If a user has access to multiple domains, the domain specified on the current record drives the functionality of that record and reference fields.

