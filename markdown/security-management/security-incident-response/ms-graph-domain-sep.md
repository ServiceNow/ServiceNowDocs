---
title: Domain separation and Microsoft Graph Security API alert ingestion
description: Domain separation is supported for this application. The Microsoft Graph Security API integration ingests alerts from Microsoft Graph security providers and automatically creates security incidents. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Domain separation and Microsoft Graph Security API alert ingestion

Domain separation is supported for this application. The Microsoft Graph Security API integration ingests alerts from Microsoft Graph security providers and automatically creates security incidents. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## How domain separation works in the Microsoft Graph Security API

To achieve domain separation, replicate the Microsoft Graph Security API Profile Process and SIR Process Alert Updates scheduled jobs and change the **Run as** users. By default, the system users execute these scheduled jobs. Change the **Run as** to a user with the sn\_si.admin role in the respective domain and run the scheduled job.

![Microsoft Graph Security API: Domain Separation I](../image/ms-graph-domain-sep.png)

![Microsoft Graph Security API: Domain Separation II](../image/ms-graph-domain-sep1.png)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

