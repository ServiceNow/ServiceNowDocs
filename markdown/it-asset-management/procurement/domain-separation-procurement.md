---
title: Domain separation and Procurement
description: Domain separation is supported in Procurement processing. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Procurement, IT Asset Management]
---

# Domain separation and Procurement

Domain separation is supported in Procurement processing. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

The support level is Standard but has some exceptions or special conditions.

-   Includes all aspects of **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must be able to configure minimum viable product \(MVP\) business logic and data parameters. This configuration is done per tenant, as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## How domain separation works in Procurement

To create or edit Purchase Orders \(POs\) or PO line items that distinguish the domain, customers must be working in the proper domain. When adjusting any configuration, you should be in the domain where you're doing the work. Use the domain picker to choose the correct domain to work in.

**Parent Topic:**[Procurement](c_Procurement.md)

**Related topics**  


[Procurement roles](../reference/r_ProcurementRoles.md)

[Procurement workflows](c_ProcurementWorkflows.md)

[Use the Procurement Overview module](../task/t_UsingTheProcurementOverviewModule.md)

[Activate Procurement](../task/t_ActivateProcurement.md)

[Sourcing items in a service catalog request](c_SourcingRequestItems.md)

[Procurement purchase order management for assets](c_UseProcurement.md)

[Receive assets](c_ReceiveAssets.md)

[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

