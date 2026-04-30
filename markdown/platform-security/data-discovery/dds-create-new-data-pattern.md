---
title: Create new data pattern
description: Create a new Data Discovery store pattern.
locale: en-US
release: zurich
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Discovery sources, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Create new data pattern

Create a new Data Discovery store pattern.

## Before you begin

Role required: discovery.admin

## Procedure

1.  Navigate to **All** &gt; **Data Discovery** &gt; **Sources**.

2.  Select **All Patterns** in the navigation pane.

3.  Select the **Create new** button.

4.  Fill in the form.

<table id="table_unl_ndg_cgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Description of the pattern.

</td></tr><tr><td>

Name

</td><td>

Name of the data pattern.

</td></tr><tr><td>

Expression

</td><td>

Regular expression used to discover the data pattern. **Note:** Expression length must be less than 1000 characters.

</td></tr><tr><td>

Keyword

</td><td>

A specific word\(or words separated by comma\) to be searched for around a expression. Must be used with **Keyword Proximity****Note:** A keyword can be used to search for additional context for a pattern. For example, using keyword can help differentiate between a date of birth or a date of hire given they have the same MM/DD/YY formatting.

</td></tr><tr><td>

Keyword Proximity

</td><td>

How far from the expression to search for keywords. Must be used with **Keyword****Note:** Default is 30, upper bound of 64

</td></tr><tr><td>

Privacy Technique Configuration

</td><td>

Privacy technique used for the pattern

</td></tr><tr><td>

Synthetic Value

</td><td>

List of values substituted for the patterns

</td></tr><tr><td>

Type

</td><td>

Type of pattern

</td></tr><tr><td>

Application

</td><td>

Application scope of pattern.

</td></tr><tr><td>

Scope

</td><td>

Scope of the pattern.

</td></tr></tbody>
</table>5.  Select the **Test** button to test your regular expressions if necessary.

6.  Select **Submit**.


## Result

The new data pattern must be set as active to be used in discovery jobs. See [Select active data patterns](dds-active-data-patterns.md) for more information.

