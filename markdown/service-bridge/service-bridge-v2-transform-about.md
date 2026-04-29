---
title: Transform data with the Service Exchange transform framework
description: Use the Transform Framework to integrate tasks between two ServiceNow instances to transform remote task data in the Service Exchange application.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Remote tasks, Explore, Service Exchange]
---

# Transform data with the Service Exchange transform framework

Use the Transform Framework to integrate tasks between two ServiceNow instances to transform remote task data in the Service Exchange application.

As a provider, you can use the Transform Framework to transform your inbound and outbound data \(such as incidents, cases, and service requests\) of the remote tasks between your ServiceNow instance and your consumer's instance. To learn what a remote task is, see [Remote tasks](service-bridge-v2-remote-task-overview.md).

While using the Service Exchange for Providers application, you and your consumer can exchange the remote task data through tables and fields. The Transform Framework helps you to convert the data between those tables and fields so that you and your consumer can easily communicate with each other while resolving the incidents, cases, and consumer requests. Transforms can be created once and used across all remote task definitions.

You can use the following transform types in the Transform Framework for your remote tasks:

-   **Simple**: Select the simple transform option to use the predefined values of the inbound and outbound fields for your remote tasks. For example, by using this transform type, you’re converting the Open state of an incident in the provider's ServiceNow® instance to the In Progress state in the consumer's ServiceNow instance.
-   **Advanced**: Use an advanced transform where you run a script to determine the inbound and outbound data values for your remote tasks. For example, use this transform type to convert an incoming sys\_id into a correlated sys\_id for a reference field.
-   **Virtual Inbound**: Use this to transform or set a value for an Inbound Virtual field. This option uses a script to transform the data and adds a mandatory Inbound Field field.
-   **Virtual Outbound**: Use this to transform or set a value for an Outbound Virtual field. This option uses a script to transform the data and adds a mandatory Outbound Field field.
-   **Global**: Use the global transform option to create a default transform definition that can be applied to all consumer accounts.

    **Note:** A matching company or account specific transform overrides the Global transform option.


To learn how to create a transform, see [Create a transform in Service Exchange](../task/service-bridge-v2-create-transform.md).

