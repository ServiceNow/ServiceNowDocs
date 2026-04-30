---
title: Create a Workplace service
description: Create a workplace service with pre-defined steps of fulfillment. Select the fulfillment type required based on the workplace service. Create workplace services like catering, office supply request, parking, or any service to support employees needs.
locale: en-US
release: xanadu
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure Workplace Case Management, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
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

-   **[Create a Workplace service activity](create-workplace-service-activity.md)**  
Create a Workplace service activity to trigger a background activity when a Workplace service is selected. The activity can be an approval action, task, or a child case.

**Parent Topic:**[Configure Workplace Case Management](../concept/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](install-workplace-case-mgmt.md)

[Create a Workplace case template](wsd-case-template.md)

[Create a Workplace task template](wsd-task-template.md)

[Configure Approval options](config-approval-optns.md)

[Configure a Record producer](wsd-create-record-producer.md)

[Configuring a record producer for request edit](../concept/config-case-edit-rp.md)

[Configuring a record producer for reservation](../concept/config-reservation-rp.md)

[Configure workplace services topic](configure-workplace-services.md)

[Create an SLA Definition](create-sla-defn-case-mgmt.md)

[Add a workplace service item to a workplace service](add-workplace-service-items.md)

[Create a workplace template configuration](create-workplace-template-confguration.md)

[Create a workplace field mapping](create-workplace-field-mapping.md)

[Configure an escalation rule](configure-escalation-rule.md)

[Add Fulfillment instructions](add-fulfillment-instructions.md)

[Group similar workplace cases under a parent case](group-similar-workplace-cases.md)

