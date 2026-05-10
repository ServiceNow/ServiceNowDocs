---
title: Configure HR Multi Instance Integration for Consumer
description: Plan and implement the configuration of HR Multi Instance Integration for Consumer.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring HR Multi Instance Integration, HR Multi Instance Integration, HR Service Delivery, Employee Service Management]
---

# Configure HR Multi Instance Integration for Consumer

Plan and implement the configuration of HR Multi Instance Integration for Consumer.

## Configuration overview

1.  Activate the HR Multi Instance Integration for Consumer application from ServiceNow Store, which installs the following plugins:
    -   HR Multi Instance Integration Base
    -   Service Bridge for Consumer
    -   Human Resources Scoped App: Core

        **Note:** In addition, you can also install ServiceNow Employee Center to enable employees to raise service requests via catalogs in Employee Center.

2.  Configure HR Multi Instance Integration for Consumer by performing the following steps:
    1.  Register a service bridge provider. For more information, see [Connect to a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-register.md).
    2.  Activate remote record producers that the provider has published for your organization. For more information, see [Activate a remote record producer in Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-activate-entitlements.md).
    3.  Enable remote catalogs under the proper catalog category so that the remote catalogs are accessible to employees in the Employee portal. For more information, see [Associate content from catalog categories to a topic](../../employee-center/task/associate-catalog-categories-to-topics-in-bulk.md).
    4.  Create an HR service that will create a task type of Submit catalog with remote record producer.

