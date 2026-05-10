---
title: Configure all catalog items or record producers to create a universal request
description: Reduce the implementation time by configuring all catalog items or all record producers at a time for universal request creation.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Catalog configuration for Universal Request, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure all catalog items or record producers to create a universal request

Reduce the implementation time by configuring all catalog items or all record producers at a time for universal request creation.

## Before you begin

Role required: admin

## About this task

For catalog items, RITM should be registered as a service in Universal Request.

For record producers, the target table should be registered as a service in Universal Request.

For information about service configurations, see [Service Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-request-for-hr-service-delivery/ur-service-config-form.md).

## Procedure

1.  Navigate to sys\_properties.list.

2.  Click **New**.

3.  To configure all catalog items to create a universal request:

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique identifier of the property. Specify**sn\_uni\_req.enable\_ur\_all\_cat\_items**.|
        |Type|Type of the property. Specify **boolean**.|
        |Value|Option to specify if all catalog items can be configured at a time to create a universal request. Possible values are **true** or **false**.|

    2.  Click **Submit**.

4.  To configure all record producers to create a universal request:

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique identifier of the property. Specify**sn\_uni\_req.enable\_ur\_all\_rec\_prod\_items**.|
        |Type|Type of the property. Specify **boolean**.|
        |Value|Option to specify if all record producers can be configured at a time to create a universal request. Possible values are **true** or **false**.|

    2.  Click **Submit**.


**Parent Topic:**[Service Catalog configuration for Universal Request](../concept/ur-catalog-config.md)

