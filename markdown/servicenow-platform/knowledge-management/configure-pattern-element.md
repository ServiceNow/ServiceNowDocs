---
title: Configure pattern elements for Self-Service Analytics
description: Configure a pattern element to specify a single activity type and how many times it occurs. Each pattern element is implemented as regular expressions.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Self-Service Analytics, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure pattern elements for Self-Service Analytics

Configure a pattern element to specify a single activity type and how many times it occurs. Each pattern element is implemented as regular expressions.

## Before you begin

[Configure activity contexts for Self-Service Analytics](configure-activity-context.md).

Role required: sn\_ssa\_core.self\_service\_manager

## About this task

By default, the system includes pattern elements for analyzing activity patterns within Knowledge, Catalog, Communities, or Virtual Agent self-service channels. These pattern elements are available with the Self-Service Analytics for Customer Service plugin \[com.snc.pa.self\_service\_analytics\_csm\].

## Procedure

1.  Navigate to **All** &gt; **Self-Service Analytics** &gt; **Configuration** &gt; **Pattern Element**.

2.  In the Pattern Elements list, modify an existing pattern element or click **New** to create another pattern element.

3.  On the Pattern Element form, fill in the fields.

<table id="table_omb_d3m_nlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the pattern element.

</td></tr><tr><td>

Activity Type

</td><td>

Activity type you want to associate with the pattern element.

</td></tr><tr><td>

Application

</td><td>

Scope of the application that contains the user entity. This field is automatically set based on the application scope selected in the application picker.

</td></tr><tr><td>

Occurrence

</td><td>

Frequency with which an activity should occur. An activity occurrence is one of the following types:-   **Once**: An activity must have occurred only once. For example, an article was marked with positive feedback only once.
-   **Optionally Once**: An activity might not have occurred, but if it has, then it has occurred only once. For example, either no catalog request was created or only one was created.
-   **Optionally Many**: An activity might not have occurred but if it has, then it has occurred multiple times. For example, either no catalog request has been created or multiple requests have been created.
-   **At Least Once**: An activity has occurred at least once. For example, a community blog was viewed one or more times.
-   **Range**: An activity has occurred as many times as is specified in a range. You specify a range using the **Minimum** and **Maximum** fields. For example, if you specify a range of 2 to 4 Virtual Agent interactions, only 2, 3, or 4 interactions can have occurred.


</td></tr><tr><td>

Minimum

</td><td>

Minimum occurrence of an activity. This field appears only when **Range** is selected from the Occurrence list.

</td></tr><tr><td>

Maximum

</td><td>

Maximum occurrence of an activity. This field appears only when **Range** is selected from the Occurrence list.

</td></tr></tbody>
</table>4.  Submit or update the pattern element.

    -   Click **Submit** if you created a new pattern element.
    -   Click **Update** if you modified an existing pattern element.

## What to do next

[Configure pattern element groups for Self-Service Analytics](configure-pattern-element-group.md).

**Parent Topic:**[Configure Self-Service Analytics](config-ssa.md)

