---
title: Domain separation and Hardware Asset Management
description: Domain separation is supported in Hardware Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Domain separation and Hardware Asset Management

Domain separation is supported in Hardware Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Enhanced

-   Includes all aspects of **Basic** and **Standard** levels of support.
-   Data-driven process enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer cannot affect another.
-   Tenants of the instance must be able to configure minimum viable product \(MVP\) business logic and data parameters for themselves. This logic and parameters would be expected for the application's normal function.

Sample use case: Tenant-customers of a shared environment must be able to modify the impact, urgency, or priority matrix to set priority within their domain.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Domain separation overview

Domain separation support in the product enables service providers to offer managed services for software and hardware asset management to their customers. This feature also caters to large organizations who manage their subsidiaries as independent domains.

## How domain separation works in Hardware Asset Management

In HAM, domain separation occurs in two stages: data separation and process separation. There are no system properties specific to Hardware Asset Management that can be used to enable or disable the separation. However, the Domain Asset Process Settings table \(alm\_domain\_asset\_process\_setting\) stores configurations for asset processes, including the normalization of hardware models. By default, normalization is performed only for models within the TOP/Default domain. However, if you have the asset or domain\_admin role, you can enable normalization for hardware models in any domain. To enable normalization for a specific domain, follow these steps:

1.  Navigate to the Domain Asset Process Settings table \(alm\_domain\_asset\_process\_setting\).
2.  Locate the specific domain for which you want to enable normalization of models.
3.  Set the **Run asset process** field to **true**.

**Note:**

The [Recommended practice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md) is to avoid customizing the base system domain configuration record.

## Required plugins

-   Service Catalog – Domain Separation \(com.glideapp.servicecatalog.domain\_separation\)
-   Domain separation extension \(com.glide.domain.msp\_extensions.installer\)
-   Performance Analytics – Domain Support \(com.snc.pa.domain\_support\)
-   HAMP \(store app\)

To learn more, see [Domain separation explained](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-what-is-domain-separation.md), [Contains queries and domain access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-contains-domain-visibility.md), and [Importance of Default domain](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-default-domain.md).

**Parent Topic:**[Hardware Asset Management reference](reference-hardware-asset-management.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

