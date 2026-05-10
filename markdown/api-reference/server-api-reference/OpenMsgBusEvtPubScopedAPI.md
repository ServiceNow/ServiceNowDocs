---
title: OpenMessageBusEventPublisherOOB - Scoped
description: The OpenMessageBusEventPublisherOOB script include provides a method for sending messages to the spoke selector, which sends the messages to the configured REST proxy.Sends the passed message to a custom message platform's REST proxy using the spoke selector.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OpenMessageBusEventPublisherOOB- Scoped

The OpenMessageBusEventPublisherOOB script include provides a method for sending messages to the spoke selector, which sends the messages to the configured REST proxy.

This script includes runs in the `sn_api_notif_mgmt` namespace. The admin role is required to access this script include.

For additional information on how to configure your instance to use this script include, see [Configure the Producer Event Notification Framework to use the Open Message Bus](../../../../../integrate/guides/ProducerEventNotifFramework/task/prod_evt_not-dev_gd-cfg_open_bus.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OpenMessageBusEventPublisherOOB - publishMessageToComptibleRestProxy\(Object tmfEventPayload, Array compatibleTopicArr\)

Sends the passed message to a custom message platform's REST proxy using the spoke selector.

For additional information on this process, see [Producing outbound trouble ticket notifications using the open message bus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/trouble-ticket-workflow-using-pub-sub-model.md). For information on how to implement this method, see [Configure the Producer Event Notification Framework to use the Open Message Bus](../../../../../integrate/guides/ProducerEventNotifFramework/task/prod_evt_not-dev_gd-cfg_open_bus.md).

<table id="table_vhg_zzf_zzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tmfEventPayload

</td><td>

Object

</td><td>

Event message to send. For additional information on the format, see [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).Format: TMF688

</td></tr><tr><td>

compatibleTopicArr

</td><td>

Array

</td><td>

List of topic record sys\_ids for which the passed event payload should be published.Table: Topic \[sn\_api\_notif\_mgmt\_topic\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
 publishEventToOpenMessageBus: function(tmfEventPayload) {
  // Fetch compatible topics
  var compatibleTopicArr = new TopicPickerUtils00B().fetchEventCompatibleTopic(tmfEventPayload);
  // Publish event in topic through REST proxy 
  new OpenMessageBusEventPublisherOOB().publishMessageToComptibleRestProxy(tmfEventPayload, compatibleTopicArr);
},
```

