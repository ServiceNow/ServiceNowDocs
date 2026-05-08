---
title: Domain separation and CDM
description: Domain separation is supported for CDM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Domain separation and DevOps Config, DevOps Config reference, DevOps Config, IT Service Management]
---

# Domain separation and CDM

Domain separation is supported for CDM. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Domain separation and CDM overview

Domain separation for CDM means that only a user in the application's domain or parent domain can access the data. All functionality for CDM works in a domain-separated environment as long as all of the following actions are performed by users within that domain:

-   Create application
-   Create/upload config data
-   Commit changeset
-   Create snapshots
-   Validate snapshots
-   Map policies
-   Export snapshots

## How domain separation works in CDM

To set up domain separation for CDM:

1.  Create your domain and then create CDM users in that domain.
2.  Only a specified user \(CDM admin in that domain\) should populate config data in the application's domain.
3.  Only users in the application's domain should upload or create data in the domain.

Follow these guidelines for successful domain separation:

-   Create a separate user for each domain to perform upload, edit, or export of config data.
-   Only users in the application's domain should upload or create data in the domain.
-   Avoid uploading or creating config data for a given application in multiple domains.
-   Policies and exporters must be either in the application's domain or in the global domain.

## Domain-separated tables in CDM

CDM tables include a **Domain** column.

-   sn\_cdm\_application
-   sn\_cdm\_changeset
-   sn\_cdm\_deployable
-   sn\_cdm\_exporter
-   sn\_cdm\_exporter\_execution
-   sn\_cdm\_exporter\_execution\_log
-   sn\_cdm\_exporter\_version
-   sn\_cdm\_exporter\_version\_argument
-   sn\_cdm\_node
-   sn\_cdm\_node\_main
-   sn\_cdm\_pace\_policy\_mapping
-   sn\_cdm\_restricted\_groups
-   sn\_cdm\_snapshot

**Parent Topic:**[Domain separation and DevOps Config](../../devops-config/concept/devops-config-domain-separation.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

