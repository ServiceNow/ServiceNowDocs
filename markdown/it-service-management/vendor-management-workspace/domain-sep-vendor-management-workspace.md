---
title: Domain separation and Vendor Management Workspace
description: Domain separation is supported in Vendor Management Workspace. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Vendor Management Workspace, IT Service Management]
---

# Domain separation and Vendor Management Workspace

Domain separation is supported in Vendor Management Workspace. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

The Vendor Management Workspace application uses performance analytics to collect data and provides domain separation support.

## Request Vendor Management Workspace Domain Separation

The Domain Support - Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\) must be activated by ServiceNow personnel. After this plugin has been activated, as an administrator, you can activate the Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) plugin.

The Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) must be activated to enable the features for Vendor Manager Workspace

-   **[Configure domain separation for Vendor Management Workspace](../task/config-domain-sep-vendor-management-configurable-workspace.md)**  
Configure domain separation for Vendor Management Workspace to collect vendor scores and analyze the data for a specific domain. Configure domains for vendor score metric models.

**Parent Topic:**[Vendor Management Workspace reference](../reference/vendor-manager-workspace-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

