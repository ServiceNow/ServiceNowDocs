---
title: AWS events-driven discovery
description: The Amazon Web Services \(AWS\) Config service can raise events for any changes in the life-cycle state or the configuration of a cloud resource. The ServiceNow event-driven discovery uses the events to auto-update the latest resource information in the Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# AWS events-driven discovery

The Amazon Web Services \(AWS\) Config service can raise events for any changes in the life-cycle state or the configuration of a cloud resource. The ServiceNow® event-driven discovery uses the events to auto-update the latest resource information in the Configuration Management Database \(CMDB\).

![Overview of the AWS events-driven discovery](../image/aws-events-driven-discovery.png "Overview of the AWS events-driven discovery")

Configure the AWS Config service to send Simple Notification Service \(SNS\) notifications to the ServiceNow instance. For more information, see [Configure the AWS Config service to send event notifications to the ServiceNow instance](../task/aws-config-service-cloud-mgt.md). After you configure the service, it starts sending event notifications to the ServiceNow Cloud Events REST API. When an event meets any one of the following criteria, the API writes it to the Cloud Events \[sn\_cmp\_cloud\_event\] table:

-   The **Type** of the event is **SubscriptionConfirmation**.
-   The **Type** of the event is **Notification** and **messageType** is **ConfigurationItemChangeNotification**.
-   Amazon CloudWatch has raised the event for a change in the tag associated with the Configuration Item \(CI\).

The Cloud Event Scheduler then picks the events in the Ready state for batch processing. During event processing, the event-driven discovery uses response mappings or patterns to update the details of the affected resource in the CMDB. The **sn\_cmp.cloud\_event.use\_response\_mapping\_aws** property determines the CMDB update method. To understand the status of an event, review its state in the Cloud Events \[sn\_cmp\_cloud\_event\] table.

Starting with the Yokohama release, the **sn\_cmp.cloud\_event.use\_response\_mapping\_aws** property is set to True by default. When this property is set to True, and suitable response mappings are available, the event-driven discovery uses the response mappings to create or update the CI in the CMDB. Otherwise, the event-driven discovery triggers the appropriate patterns to discover the affected resource and create or update the CI in the CMDB.

Starting with the Yokohama release, use the **sn\_cmp.cloud\_event.parallel\_scheduler\_count** property to scale the Cloud Event Scheduler per the event inflow rate. Running multiple cloud event schedulers in parallel helps to improve the event processing rate of the instance. For more information on scaling the Cloud Event Schedulers, see [Scale the AWS cloud event schedulers](../task/scale-aws-cloud-event-schedulers.md).

During event processing, the Cloud Event Scheduler identifies the domain of the service account and assigns to the event. If an error occurs in identifying the domain before processing, the event can sometimes stay unassigned and become visible to all domains. To prevent the failed events visibility to all domains, you can set the **sn\_cmp.error\_events.default\_domain** property to sys\_id of the service-provider domain so that the failed events appears only to the service-provider domain administrator.

