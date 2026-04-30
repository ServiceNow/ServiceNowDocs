---
title: Domain separation and Digital Portfolio Management
description: Domain separation is supported in Digital Portfolio Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Digital Portfolio Management reference, Digital Portfolio Management, IT Service Management]
---

# Domain separation and Digital Portfolio Management

Domain separation is supported in Digital Portfolio Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level Standard

-   Includes Basic level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

The Digital Portfolio Management application uses Performance Analytics to collect data and provides domain separation support.

## Request Digital Portfolio Management Domain Separation

The Domain Support - Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\) must be activated by ServiceNow personnel. After this plugin has been activated, as an administrator, you can activate the Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\).

The Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) must be activated to enable the features for Digital Portfolio Management.

**Parent Topic:**[Digital Portfolio Management reference](../reference/dpm-reference-cfw.md)

