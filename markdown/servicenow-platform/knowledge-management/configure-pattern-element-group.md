---
title: Configure pattern element groups for Self-Service Analytics
description: Define a logical combination of two pattern elements, pattern element group, or both and how many times the combination occurs. Each pattern element group is implemented as regular expressions.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Self-Service Analytics, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure pattern element groups for Self-Service Analytics

Define a logical combination of two pattern elements, pattern element group, or both and how many times the combination occurs. Each pattern element group is implemented as regular expressions.

## Before you begin

[Configure pattern elements for Self-Service Analytics](configure-pattern-element.md).

Role required: sn\_ssa\_core.self\_service\_manager

## About this task

By default, the system includes pattern element groups for analyzing activity patterns within the Knowledge, Catalog, Communities, and Virtual Agent self-service channels. These pattern elements are available with the Self-Service Analytics for Customer Service plugin \[com.snc.pa.self\_service\_analytics\_csm\].

## Procedure

1.  Navigate to **All** &gt; **Self-Service Analytics** &gt; **Configuration** &gt; **Pattern Element Group**.

2.  Either configure an existing group or create a new group.

    -   Select an existing group in the Pattern Element Groups list.
    -   Create a new group by clicking **New**.
3.  On the Pattern Element Group form, fill in the fields.

<table id="table_omb_d3m_nlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the pattern element group.

</td></tr><tr><td>

First Element

</td><td>

Conditional regular expression consisting of a pattern element or pattern element group.

</td></tr><tr><td>

Second Element

</td><td>

Another conditional regular expression consisting of a pattern element or pattern element group.

</td></tr><tr><td>

Application

</td><td>

Scope of the application that contains the user entity. This field is automatically set based on the application scope selected in the application picker.

</td></tr><tr><td>

Operator

</td><td>

Logical operator that returns the result of the combination of the first and second elements. Valid values are:-   **And**: Both the first and second elements are true.
-   **Or**: Either the first or second element is true.


</td></tr><tr><td>

Occurrence

</td><td>

Frequency with which a pattern element or pattern element group must occur. An occurrence is one of the following types:

 -   **Once**: Must have occurred only once.
-   **Optionally Once**: Might not have occurred but if it has, then it has occurred only once.
-   **Optionally Many**: Might not have occurred but if it has, then it has occurred multiple times.
-   **At Least Once**: Has occurred at least once.
-   **Range**: Has occurred within a range. You specify a range using the **Minimum** and **Maximum** fields.


</td></tr><tr><td>

Minimum

</td><td>

Minimum occurrence of the result of the logical combination of the first and second elements. This field appears only when Occurrence is set to **Range**.

</td></tr><tr><td>

Maximum

</td><td>

Maximum occurrence of the result of the logical combination of the first and second elements. This field appears only when Occurrence is set to **Range**.

</td></tr></tbody>
</table>4.  Save the pattern element group settings.

    -   Save a new pattern element group by clicking **Submit**.
    -   Save the changes to an existing pattern element group by clicking **Update**.

## What to do next

[Configure activity patterns for Self-Service Analytics](configure-activity-pattern.md).

