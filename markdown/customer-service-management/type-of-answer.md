---
title: Answer types for questions
description: Several answer types are available for agents to provide answers to questions in a decision tree.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add questions or instructions to a decision tree, Configuring decision trees in Decision Tree Builder, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Answer types for questions

Several answer types are available for agents to provide answers to questions in a decision tree.

<table id="table_ugg_fft_qwb"><thead><tr><th>

Choice

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choice

</td><td>

A list of choices. The list types are:-   **New list**: New choice list
-   **Pre-defined list from a table**: Existing choice list from a selected table

**Use "None" as the first choice in the list**: Option to add **None** as the default value in the list.

</td></tr><tr><td>

Date

</td><td>

Date in the format of YYYY-MM-DD

</td></tr><tr><td>

Date/time

</td><td>

Date and time in the format of YYYY-MM-DD HH:MM:SS

</td></tr><tr><td>

Decimal

</td><td>

A number including decimal points.

</td></tr><tr><td>

Integer

</td><td>

A number that does not include decimal points.

</td></tr><tr><td>

Reference

</td><td>

Reference to a field from another table. When this answer type is selected, the following fields appear:-   **Reference table**: Table for selecting a field from.
-   **Apply a filter**: Condition to filter the search results.

For example, the Caller field on the Incident table is a reference to the User \[sys\_user\] table.

</td></tr><tr><td>

String

</td><td>

A line of text. When this answer type is selected, the following field appears:**Maximum number of characters**: Length limit of the text string.

</td></tr><tr><td>

True/False

</td><td>

Check box that enables the user to indicate whether the condition is true or false. If selected, it returns a value of true.

</td></tr></tbody>
</table>