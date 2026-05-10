---
title: Domain separation and IBM QRadar Offense Ingestion
description: Domain separation is supported in IBM QRadar offense ingestion. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Domain separation and IBM QRadar Offense Ingestion

Domain separation is supported in IBM QRadar offense ingestion. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## How domain separation works in IBM QRadar Offense Ingestion

Follow these steps to achieve domain separation:

-   Create a user with the `sn_si.admin` role in the respective domain.

    **Note:** When you create the profile, use the domain picker to select the specific domain. Do not create the user in the parent domain and later change the domain of the profile. You should have a specific user for each domain for your profile with the `sn_si.admin` role. Use this user to create or modify settings in the profile.

-   Disable existing scheduled jobs.
-   Replicate the IBM QRadar Process Polling Queue, the IBM QRadar Process Profiles, and the Offense Updates scheduled jobs for every domain.
-   Change the **Run as** from the system user to the user with the `sn_si.admin` role in the respective domain and run the scheduled job.

![IBM QRadar Process Polling Queue job](../image/ibm-qradar-domain-sep1.png)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

