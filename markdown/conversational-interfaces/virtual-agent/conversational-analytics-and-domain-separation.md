---
title: Domain separation and Conversational Analytics
description: In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported in Conversational Analytics dashboard. Domain separation enables you to separate data into logical groupings called domains. You can control several aspects of this application, including which users can see and access data.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-11-03"
reading_time_minutes: 2
breadcrumb: [Conversational Analytics dashboard reference, Conversational Analytics dashboard, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# Domain separation and Conversational Analytics

Domain separation is supported in Conversational Analytics dashboard. Domain separation enables you to separate data into logical groupings called domains. You can control several aspects of this application, including which users can see and access data.

## Support level: Basic\*

The support level is Basic but has some exceptions or special conditions.

-   Business logic: Ensure that data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   The user interface, cache keys, reporting, rollups, and aggregations all use the domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Required approach to domain separation

Currently, only Global approach is supported to domain separation in Conversational Analytics dashboard. To learn more, see [Domain separation and Performance Analytics](https://www.servicenow.com/docs/access?context=c_PAWithDomainSeparation&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## Overview of domain separation

Conversational Analytics dashboard is built on the Platform Analytics experience. See [Domain separation for Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=domain-sep-pa-dashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

## How domain separation works in Conversational Analytics

With domain separation in Conversational Analytics, users in one domain cannot access data or functionality that belongs to another domain. Additionally, administrators who are assigned to a domain cannot see or manage Conversational Analytics dashboard in other domains, ensuring complete separation and security.

**Note:** If you override a formula in any domain, the system applies that updated formula to all other domains.

## Requirements

All domain support features require the Domain Support - Domain Extensions Installer \[com.glide.domain.msp\_extensions.installer\] plugin. For details, see [Request domain separation](https://www.servicenow.com/docs/access?context=t_ActivateDomainSeparation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Use cases

If you are a service provider that hosts multiple clients in the same instance, you can set up domain separation to separate tenant data. Administrative tasks and process separation are currently not supported.

**Parent Topic:**[Conversational Analytics dashboard reference](conversational-analytics-dashboard-reference-pae.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

