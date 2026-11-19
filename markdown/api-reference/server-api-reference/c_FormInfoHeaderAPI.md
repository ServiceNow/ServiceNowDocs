---
title: FormInfoHeader - Global
description: The FormInfoHeader script include provides methods to add an HTML message as a form info message.Adds an HTML message to the form header, where form info messages are displayed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/server-api-reference/c\_FormInfoHeaderAPI.html
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# FormInfoHeader- Global

The FormInfoHeader script include provides methods to add an HTML message as a form info message.

The addMessage\(\) method is commonly used in record producers.

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/server-api-reference/api-server.md)

## FormInfoHeader - addMessage\(String message\)

Adds an HTML message to the form header, where form info messages are displayed.

|Name|Type|Description|
|----|----|-----------|
|message|String|A message that may include HTML tags.|

|Type|Description|
|----|-----------|
|void| |

```
gs.include("FormInfoHeader");
  var fi = new FormInfoHeader();
  fi.addMessage('This incident was opened on your behalf<br/>
     The IT department will contact you for further information or when the incident is resolved');
```

