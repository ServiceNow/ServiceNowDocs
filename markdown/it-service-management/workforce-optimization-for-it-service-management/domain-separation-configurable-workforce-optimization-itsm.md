---
title: Domain separation and Workforce Optimization for ITSM
description: Domain separation is supported in Workforce Optimization for ITSM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced configurations, Workforce Optimization for ITSM, IT Service Management]
---

# Domain separation and Workforce Optimization for ITSM

Domain separation is supported in Workforce Optimization for ITSM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## How domain separation works in Workforce Optimization for ITSM

Domain separation is supported in Workforce Optimization for ITSM and does not require any setup or configuration.

## Domain separation for Channels in Workforce Optimization for ITSM

For information on how domain separation works in Channel Management for Workforce Optimization for Customer Service, refer to Domain separation and Advanced Work Assignment.

Domain separated tables for Channel Management

-   sn\_customerservice\_case
-   interaction

## Domain separation for Scheduling in Workforce Optimization for ITSM

When an agent schedule is generated and assigned to an agent, the schedule is only available in the domain to which that agent belongs.

Domain separated tables for Scheduling

-   sn\_shift\_planning\_agent\_schedule
-   sn\_shift\_planning\_agent\_schedule\_request
-   sn\_shift\_planning\_break
-   sn\_shift\_planning\_day
-   sn\_shift\_planning\_event
-   sn\_shift\_planning\_schedule\_plan
-   sn\_shift\_planning\_schedule\_shift
-   sn\_shift\_planning\_schedule\_shift\_agent
-   sn\_shift\_planning\_shift\_plan
-   sn\_shift\_planning\_shift\_swap\_request

## Domain separation for Teams in Workforce Optimization for ITSM

The **sn\_wfo\_add\_manager** table is domain separated. When users are added as additional managers, those users can only view users within that domain.

## Domain separation for Skill Recommendation in Workforce Optimization for ITSM

Domain separated tables for Skill Recommendation

-   sn\_sre\_task\_predicted\_skill
-   sn\_sre\_user\_predicted\_skill

## Domain separation for Coaching in Workforce Optimization for ITSM

For information on how domain separation works in Coaching for Workforce Optimization for ITSM, refer to [Domain separation and Coaching](../../cf-coaching/concept/cf-domain-separation-coaching.md).

**Parent Topic:**[Advanced configurations for Workforce Optimization for ITSM](advanced-configuration-workforce-optimization-itsm.md)

