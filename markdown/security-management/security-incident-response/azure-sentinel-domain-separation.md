---
title: Domain separation
description: Domain separation is supported for this application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/security-incident-response/azure-sentinel-domain-separation.html
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Domain separation

Domain separation is supported for this application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-security/servicenow-ai-platform-security/domain-separated-apps.md).

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

\[Omitted image "sentinel-domain-sep1.png"\] Alt text: Replicate Azure Sentinel comments and Status update job and run as system user.

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-security/servicenow-ai-platform-security/domain-sep-landing-page.md)

