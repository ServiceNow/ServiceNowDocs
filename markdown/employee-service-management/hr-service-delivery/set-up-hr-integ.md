---
title: Setting up Enterprise Service Management Integrations Framework
description: Understand how to set up Enterprise Service Management Integrations Framework to use for integration with third-party systems.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Setting up Enterprise Service Management Integrations Framework

Understand how to set up Enterprise Service Management Integrations Framework to use for integration with third-party systems.

## Before you begin

Role required: sn\_hr\_integr\_fw.admin

To set up Enterprise Service Management Integrations Framework, you must first activate the Enterprise Service Management Integrations Framework application from ServiceNow Store. Next, you must [Setting up Enterprise Service Management Integrations Framework](set-up-hr-integ.md).

## Procedure

1.  Create a source record by specifying the third-party application with which you want to integrate your ServiceNow application.

    For more information, refer to [Create a source in Enterprise Service Management Integrations Framework](create-source-hrint.md).

2.  Create an import set table.

3.  Create a flow in Flow Designer.

    For more information, refer to [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    **Note:** The flows or subflows that you are parsing into integration services must follow the input and output structure of Template Integration Service.

4.  Create an integration service to connect with the third-party system.

    For more information, refer to [Create an integration service in Enterprise Service Management Integrations Framework](create-hr-service-hrint.md).

5.  Create transformation maps.

    For more information, see [Create transform maps in Enterprise Service Management Integrations Framework](transform-maps-HR.md).

    **Note:**

    -   You must create transformation maps only for Schedule Pull services, and not for Ondemand Push services.
    -   If you are using Enterprise Service Management Integrations Framework to pull tasks from a third-party system, use the Pull to-do transform map.

