---
title: Domain separation and Software Asset Management
description: Domain separation is supported in Software Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Domain separation and Software Asset Management

Domain separation is supported in Software Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Enhanced

-   Includes all aspects of **Basic** and **Standard** levels of support.
-   Data-driven process enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer cannot affect another.
-   Tenants of the instance must be able to configure minimum viable product \(MVP\) business logic and data parameters for themselves. This logic and parameters would be expected for the application's normal function.

Sample use case: Tenant-customers of a shared environment must be able to modify the impact, urgency, or priority matrix to set priority within their domain.

For more information on support levels, see Application support for domain separation.

## Overview

Domain separation support in the product enables service providers to offer managed services for software and hardware asset management to their customers. This feature also caters to large organizations who manage their subsidiaries as independent domains.

## How domain separation works in Software Asset Management

In SAM, domain separation occurs in two stages: data separation and process separation. From the Paris release, both data and process are domain-separated.

Any user with sam\_integrator role has access to create and modify the SaaS integration profiles. Since users with this role can also access the Oauth application registry \(currently not domain-separated, so records across all domains are visible\), this sam\_integrator role should be assigned with caution. The user should be in the service provider organization and satisfy high permissions criteria.

To view logs for domain separation, you need to create a system property titled **asset.log\_level** and set its value to **debug**, **trace** or **info**. Based on the value that you set, logs are shown when any scheduled job that extends the AssetManagementBaseJobscheduled job runs.

In a domain-separated instance, the content data service \(CDS\) should populate data in the instance with domain set as **global**.

**Note:**

The Recommended practice is to avoid customizing the base system domain configuration record.

## Required plugins

-   Domain separation extension \(com.glide.domain.msp\_extensions.installer\)
-   Performance Analytics – Domain Support \(com.snc.pa.domain\_support\)
-   SAMP \(com.sn\_samp\_master\)
-   HAMP \(store app\)

## Other supported plugins

-   Service Catalog – Domain Separation \(com.glideapp.servicecatalog.domain\_separation\)
-   Procurement \(com.snc.procurement\)
-   Cost Management \(com.snc.cost\_management\)
-   Contract Management \(com.snc.contract\_management\)

To learn more, see Domain separation explained, Contains queries and domain access, and Importance of Default domain.

-   **[Domain separation and lifecycle reports](domain-sep-sam-lifecycle.md)**  
There are certain domain separation aspects to consider when running software lifecycle reports.

**Parent Topic:**[Software Asset Management references](../reference/references.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

