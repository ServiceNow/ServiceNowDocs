---
title: Remote tasks
description: Learn how you, as a provider, can resolve and fulfill multiple consumer tasks, such as incidents, cases, and service requests, by using remote tasks. Also as a consumer, you can assign the incidents to multiple providers for resolution.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Service Exchange]
---

# Remote tasks

Learn how you, as a provider, can resolve and fulfill multiple consumer tasks, such as incidents, cases, and service requests, by using remote tasks. Also as a consumer, you can assign the incidents to multiple providers for resolution.

Remote tasks enable you to assign and synchronize the task's data on separate instances so that you can quickly fulfill the service requests from your consumers. Some examples of the consumer requests are as follows:

1.  Request help for issues that your consumers are having with your services.​
2.  Request for service changes to the services that your consumers have purchased.
3.  Request to assign the existing tasks to you so that you can support your consumer's issues​.

## How a remote task works

As a provider, you must first create and publish the remote task definitions that your consumers can use for creating a remote task. You entitle these definitions to your consumers who can adjust the mappings and field data rules or simply activate the definition. Your consumers can apply a trigger on the definition or manually create a remote task for you, the provider, based on an active definition.

For more information, see [Create a remote task definition in Service Exchange for Providers](../task/service-bridge-v2-create-remote-tasks-defs.md).

The remote task feature includes a Remote Task table, which is an extension of the Task table in the ServiceNow AI Platform. With remote tasks, you can enable bidirectional linking of workflows between multiple ServiceNow instances.

**Note:** When data, such as an attachment or task, is shared with another instance through Service Exchange, it becomes part of that instance’s data. Service Exchange does not delete data on remote instances; the receiving instance must handle the deletion if required.

For example, an incident on a consumer instance must be assigned to a provider's instance as a case. The Remote Task record in each instance facilitates the bidirectional flow of the task's data between the case and the incident.

