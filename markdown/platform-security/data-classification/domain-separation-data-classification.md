---
title: Domain separation and Data Classification
description: Domain separation is supported for Data Classification . Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Data Classification
classification: data-classification
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Classification, Platform Privacy]
---

# Domain separation and Data Classification

Domain separation is supported for Data Classification. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Enhanced

-   Includes all aspects of **Basic** and **Standard** levels of support.
-   Data-driven process enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer cannot affect another.
-   Tenants of the instance must be able to configure minimum viable product \(MVP\) business logic and data parameters for themselves. This logic and parameters would be expected for the application's normal function.

Sample use case: Tenant-customers of a shared environment must be able to modify the impact, urgency, or priority matrix to set priority within their domain.

For more information on support levels, see [Application support for domain separation](../../company-and-domain-separation/reference/domain-separated-apps.md).

## How domain separation works in Data Classification

For domain separation, the application uses process separation for the Data Classification \[sys\_data\_classification\] table. For the Dictionary-Data Class \[m2m\_dictionary\_dataclass\] table, it uses data separation. For learn more about data and process separation, see [Domain separation explained](../../company-and-domain-separation/concept/bp-what-is-domain-separation.md).

**Related topics**  


[Domain separation for service providers](../../company-and-domain-separation/reference/domain-sep-landing-page.md)

