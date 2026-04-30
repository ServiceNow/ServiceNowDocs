---
title: Service Exchange Remote Catalog items
description: Service Exchange Remote Catalog items are ordered from the consumer's ServiceNow instance, and they create provider tasks in each instance. The provider's agent fulfills these provider tasks in their ServiceNow instance. The data in these tasks is synchronized between instances so that they both can track the progress.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use Service Exchange for providers, Service Exchange for Providers, Service Exchange]
---

# Service Exchange Remote Catalog items

Service Exchange Remote Catalog items are ordered from the consumer's ServiceNow instance, and they create provider tasks in each instance. The provider's agent fulfills these provider tasks in their ServiceNow instance. The data in these tasks is synchronized between instances so that they both can track the progress.

Some common Service Exchange Remote Catalog items are as follows:

-   Help requests
-   Service-affecting issues​
-   Requests for changes in service

## Service Exchange request fulfillment process

1.  The consumer selects a Service Exchange related item from the service catalog.
2.  The consumer provides the information in the Service Exchange request form and clicks **Submit**. When the consumer places the request, the Task View appears.

    Within the view, the consumer can add comments that are replicated in the provider's instance.

3.  In the consumer's instance, a single tracking task type, the Provider Task, is generated, regardless of the service.
4.  The Provider Task is replicated on the provider's instance, triggering a flow that triggers the parent task.
5.  The state of the task in the consumer's instance is set to Received.
6.  In the provider's instance, an agent takes ownership of the parent task by clicking **Assign to me**.
7.  After an agent takes ownership, the state of the Provider Task in the consumer's instance is updated to Work in Progress.

    When the agent posts a comment on the provider's instance, the comment is replicated in the consumer's instance. Comments that the consumer posts are replicated in the provider's instance.

8.  After the agent resolves the request, sets a resolution code, and clicks **Propose solution**, the state of the Provider Task in the consumer's instance is updated to Resolved.

    The Actions menu displays the following options, **Accept**, **Reject**, or **Cancel**.

9.  If the consumer accepts the resolution, the state of the provider task on the consumer's instance, and the state of the request on the provider's instance, are updated to **Closed**.

