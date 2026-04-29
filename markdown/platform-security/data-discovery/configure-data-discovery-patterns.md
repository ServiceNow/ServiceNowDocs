---
title: Configure Data Discovery patterns
description: Configure a Data Discovery pattern and review current patterns. A Data Discovery pattern defines the regular expression used to match data against a target table.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Configure Data Discovery patterns

Configure a Data Discovery pattern and review current patterns. A Data Discovery pattern defines the regular expression used to match data against a target table.

## Before you begin

Role required: data\_discovery\_admin

## Procedure

1.  Navigate to **System Security** &gt; **Data Discovery** &gt; **All Data Patterns**.

2.  In the Data Discovery Pattern list, select **New**.

3.  In the Data Discovery job fields form, fill in the fields.

<table id="table_tgp_2pb_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internal Scope

</td><td>

Scope of the pattern.

</td></tr><tr><td>

Description

</td><td>

Description of the job.

</td></tr><tr><td>

Name

</td><td>

Name of the data pattern.

</td></tr><tr><td>

Application

</td><td>

Application scope of pattern.

</td></tr><tr><td>

Expression

</td><td>

Regular expression used to discover the data pattern. **Note:** Expression length must be less than 1000 characters.

</td></tr><tr><td>

Keyword\(Optional\)

</td><td>

A specific word\(or words separated by comma\) to be searched for around a expression. Must be used with **Keyword Proximity****Note:** A keyword can be used to search for additional context for a pattern. For example, using keyword can help differentiate between a date of birth or a date of hire given they have the same MM/DD/YY formatting.

</td></tr><tr><td>

Keyword Proximity\(Optional\)

</td><td>

How far from the expression to search for keywords. Must be used with **Keyword****Note:** Default is 30, upper bound of 64

</td></tr><tr><td>

Privacy technique configuration

</td><td>

Privacy technique used for the pattern

</td></tr><tr><td>

Synthetic Value

</td><td>

List of values substituted for the patterns

</td></tr><tr><td>

Type

</td><td>

Type of pattern-   **Local**: The pattern is regex-based
-   **Model**: Uses AI/ML service


</td></tr></tbody>
</table>4.  Select **Submit**.

    -   The **Test** button enables you to test your regular expression before submitting the data pattern list.
5.  The data pattern must be set as active to be used with scheduled jobs.
6.  Navigate to **System Security** &gt; **Data Discovery** &gt; **Active Data Patterns**.

7.  In the Data Discovery Active Pattern list, select **Edit**.

8.  Select the pattern list from **Available Lists** and move it to **Selected Lists**.


