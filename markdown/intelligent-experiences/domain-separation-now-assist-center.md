---
title: Domain separation and Now Assist Center
description: Domain separation is supported for Now Assist Center.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Reference, Now Assist Center, Enable AI experiences]
---

# Domain separation and Now Assist Center

Domain separation is supported for Now Assist Center.

Domain separation allows you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level: Basic

-   Business logic: Ensure data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all use domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Domain separation uses in Now Assist Center

-   The system supports domain separation for skills and instructions.
-   Ability to view domain-based skills in the actionable use cases on the home page.
-   Ability to duplicate skills for different domains.
-   Now Assist Center analytics data contains records from multiple domains.

## Tables

The following Now Assist Center tables contain domain-separated fields:

-   nac\_promoted\_skill
-   nac\_promoted\_skill\_state

## Fields

The following domain-separated fields are supported:

-   sys\_domain

    Associates the state record with a specific domain.

-   sys\_domain\_path

    Manages domain hierarchy relationships.

-   sys\_overrides

    Enables child domain state records to override parent domain states.


**Parent Topic:**[Now Assist Center reference](now-assist-center-reference.md)

**Related topics**  


[Components installed with Now Assist Center](components-installed-with-now-assist-center.md)

[Now Assist Center glossary](../concept/now-assist-center-glossary.md#)

[Now Assist Center roles](now-assist-center-roles.md#)

