---
title: Domain separation and SRM
description: Domain separation is supported for Service Reliability Management \(SRM\).This needs to be updated with correct version.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Reliability Management reference, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Domain separation and SRM

Domain separation is supported for Service Reliability Management \(SRM\).

## Support level: Basic\*

The support level is Basic but has some exceptions or special conditions.

-   Business logic: Ensure that data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   The user interface, cache keys, reporting, rollups, and aggregations all use the domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

Sample use case: When an SP uses chat to respond to a tenant-customer’s message, the client must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview of domain separation

-   Domain separation is present in all metadata tables in the application. Instance level tables also have domain separation explicitly. Other internal tables, such as the internal Team Request table, are domain-separated implicitly by referencing domain-separated records.
-   System properties are not domain-separated, which has implications for Team Management features. The properties are shared by multiple domains and are set at the instance level. Domain-specific setup for these is not supported.
-   Where another application is being leveraged \(for example the Event Management Connectors\) domain separation is determined by the domain-separation capabilities of that application.

## How domain separation works in the Service Reliability Management application

The specific conditions indicated by the Basic\* support level rating above relate to team management:

-   New teams created through a catalog item backed by an Integration Hub flow are setup by the Service Operations Workspace administrator. They can initiate it from the Service Portal. An SRM admin, manager or responder can do it through the SRM workspace. Instructions appear in the SRM documentation.
-   Integration Hub subflows and actions control management of SRM teams.
-   Only one catalog item and flow can be set up for each instance. The customer is responsible for setting up team properties to support domain separation as a customization of the existing flows.
-   The requestor of a team catalog item is associated with the domain and is available as part of the request item. As a result, if needed, the requester can create the team in a specific domain or the catalog Item and extend it to capture the domain another way. In either case, the Service Operations Workspace must make changes to the Integration Hub flows and actions to support this.

For more information, see [Domain separation and On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/domain-separation-on-call-scheduling.md).

**Parent Topic:**[Service Reliability Management reference](../reference/service-reliability-management-reference.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

