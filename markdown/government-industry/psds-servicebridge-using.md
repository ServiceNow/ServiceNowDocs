---
title: Using Service Exchange for Public Sector Digital Services
description: As a government service agency provider, learn how to use Service Bridge to receive and fulfill service requests from the service catalog from your provider instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, Public Sector Digital Services \(PSDS\)]
---

# Using Service Exchange for Public Sector Digital Services

As a government service agency provider, learn how to use Service Bridge to receive and fulfill service requests from the service catalog from your provider instance.

As an agency provider, you can author and publish remote catalogs from your instance for consumers to generate service requests that can be fulfilled in your instance. You can also integrate your tasks with your consumer's tasks, sending them back and forth for fulfillment, as well as send cases to your consumer's instance via Provider Task.

Service Bridge service requests are initiated from the constituent's ServiceNow instance, viewed through the Government Service Portal. The agency provider's agent fulfills these requests in their ServiceNow agency provider instance. The data in the request then synchronizes the agent and customer instances so that they both can track its progress.

## Using Service Exchange for consumers

As a constituent using a Service Exchange for consumers instance, you can:

-   Review remote catalog items entitled to you from your local catalog and send requests to your agency provider for fulfillment.
-   Bidirectionally integrate your tasks with your agency provider's tasks.
-   Receive proactive tasks from providers for transparency and collaboration.

## Using Service Exchange for providers

As a provider, learn how to use Service Exchange to fulfill requests from the service catalog, and track order fulfillment from your agency provider instance.

As a provider, you can:

-   Author and publish remote service catalogs for your consumers on their instances.
-   Integrate your instance with your consumer's instance.
-   Receive and fulfill service requests on your instance from your constituent's ServiceNow instance.

As a provider, you must first create and publish the remote service catalog and remote task definitions that your constituents can use for creating a remote task. You entitle these definitions to your constituents, who can adjust the mappings and field data rules, or simply activate the definition. Your constituents can apply a trigger on the definition or manually create a remote task for you, the provider, based on an active definition.

Remote Catalog items are ordered from the consumer instance, and create provider tasks in both the provider and consumer instance. The provider agent fulfills these provider tasks in their ServiceNow instance. The data in these tasks is synchronized between instances so that they both can track the progress.

The process for agency providers to create a remote catalog is as follows:

1.  Create a remote record producer in a remote catalog. For information on how to do this, see [Create a remote record producers in a remote catalog in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-remote-rec-prod&version=australia&pubname=australia-service-exchange&ft:locale=en-US).
2.  Create variables for remote record producers. For information on how to do this, [Create variables for remote record producers in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-assign-variables-ser-defn&version=australia&pubname=australia-service-exchange&ft:locale=en-US).
3.  Associate flows to the record producers.

Remote tasks enable you to assign and synchronize the task's data on separate instances so that you can quickly fulfill the service requests from your constituents. Some examples of the consumer requests are as follows:

1.  Request help for issues that your constituents are having.​
2.  Request to assign the existing tasks to you so that you can support your constituent's issues​.

For information on how to create a remote task definition that triggers the assignment of a remote task, see [Create a remote task definition in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-remote-tasks-defs&version=australia&pubname=australia-service-exchange&ft:locale=en-US).

## Service Exchange request fulfillment process

1.  The constituent selects a Service Bridge related item from the service catalog.
2.  The consumer provides the information in the Service Exchange request form and selects **Submit**. When the consumer places the request, the Task View appears on the portal. Within the view, the constituent can add comments that are replicated in the agency provider's instance.
3.  In the constituent's instance, a single tracking task type, the Provider Task, is generated, regardless of the service.
4.  The Provider Task is replicated on the agency provider's instance, triggering a flow that triggers the parent task.
5.  The state of the task in the constituent's instance is set to **Received**.
6.  In the agency provider's instance, an agent takes ownership of the parent task by selecting **Assign to me**.
7.  After an agent takes ownership of the task, the state of the Provider Task in the constituent's instance is updated to **Work in Progress**. When the agent posts a comment on the agency provider's instance, the comment is replicated in the constituent's instance. Comments that the constituent posts are replicated in the provider's instance.
8.  After the agent resolves the request, sets a resolution code, and selects **Propose solution**, the state of the Provider Task in the consumer's instance is updated to **Resolved**. The Actions menu displays the following options, Accept, Reject, or Cancel.
9.  If the consumer accepts the resolution, the state of the provider task on the constituent's instance, and the state of the request on the agency provider's instance, are both updated to **Closed**.

## Use Cases

-   Licensing Example: A state uses both provider and consumer instances of Service Exchange. Users in the consumer instance need to access specific content or complete tasks in the provider instance. With Remote Content Items, users can click on a catalog item in the consumer instance, which opens a new tab and logs them into the provider instance to complete the task seamlessly.​
-   Integration Example: Users clicking on a catalog item in the consumer instance, which opens a new tab and logs them into the provider instance to complete the task. This ensures that users can perform tasks across different instances without any interruptions.​

