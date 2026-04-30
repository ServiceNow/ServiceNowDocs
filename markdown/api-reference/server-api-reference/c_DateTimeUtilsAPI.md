---
title: DateTimeUtils - Global
description: The DateTimeUtils script include is a collection of date/time functions.Converts Microsoft AD integer8 DateTime format into GlideDateTime format.Convert milliseconds to a GlideDateTime object
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DateTimeUtils- Global

The DateTimeUtils script include is a collection of date/time functions.

You can use this script include in any server-side script, and is available through GlideAjax.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DateTimeUtils - int8ToGlideDateTime\(Number int64\)

Converts Microsoft AD integer8 DateTime format into GlideDateTime format.

Integer8 is also known as Microsoft Filetime format. This method is commonly used when importing AD user's date fields, such as Expiration Date.

|Name|Type|Description|
|----|----|-----------|
|int64|Number|A 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 \(UTC\).|

|Type|Description|
|----|-----------|
|GlideDateTime|A GlideDateTime object set to the Integer8 date and time.|

```
//convert and set account expiration date from AD
//this is an example that could be used in an LDAP import transform map to import the LDAP account 
//expires attribute to a customer created u_account_expires GlideDateTime field
var dtUtil = new DateTimeUtils();
target.u_account_expires = dtUtil.int8ToGlideDateTime(source.u_accountexpires);
```

## DateTimeUtils - msToGlideDateTime\(Number milliseconds\)

Convert milliseconds to a GlideDateTime object

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|The number of milliseconds|

|Type|Description|
|----|-----------|
|GlideDateTime|A GlideDateTime object|

```
//example script to call the method from a client
Replace MILLISECONDSVALUE with your variable
var ga = new GlideAjax('DateTimeUtils');
ga.addParam('sysparm_name','msToGlideDateTime');
ga.addParam('sysparm_value', MILLISECONDSVALUE);
ga.getXMLWait();
var newGDT = ga.getAnswer();
```

