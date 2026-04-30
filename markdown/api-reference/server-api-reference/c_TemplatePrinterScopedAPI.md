---
title: TemplatePrinter - Scoped
description: The TemplatePrinter API provides methods to handle printing from a mail script to the email message.Prints the string to the email body.Adds non-breaking spaces to the email body.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TemplatePrinter- Scoped

The TemplatePrinter API provides methods to handle printing from a mail script to the email message.

There is no constructor for this API. The methods are called in mail scripts using the template global variable.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TemplatePrinter - print\(String string\)

Prints the string to the email body.

|Name|Type|Description|
|----|----|-----------|
|string|String|String to print.|

|Type|Description|
|----|-----------|
|void| |

```
template.print("Incident number - " + current.number + "\n");
```

## TemplatePrinter - space\(Number spaces\)

Adds non-breaking spaces to the email body.

|Name|Type|Description|
|----|----|-----------|
|spaces|Number|Number of non-breaking spaces to output to the email body.|

|Type|Description|
|----|-----------|
|void| |

```
template.space(4);
```

