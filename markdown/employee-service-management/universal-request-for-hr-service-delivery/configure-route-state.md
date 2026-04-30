---
title: Transfer configuration
description: You can enable agents to transfer department-specific tickets, such as an incident ticket or an HR case back to the Universal Request \(UR\), to another department, or service. This transfer configuration allows you to determine what happens to the departmental ticket when the request is transferred to another department or back to UR.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Transfer configuration

You can enable agents to transfer department-specific tickets, such as an incident ticket or an HR case back to the Universal Request \(UR\), to another department, or service. This transfer configuration allows you to determine what happens to the departmental ticket when the request is transferred to another department or back to UR.

## Before you begin

Role required: admin

## About this task

The transfer configuration has the following configurations.

-   **Transfer Information**

    Determines the state and template to apply on the department ticket when a department ticket is transferred.

-   **Closure Information**

    Determines the final closure state and template to apply on the department ticket associated with a UR that is closed.


When you transfer a department ticket, you can transfer it with one of the following reasons:

-   **Transfer with resolution**

    When the request is resolved and transferred back to UR, to the specific department, or service.

-   **Transfer without resolution**

    When the request is not resolved or does not belong to the specific department and is transferred back to UR, to the specific department, or service.


For example, if an incident ticket is transferred without resolution, in the **Transfer Information** tab, you can configure the **Transfer state** as `Canceled`. In the **Closure Information** tab, you can configure the closed state of the incident ticket when the UR is closed.

To perform this transfer action, you must configure the transfer configuration details in the Universal Request application.

![Transfer configuration form](../images/ur-route-config.png)

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration** &gt; **Transfer Configuration**.

2.  Open and edit an existing configuration or click **New** for a new configuration record.

3.  On the form, fill in the fields.

    For more information on the field descriptions, see [Transfer configuration form](../reference/ur-route-config-form.md).


**Parent Topic:**[Configuring Universal Request](../concept/configure-ur.md)

