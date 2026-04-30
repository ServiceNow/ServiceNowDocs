---
title: GlideNotification - Client
description: The GlideNotification API provides methods that display messages over the page content.Displays the specified string over the page content as the specified type of message. When the duration timer expires, the message is removed.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideNotification- Client

The GlideNotification API provides methods that display messages over the page content.

Access this API using the `g_notification` global object. List V3 must be activated for the g\_notification object to be available.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideNotification - show\(String type, String message, Number duration\)

Displays the specified string over the page content as the specified type of message. When the duration timer expires, the message is removed.

**Note:** When using this method in a scoped application, you must specify the associated namespace `nowapi`. For example, `nowapi.g_notification.show("info", "The record has been updated", 10000);`

<table id="table_yyd_2bc_mv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

type

</td><td>

String

</td><td>

Type of message to display.Valid values:

-   error
-   info
-   warning

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Message to display.

</td></tr><tr><td>

duration

</td><td>

Number

</td><td>

Optional. Amount of time to display the message.Unit: Milliseconds

Default: 5,000

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
// Displays an info message at the top of the screen
g_notification.show("info", "The record has been updated", 10000);
	 
// Displays an error message at the top of the screen in a scoped app
nowapi.g_notification.show("error", "You need to provide notes!");
```

