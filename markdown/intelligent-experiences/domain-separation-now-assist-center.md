---
title: Domain separation and AI Admin Center
description: Domain separation is supported for AI Admin Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/domain-separation-now-assist-center.html
release: australia
topic_type: reference
last_updated: "2026-07-30"
reading_time_minutes: 1
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Reference, AI Admin Center, Enable AI experiences]
---

# Domain separation and AI Admin Center

Domain separation is supported for AI Admin Center.

Domain separation allows you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Business logic: Ensure data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all use domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Domain separation uses in AI Admin Center

-   The system supports domain separation for skills and instructions.
-   Ability to view domain-based skills in the actionable use cases on the home page.
-   Ability to duplicate skills for different domains.
-   AI Admin Center analytics data contains records from multiple domains.

## Tables

The following AI Admin Center tables contain domain-separated fields:

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


**Parent Topic:**[AI Admin Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-reference.md)

**Related topics**  


[Components installed with AI Admin Center]()

[AI Admin Center glossary]()

[AI Admin Center roles]()

