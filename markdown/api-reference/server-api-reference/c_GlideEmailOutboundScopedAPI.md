---
title: GlideEmailOutbound - Scoped
description: The scoped GlideEmailOutbound API implements the email object for scoped applications. You can use the GlideEmailOutbound methods with the email global object available in mail scripts. The email object behaves identically for global and scoped applications.Instantiates a scoped GlideEmailOutbound object.Adds the address to either the cc or bcc list.Adds the recipient to either the cc or bcc list, but uses the display name instead of the address when showing the recipient.Returns the email's subject line.Returns the email's watermark.Sets the body of the email.Sets the sender's address.Sets the reply to address.Sets the email's subject line.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideEmailOutbound- Scoped

The scoped GlideEmailOutbound API implements the email object for scoped applications. You can use the GlideEmailOutbound methods with the email global object available in mail scripts. The email object behaves identically for global and scoped applications.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideEmailOutbound - GlideEmailOutbound\(\)

Instantiates a scoped GlideEmailOutbound object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## GlideEmailOutbound - addAddress\(String type, String address\)

Adds the address to either the cc or bcc list.

|Name|Type|Description|
|----|----|-----------|
|type|String|Either cc or bcc, determines the list to which the address is added.|
|address|String|The recipient's email address.|

|Type|Description|
|----|-----------|
|void| |

```
email.addAddress('cc', 'joe.employee@something.com');
```

## GlideEmailOutbound - addAddress\(String type, String address, String displayName\)

Adds the recipient to either the cc or bcc list, but uses the display name instead of the address when showing the recipient.

|Name|Type|Description|
|----|----|-----------|
|type|String|Either cc or bcc, determines the list to which the address is added.|
|address|String|The recipient's email address.|
|displayName|String|The name to be shown instead of the email address.|

|Type|Description|
|----|-----------|
|void| |

```
email.addAddress('bcc', 'joe.employee@something.com', 'dudley rocks');
```

## GlideEmailOutbound - getSubject\(\)

Returns the email's subject line.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The email's subject line.|

## GlideEmailOutbound - getWatermark\(\)

Returns the email's watermark.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The email's watermark.|

```
var watermark = email.getWatermark();
```

## GlideEmailOutbound - setBody\(String bodyText\)

Sets the body of the email.

|Name|Type|Description|
|----|----|-----------|
|bodyText|String|The body of the email.|

|Type|Description|
|----|-----------|
|void| |

```
email.setBody('Dear Sir, ...');
```

## GlideEmailOutbound - setFrom\(String address\)

Sets the sender's address.

|Name|Type|Description|
|----|----|-----------|
|address|String|The sender's email address.|

|Type|Description|
|----|-----------|
|void| |

```
email.setFrom('joe.employee@something.com');
```

## GlideEmailOutbound - setReplyTo\(String address\)

Sets the reply to address.

|Name|Type|Description|
|----|----|-----------|
|address|String|The reply to email address.|

|Type|Description|
|----|-----------|
|void| |

```
email.setReplyTo('joe.employee@something.com');
```

## GlideEmailOutbound - setSubject\(String subject\)

Sets the email's subject line.

|Name|Type|Description|
|----|----|-----------|
|subject|String|Text for the subject line.|

|Type|Description|
|----|-----------|
|void| |

```
email.setSubject('Important Issues to discuss');
```

