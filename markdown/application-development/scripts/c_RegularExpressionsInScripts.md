---
title: Using regular expressions in server-side scripts
description: JavaScript regular expressions automatically use an enhanced regex engine, which provides improved performance and supports all behaviors of standard regular expressions as defined by Mozilla JavaScript. The enhanced regex engine supports using Java syntax in regular expressions.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Using regular expressions in server-side scripts

JavaScript regular expressions automatically use an enhanced regex engine, which provides improved performance and supports all behaviors of standard regular expressions as defined by Mozilla JavaScript. The enhanced regex engine supports using Java syntax in regular expressions.

The SNC.Regex API is not available for scoped applications. For scoped applications, remove the SNC.Regex API and use standard JavaScript regular expressions.

For more information on JavaScript regular expressions, see the Mozilla JavaScript documentation on [regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) and [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp).

-   **[Using Java syntax in JavaScript regular expressions](../reference/r_JvSyntxJaScrRegex.md)**  
The enhanced regex engine includes an additional flag to allow Java syntax to be used in JavaScript regular expressions.
-   **[Convert SNC Regex expressions to enhanced regex expressions](../task/t_ConvertSNCRegexExpressions.md)**  
When you upgrade to Eureka Patch 5 or later releases, you should convert scripts that use the SNC.Regex API to use regular JavaScript expressions.

**Parent Topic:**[Server-side scripting](../../server-scripting/concept/c_ServerScripting.md)

