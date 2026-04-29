---
title: Messaging - Scoped
description: The Messaging API provides methods to perform actions in a third-party messaging application.Sends a custom message to a third-party application in response to a messaging event. For example, you can send a custom welcome message to a Slack channel when the Now Actions application installs.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Messaging- Scoped

The Messaging API provides methods to perform actions in a third-party messaging application.

This class requires the Messaging Notification plugin \(com.glide.notification.messaging\) and an integration with a third-party messaging application such as Slack or Teams. Use these methods in an action script in the Message Actions \[messaging\_observer\_handler\] table.

Use the `sn_notification` namespace to access the Messaging API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Messaging - send\(GlideRecord messagingApplication, String recipient, GlideRecord messagingContent, GlideRecord target\)

Sends a custom message to a third-party application in response to a messaging event. For example, you can send a custom welcome message to a Slack channel when the Now Actions application installs.

Use this method in an action script in the Message Actions \[messaging\_observer\_handler\] table.

|Name|Type|Description|
|----|----|-----------|
|messagingApplication|GlideRecord|Third-party application to send a message to from the Messaging Entities \[messaging\_application\] table.|
|recipient|String|Recipient of the message. When the instance receives an inbound message, you can send a response to a Slack channel, Team, or individual user ID found in the inbound payload.|
|messagingContent|GlideRecord|Message content to send from the Messaging Contents \[messaging\_content\] table.|
|target|GlideRecord|Record used to define dynamic field values in the message. Table must match the **Target table** field in the Messaging Contents record. If the Messaging Contents record does not use a target table, set the value to null.|

|Type|Description|
|----|-----------|
|void| |

```
//Send a message to a Teams user
var app = new GlideRecord('messaging_application');
app.get('1f2d26527f4213007f005212bdfa9102');

var content = new GlideRecord('messaging_content');
content.get('17f1f9617320130082999cfd7bf6a706');

sn_notification.Messaging.send(app, '29:1ojsgDg1xuA_jZ70PDI2_6E7mn7P6Mc0wK7z0n2lblL-SaNXYVI1cR7i6qncllAGvdmhy2-kXh76IEVpUHXdz3w', content, null);

//Send a message to a Slack user
var app = new GlideRecord('messaging_application');
app.get('5d2e38c07f6113007f005212bdfa9160');

var content = new GlideRecord('messaging_content');
content.get('69c48ba77310130082999cfd7bf6a7af');

sn_notification.Messaging.send(app, 'U8P706QFQ', content, null);

//Send a message to a Slack channel
var app = new GlideRecord('messaging_application');
app.get('5d2e38c07f6113007f005212bdfa9160');

var content = new GlideRecord('messaging_content');
content.get('69c48ba77310130082999cfd7bf6a7af');

sn_notification.Messaging.send(app, 'CA6232N65', content, null);
```

