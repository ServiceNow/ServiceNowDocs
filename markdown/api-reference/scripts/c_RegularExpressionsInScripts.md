---
title: Using regular expressions in server-side scripts
description: JavaScript regular expressions automatically use an enhanced regex engine, which provides improved performance and supports all behaviors of standard regular expressions as defined by Mozilla JavaScript. The enhanced regex engine supports using Java syntax in regular expressions.The enhanced regex engine includes an additional flag to allow Java syntax to be used in JavaScript regular expressions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_RegularExpressionsInScripts.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Write server-side scripts, Scripting, API implementation, API implementation and reference]
---

# Using regular expressions in server-side scripts

JavaScript regular expressions automatically use an enhanced regex engine, which provides improved performance and supports all behaviors of standard regular expressions as defined by Mozilla JavaScript. The enhanced regex engine supports using Java syntax in regular expressions.

The SNC.Regex API is not available for scoped applications. For scoped applications, remove the SNC.Regex API and use standard JavaScript regular expressions.

For more information on JavaScript regular expressions, see the Mozilla JavaScript documentation on [regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) and [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp).

**Parent Topic:**[Writing server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/server-side-scripting-overview.md)

## Using Java syntax in JavaScript regular expressions

The enhanced regex engine includes an additional flag to allow Java syntax to be used in JavaScript regular expressions.

Regular expressions with the additional flag work in all places that expect a regular expression, such as `String.prototype.split` and `String.prototype.replace`. To use Java syntax in a regular expression, use the Java inline flag j, for example `/(?ims)ex(am)ple/j`

|Flag|Description|
|----|-----------|
|j|Defines a regular expression that executes using the Java regular expression engine. It can be used to access Java-only features of regular expressions \(such as look behind, negative look behind\) or to use Java regular expressions without translating them into JavaScript regular expressions. For example: `var regex = /ex(am)ple/j;`|

