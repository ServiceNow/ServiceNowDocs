---
title: Configure Enterprise Service Management Integrations Framework
description: Understand how to set up Enterprise Service Management Integrations Framework to use for integration with third-party systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/set-up-hr-integ.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure Enterprise Service Management Integrations Framework

Understand how to set up Enterprise Service Management Integrations Framework to use for integration with third-party systems.

## Before you begin

Role required: sn\_hr\_integr\_fw.admin

To set up Enterprise Service Management Integrations Framework, you must first activate the Enterprise Service Management Integrations Framework application from ServiceNow Store. Next, you must [Configure Enterprise Service Management Integrations Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/set-up-hr-integ.md).

## Procedure

1.  Create a source record by specifying the third-party application with which you want to integrate your ServiceNow application.

    For more information, refer to [Create a source in Enterprise Service Management Integrations Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/create-source-hrint.md).

2.  Create an import set table.

3.  Create a flow in Flow Designer.

    For more information, refer to Create a flow.

    **Note:** The flows or subflows that you are parsing into integration services must follow the input and output structure of Template Integration Service.

4.  Create an integration service to connect with the third-party system.

    For more information, refer to [Create an integration service in Enterprise Service Management Integrations Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/create-hr-service-hrint.md).

5.  Create transformation maps.

    For more information, see [Create transform maps in Enterprise Service Management Integrations Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/transform-maps-HR.md).

    **Note:**

    -   You must create transformation maps only for Schedule Pull services, and not for Ondemand Push services.
    -   If you are using Enterprise Service Management Integrations Framework to pull tasks from a third-party system, use the Pull to-do transform map.

