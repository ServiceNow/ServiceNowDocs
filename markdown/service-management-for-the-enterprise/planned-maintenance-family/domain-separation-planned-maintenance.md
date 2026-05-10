---
title: Domain separation and Planned Maintenance
description: Domain separation is supported in Planned Maintenance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Planned Maintenance, Service Management]
---

# Domain separation and Planned Maintenance

Domain separation is supported in Planned Maintenance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

The support level is Standard but has some exceptions or special conditions.

-   Includes all aspects of **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must be able to configure minimum viable product \(MVP\) business logic and data parameters. This configuration is done per tenant, as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## How domain separation works in Planned Maintenance

There is no sys\_domain column in the Maintenance Plan \(sm\_maint\_plan\) table. The application cannot be exposed to customer fulfillers; however, the table is condition-based so there is some limited support.

You can set maintenance plans to include or exclude domains or set them globally by design. Support in the Part Requirements \(sm\_part\_requirement\} table is data only.

**Parent Topic:**[Planned Maintenance](c_SMPlanMaint.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

