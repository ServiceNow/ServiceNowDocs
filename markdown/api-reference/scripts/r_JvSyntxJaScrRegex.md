---
title: Using Java syntax in JavaScript regular expressions
description: The enhanced regex engine includes an additional flag to allow Java syntax to be used in JavaScript regular expressions.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using regular expressions in server-side scripts, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Using Java syntax in JavaScript regular expressions

The enhanced regex engine includes an additional flag to allow Java syntax to be used in JavaScript regular expressions.

Regular expressions with the additional flag work in all places that expect a regular expression, such as `String.prototype.split` and `String.prototype.replace`. To use Java syntax in a regular expression, use the Java inline flag j, for example `/(?ims)ex(am)ple/j`

|Flag|Description|
|----|-----------|
|j|Defines a regular expression that executes using the Java regular expression engine. It can be used to access Java-only features of regular expressions \(such as look behind, negative look behind\) or to use Java regular expressions without translating them into JavaScript regular expressions. For example: `var regex = /ex(am)ple/j;`|

**Parent Topic:**[Using regular expressions in server-side scripts](../concept/c_RegularExpressionsInScripts.md)

