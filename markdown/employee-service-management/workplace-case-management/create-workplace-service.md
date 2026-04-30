---
title: Create a Workplace service
description: Create a workplace service with pre-defined steps of fulfillment. Select the fulfillment type required based on the workplace service. Create workplace services like catering, office supply request, parking, or any service to support employees needs.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a Workplace service

Create a workplace service with pre-defined steps of fulfillment. Select the fulfillment type required based on the workplace service. Create workplace services like catering, office supply request, parking, or any service to support employees needs.

## Before you begin

Ensure that you have the following details:

-   Task templates and Case templates to link it to the workplace service.
-   Record producer to which the workplace service must be linked.
-   Active flows in case you want to create workplace service flow.

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

Create a workplace service and specify how the workplace service must be fulfilled. You can choose to fulfill the workplace service manually, by triggering a series of tasks i.e by a service activity or using a flow. Specify the following for the workplace service:

-   Name of the workplace service. The workplace service will be displayed at all location with this name.
-   The fulfillment type like manual, service activity or flow.
-   Specify from where you want to enable users to order. That is, specify if users can order through a workplace service request or while making a reservation or both.
-   Specify if an employee can request more than one workplace item that belongs to the same category.
-   Select a template to pre-fill certain values when creating a workplace case or a workplace task.
-   The record producer to which you want to link the workplace service if you want to make it available. The workplace service can be requested only through a record producer created in the Workplace Case Management application.
-   Description about the workplace. You can enter a brief description about the purpose of workplace service. You can enter a regular text or a HTML text.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Select **New**.

3.  On the Workplace service form, fill in the fields.

    For a description of the field values, see [Workplace Service form](../reference/workplace-service-form.md).

4.  Select **Submit**.


## Result

The workplace service is created and is requested whenever the associated record producer is selected. If you want to create a workplace service activity for the workplace service, refer to [Create a Workplace service activity](create-workplace-service-activity.md).

