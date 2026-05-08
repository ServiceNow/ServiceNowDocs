---
title: Domain separation in Workforce Optimization for Customer Service
description: Domain separation is supported in Workforce Optimization for Customer Service. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Domain separation in Workforce Optimization for Customer Service is configured to apply to all features of the application. Separation of data is configured along with separation of logic and process.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Workforce Optimization for Customer Service, Customer Service Management]
---

# Domain separation in Workforce Optimization for Customer Service

Domain separation is supported in Workforce Optimization for Customer Service. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Domain separation in Workforce Optimization for Customer Service is configured to apply to all features of the application. Separation of data is configured along with separation of logic and process.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## How domain separation works in Workforce Optimization for Customer Service

Domain separation in Workforce Optimization for Customer Service does not require any setup or configuration.

## Domain separation for Channel Management in Workforce Optimization for Customer Service

The work items, such as cases, interactions, and their associated actions, appear based on the selected domain. For information on how work assignments are routed based on domain in Channel Management, refer to Domain separation and Advanced Work Assignment

The domain-separated tables for Channel Management are as follows:

-   Service Channel Reports \[m2m\_awa\_service\_channel\_report\]
-   Queue Reports \[m2m\_awa\_queue\_report\]

## Domain separation for Scheduling in Workforce Optimization for Customer Service

When an agent schedule is generated and assigned to an agent, the schedule is only available in the domain that agent belongs to.

The domain-separated tables for Scheduling are as follows:

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

## Domain separation for Teams in Workforce Optimization for Customer Service

The **sn\_wfo\_add\_manager** table is domain separated. When users are added as additional managers, those users can only view users within that domain.

## Domain separation for Skill Recommendation in Workforce Optimization for Customer Service

Domain separated tables for Skill Recommendation

-   sn\_sre\_task\_predicted\_skill
-   sn\_sre\_user\_predicted\_skill

## Domain separation for Coaching in Workforce Optimization for Customer Service

For information on how domain separation works in Coaching for Workforce Optimization for ITSM, refer to Domain separation and Coaching.

**Parent Topic:**[Configuring Workforce Optimization for Customer Service](setup-configurable-wfo-cs.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

