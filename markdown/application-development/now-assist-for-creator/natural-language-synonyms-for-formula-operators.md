---
title: Natural language synonyms for formula operators
description: Data Binding Generation enables Now Assist to recognize property names by using a set of frequently used synonyms.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: reference
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Reference, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Natural language synonyms for formula operators

Data Binding Generation enables Now Assist to recognize property names by using a set of frequently used synonyms.

## Formula operators

With Data Binding Generation, Now Assist can recognize property names through a library of common synonyms. This feature reduces failed field matching and eliminates the need for builders to understand the exact syntax. For instance, the LEN formula operator is associated with various common terms and phrases such as count, how many, length, number of items, and size. This enhancement improves accuracy and speeds up the binding generation process.

Here’s a list of additional examples of operators and their synonyms to guide effective prompt writing:

|Formula Operator|Category|Common Synonyms|
|----------------|--------|---------------|
|`LEN`|Math / String|count, how many, length, number of items, size|
|`SUM`|Math|addition, add up, calculate, total|
|`MIN`|Math|least, lowest, minimum, smallest|
|`MAX`|Math|greatest, highest, largest, maximum|
|`AVG`|Math|average, mean, middle value|
|`ROUND`|Math|round off, round to, to decimal places|
|`ABS`|Math|absolute, magnitude, positive value|
|`CONCAT`|String|append, combine, join, merge strings|
|`TRIM`|String|clean up, remove spaces, strip whitespace|
|`UPPER`|String|capitalize all, make uppercase, to caps|
|`LOWER`|String|all lowercase, make lowercase, to small letters|
|`CONTAINS`|String|has, includes, is part of|
|`STARTSWITH`|String|begins with, leads with, starts|
|`ENDSWITH`|String|closes with, ends in, finishes with|
|`IF`|Logic|case, check, condition, decision, when|
|`AND`|Logic|all of, both, every condition, together with|
|`OR`|Logic|any of, at least one, either|
|`NOT`|Logic|does not, exclude, negate, opposite of|
|`ISBLANK`|Logic|empty, is empty, missing, no value|
|`NOW`|Date / Time|current datetime, right now, today's time|
|`TODAY`|Date / Time|current date, present day, this date|
|`DATEDIFF`|Date / Time|days between, elapsed time, time gap|
|`DATEADD`|Date / Time|add days, days from now, future date|
|`PARSE`|Data|break down, decode, interpret, read format|
|`LOOKUP`|Data|find value, get field, reference table|

**Note:** There are more than 70 operators, each with multiple synonyms mapped together. This table lists the most commonly used operators. For a complete list, open Formula Builder within UI Builder and select **Browse operators**.

## Property labels

With Data Binding Generation, Now Assist is able to recognize properties based on keywords found in the data property label. If a prompt uses a synonym that doesn’t match an exact property \(such as, surname\), Now Assist finds the closest related keyword, such as "name". When a prompt includes either an exact property label or part of the label, such as a first name or family name, it matches directly and improves accuracy.

**Parent Topic:**[UI generation reference](../concept/ui-generation-reference.md)

