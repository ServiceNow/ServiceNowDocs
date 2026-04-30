---
title: Managing the CSDM framework
description: The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Managing the CSDM framework

The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

## CSDM modules

Navigate to the modules that assist you in implementing and managing the CSDM domains and their components.

![Navigating to CSDM modules.](../image/nav-pane.png)

-   **CSDM Data Foundations Dashboard**

    The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products. See [CSDM Data Foundations dashboard](csdm-data-foundations-dashboard.md).

-   **Getting Started**

    Select **Getting Started** to open the library of CSDM user documentation — the documentation you are viewing now.

-   **Application Service Settings**

    Use the Application Service Settings module to specify the attributes and relationships that are required when a user creates an application service. See [Specifying attributes and relationships for Application Services](csdm-module-app-service-settings.md).

    See [Monitor the health of application services on the Application Services dashboard](../../configuration-management/task/app-service-dashboard.md).

-   **Application Services Dashboard**

    The Application services dashboard enables you to monitor and manage application services to ensure that application services are fully configured and are populated in the CMDB. See [Monitoring and managing application services](csdm-module-app-service-dashboard.md).

-   **Life Cycle Mapping**

    Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(**life cycle stage** and **life cycle stage status**\). You map both asset and CI legacy status values to life-cycle value pairs. See [Enabling CSDM life-cycle sync between legacy fields and related assets](../../configuration-management/concept/csdm-life-cycle-standard-values.md#).

-   **Design**

    Work in the tables that are referenced in the Design domain of the CSDM. See [Design domain of the CSDM framework](design-domain.md).

-   **Manage Technical Services**

    Work in the tables that are referenced in the Manage Technical Services domain of the CSDM. See [Manage Technical Services domain of the CSDM framework](manage-tech-servs-domain.md).

-   **Sell and Consume**

    Work in the tables that are referenced in the Sell/Consume domain of the CSDM. See [Sell/Consume domain of the CSDM framework](sell-consume-domain.md).


## Synchronize data for 'Managed by' and 'Change' groups

[Synchronizing group assignment attributes](csdm-data-synchronize.md)

[Set the group for a CI or an entire class of CIs](../task/csdm-data-synchronize-enable.md)

[Synchronize data using a technical service offering](../task/csdm-enable-tso.md)

-   **[CSDM Data Foundations dashboard](csdm-data-foundations-dashboard.md)**  
The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products.
-   **[Specifying attributes and relationships for Application Services](csdm-module-app-service-settings.md)**  
Use the Application Service Settings module to specify the attributes and relationships that are required when a user creates an application service.
-   **[Monitoring and managing application services](csdm-module-app-service-dashboard.md)**  
The Application services dashboard enables you to monitor and manage application services to ensure that application services are fully configured and are populated in the CMDB.
-   **[Synchronizing group assignment attributes](csdm-data-synchronize.md)**  
To empower a particular user group to manage a collection of CIs or CI classes, set group assignment attributes through the technical service offering or the CI Class Manager. The operation synchronizes the group attribute data across all CIs that belong to the specified CI class or groups of CIs.

**Parent Topic:**[Common Service Data Model](csdm-landing-page.md)

