---
title: spAriaUtil - Client
description: The spAriaUtil API provides methods to show messages on a screen reader.Announce a message to a screen reader.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/spAriaUtil-API.html
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# spAriaUtil- Client

The spAriaUtil API provides methods to show messages on a screen reader.

This API is an angular service that you can use in Service Portal widget client scripts.

**Parent Topic:**[Client API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/api-client.md)

## spAriaUtil - sendLiveMessage\(String message\)

Announce a message to a screen reader.

The sendLiveMessage\(\) method injects text into an aria-live region on the page. The default setting for an aria-live region is `assertive`, which means that messages are announced immediately. This can annoy and confuse users if used too frequently.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to be shown.|

|Type|Description|
|----|-----------|
|void| |

```
function(spAriaUtil) {
  /* widget controller */

  spAriaUtil.sendLiveMessage('Hello world!');
}
```

