---
title: Domain separation and Asset Management - Procurement Integration
description: Domain separation is supported for Asset Management - Procurement Integration. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating with external procurement applications, Procurement, IT Asset Management]
---

# Domain separation and Asset Management - Procurement Integration

Domain separation is supported for Asset Management - Procurement Integration. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Enhanced

-   Includes **Basic** and **Standard** levels.
-   Data-driven process enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer can’t affect another.
-   Tenants of the instance must be able to configure minimum viable product \(MVP\) business logic and data parameters for themselves. This logic and parameters would be expected for the application's normal function.

Sample use case: Tenant-customers of a shared environment must be able to change the impact, urgency, or priority matrix to set priority within their domain.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Asset Management - Procurement integration overview

Domain separation is present in all aspects of the Asset Management - Procurement Integration application.

## How domain separation works in Asset Management - Procurement Integration

-   You can create multiple procurement integration profiles in each domain. You must have only one published and active profile in each domain, including the parent domain.
-   For the Purchase Order to create a requisition in your external purchasing application, a published procurement integration profile must exist in the domain of the purchase order.
-   All Purchase Orders, Purchase Order Lines, Receiving Slips, Receiving Slip Lines, entitlements, entitlement import errors, and expense line records that you created are stamped with the respective domain of the purchase order.

The Procurement Integration Job \[itam\_procurement\_integration\_job\] table isn't domain separated.

However, each procurement integration job is associated with a procurement integration profile. The job execution only synchronizes the updates from the external purchasing application to the purchase orders that are stamped with the corresponding procurement integration profile.

## Domain separated tables

-   Procurement Integration Profile \[itam\_procurement\_integration\_profile\]
-   Procurement Integration Job Log \[itam\_procurement\_integration\_job\_log\]

## Required plugins

-   Domain separation extension \(com.glide.domain.msp\_extensions.installer\)
-   SAMP \(com.sn\_samp\_master\)
-   Procurement \(com.snc.procurement\)

**Other supported plugins**

Service Catalog – Domain Separation \(com.glideapp.servicecatalog.domain\_separation\)

