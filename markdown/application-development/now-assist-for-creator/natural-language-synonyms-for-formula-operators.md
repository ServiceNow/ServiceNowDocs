---
title: Natural language synonyms for formula operators
description: Data Binding Generation enables Now Assist to recognize property names by using a set of frequently used synonyms.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Reference, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Natural language synonyms for formula operators

Data Binding Generation enables Now Assist to recognize property names by using a set of frequently used synonyms.

## Formula operators

With Data Binding Generation, Now Assist can recognize property names through a library of common synonyms. This feature reduces failed field matching and eliminates the need for builders to understand the exact syntax. For instance, the LEN formula operator is associated with various common terms and phrases such as count, how many, length, number of items, and size. This enhancement improves accuracy and speeds up the binding generation process.

Here’s a list of additional examples of operators and their synonyms to guide effective prompt writing:

|Formula operators|Synonyms|
|-----------------|--------|
|LEN|count, how many, length, number of items, size|
|IF|check, case, condition, decision|
|SUM|addition, calculate, add up, total|
|PARSE|decode, break down, interpret, read format|

**Note:** There are more than 70 operators, each with multiple synonyms mapped together.

## Property labels

With Data Binding Generation, Now Assist is able to recognize properties based on keywords found in the data property label. If a prompt uses a synonym that doesn’t match an exact property \(such as, surname\), Now Assist finds the closest related keyword, such as "name". When a prompt includes either an exact property label or part of the label, such as a first name or family name, it matches directly and improves accuracy.

**Parent Topic:**[UI generation reference](../concept/ui-generation-reference.md)

