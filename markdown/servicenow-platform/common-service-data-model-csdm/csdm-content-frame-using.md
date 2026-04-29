---
title: Access CSDM features
description: The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB help to promote that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Access CSDM features

The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB help to promote that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

## CSDM modules

Navigate to the modules that assist you in implementing and managing the CSDM domains and their components.

![Navigating to CSDM modules.](../image/csdm-nav-pane-v5.png)

-   **CSDM Data Foundations Dashboard**

    The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products. See [CSDM Data Foundations dashboard](csdm-data-foundations-dashboard.md).

-   **Getting Started**

    Select **Getting Started** to open the library of CSDM user documentation — the documentation you're viewing now.

-   **Service Instance Settings**

    Use the Service Instance Settings module to specify the attributes and relationships that are required when a user creates a service instance. For more information, see [Modify the attributes and relationships required for application services](../../configuration-management/task/modify-req-fields-appservice.md).

    See [Use Service instance \(Application Services\) dashboard to monitor health](../../configuration-management/task/app-service-dashboard.md).

-   **Service instances Dashboard**

    The Service instance dashboard enables you to monitor and manage service instances \(service instances were formerly called application services\) to confirm that they are fully configured and are populated in the CMDB. See [Monitoring and managing service instance settings](csdm-module-app-service-dashboard.md).

-   **Life Cycle Mapping**

    Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(**life cycle stage** and **life cycle stage status**\). You map both asset and CI legacy status values to life-cycle value pairs. See [Enabling life-cycle synchronization from legacy to asset](../../configuration-management/concept/csdm-life-cycle-standard-values.md#).

-   **Design**

    Work in the tables that are referenced in the Design &amp; Planning domain of the CSDM. See [Design &amp; Planning domain in the CSDM model](design-domain.md).

-   **Service Delivery**

    Work in the tables that are referenced in the Service Delivery domain of the CSDM. See [Service Delivery domain in the CSDM model](manage-tech-servs-domain.md).

-   **Sell and Consume**

    Work in the tables that are referenced in the Service Consumption domain of the CSDM. See [Service Consumption domain in the CSDM model](sell-consume-domain.md).


## Synchronize data for 'Managed by' and 'Change' groups

[Synchronizing group assignment attributes](csdm-data-synchronize.md)

[Set the group for a CI or an entire class of CIs](../task/csdm-data-synchronize-enable.md)

[Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md)

-   **[CSDM Data Foundations dashboard](csdm-data-foundations-dashboard.md)**  
The CSDM Data Foundations dashboard displays key CSDM indicators on a single page to help you get the full benefit from your ServiceNow AI Platform products.
-   **[Monitoring and managing service instance settings](csdm-module-app-service-dashboard.md)**  
The Service instance dashboard enables you to monitor and manage service instances \(service instances were formerly called application services\) to confirm that they are fully configured and are populated in the CMDB.

**Parent Topic:**[Common Service Data Model](csdm-landing-page.md)

