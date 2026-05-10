---
title: Domain separation and Automation Center
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Automation Center. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Automation Center, Workflow Data Fabric]
---

# Domain separation and Automation Center

Domain separation is supported for Automation Center. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview of domain separation in Automation Center

The goal of Automation Center is to govern the end-to-end multi-vendor life cycle from one place. Domain separation is enabled in all the features.

You should have either a flat hierarchy or a single-tier hierarchy and at least one primary or top-level domain.

To support domain separation for particular widgets in Automation Center, you must install and configure com.snc.pa.domain\_support.

**Note:** Action Center and Connection Manager encounter challenges due to process separation in flows. In Action Center, the domain data from both global and current session domains is displayed. In Connection Manager, only current session's domain data is displayed.

**Parent Topic:**[Automation Center reference](automation-center-reference.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

