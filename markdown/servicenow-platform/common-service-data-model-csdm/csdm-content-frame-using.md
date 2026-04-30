---
title: Managing the CSDM framework
description: The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Managing the CSDM framework

The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.

## CSDM modules

Navigate to the modules that assist you in implementing and managing the CSDM domains and their components.

![Navigating to CSDM modules.](../image/nav-pane.png)

-   **CSDM Data Foundations Dashboard**

    The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products. See [CSDM Data Foundations dashboard](csdm-data-foundations-dashboard.md).

-   **Getting Started**

    Select **Getting Started** to open the library of CSDM user documentation — the documentation you are viewing now.

-   **Service Instance Settings**

    Use the Service Instance Settings module to specify the attributes and relationships that are required when a user creates a service instance. See [Specifying attributes and relationships for service instances](csdm-module-app-service-settings.md).

    See [Monitor the health of application services on the Application Services dashboard](../../configuration-management/task/app-service-dashboard.md).

-   **Service instances Dashboard**

    The Service Instances dashboard \(formerly Application Services\) enables you to monitor and manage service instances to ensure that they are fully configured and are populated in the CMDB. See [Monitoring and managing service instances](csdm-module-app-service-dashboard.md).

-   **Life Cycle Mapping**

    Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(**life cycle stage** and **life cycle stage status**\). You map both asset and CI legacy status values to life-cycle value pairs. See [Enabling CSDM life-cycle sync between legacy fields and related assets](../../configuration-management/concept/csdm-life-cycle-standard-values.md#).

-   **Design**

    Work in the tables that are referenced in the Design domain of the CSDM. See [Design domain in the CSDM framework](design-domain.md).

-   **Manage Technology Management Services**

    Work in the tables that are referenced in the Manage Technology Management Services domain of the CSDM. See [Manage Technology Management Services domain in the CSDM framework](manage-tech-servs-domain.md).

-   **Sell and Consume**

    Work in the tables that are referenced in the Sell/Consume domain of the CSDM. See [Sell/Consume domain in the CSDM framework](sell-consume-domain.md).


## Synchronize data for 'Managed by' and 'Change' groups

[Synchronizing group assignment attributes](csdm-data-synchronize.md)

[Set the group for a CI or an entire class of CIs](../task/csdm-data-synchronize-enable.md)

[Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md)

-   **[CSDM Data Foundations dashboard](csdm-data-foundations-dashboard.md)**  
The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products.
-   **[Specifying attributes and relationships for service instances](csdm-module-app-service-settings.md)**  
Use the Service Instance Settings module to specify the attributes and relationships that are required when a user creates a service instance.
-   **[Monitoring and managing service instances](csdm-module-app-service-dashboard.md)**  
The Service Instances dashboard \(formerly Application Services\) enables you to monitor and manage service instances to ensure that they are fully configured and are populated in the CMDB.
-   **[Matching the usage of dynamic CI groups to service type](csdm-dynamic-ci-groups-by-service.md)**  
The type of service determines how you use dynamic CI groups.

**Parent Topic:**[Common Service Data Model](csdm-landing-page.md)

