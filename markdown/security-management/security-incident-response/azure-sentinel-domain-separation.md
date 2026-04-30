---
title: Domain separation and Microsoft Azure Sentinel integration
description: Domain separation is supported for this application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Domain separation and Microsoft Azure Sentinel integration

Domain separation is supported for this application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## How domain separation works in the Microsoft Azure Sentinel integration

Follow these steps to achieve domain separation:

-   Create a user with the sn\_si.admin role in the respective domain.

    **Note:** When you create the profile, use the domain picker to select a domain. Do not create the user in the parent domain and later change the domain of the profile. You should have a user for each domain for your profile with the sn\_si.admin role. Use this user to create or modify settings in the profile.

-   Disable existing scheduled jobs.
-   Replicate the following scheduled jobs for every domain:
    -   Azure Sentinel Fetching Alerts &amp; Entities
    -   Azure Sentinel Comments Sync
    -   Azure Sentinel Status Update
    -   Azure Sentinel Profile Process
    -   Azure Sentinel Process Raw Data
    -   Azure Sentinel Data Cleanup
    -   Azure Sentinel Historic Comment Pull
-   Change the **Run as** from the system user to the user with the sn\_si.admin role in the respective domain and then run the scheduled job.

The following example shows how to replicate the Azure Sentinel comments and Status update job and run the job as a system user.

![Replicate Azure Sentinel comments and Status update job and run as system user.](../image/sentinel-domain-sep1.png)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

