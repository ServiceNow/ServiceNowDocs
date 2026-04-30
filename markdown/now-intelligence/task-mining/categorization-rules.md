---
title: Categorization rule form in Task Mining
description: Organize and add context to your data by grouping similar workstation activities with user-friendly category names. Categorization rules have a fixed order value that determines how information from apps and windows is shown on an analysis.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Task Mining, Platform Analytics]
---

# Categorization rule form in Task Mining

Organize and add context to your data by grouping similar workstation activities with user-friendly category names. Categorization rules have a fixed order value that determines how information from apps and windows is shown on an analysis.

For information about categorization, see [Categorize workstation activities to simplify analysis](../task/define-default-categorization-rules.md).

<table id="table_y2k_vdx_tcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

File name condition of the application.

</td></tr><tr><td>

Window name

</td><td>

Window name condition of the window.

</td></tr><tr><td>

URL

</td><td>

URL condition of the application or window.

</td></tr><tr><td>

Rank

</td><td>

Order that defines the order in which categorization rules applies.

</td></tr><tr><td>

Activity

</td><td>

Determines how usage of apps and windows is shown on dashboards. Defines whether the activity is work related or other. The available options are:-   **Productive**: Used for work applications.
-   **Non-productive**: Used when the agent is in private mode or used when activities are defined as private.
-   **Break**: Used when the workstation is locked.
-   **Off**: Used when the workstation is turned off.

</td></tr><tr><td>

Category

</td><td>

The type of work being done that the application is related to. Don’t use the **Other** category as other is used by the Max rule and represents uncategorized apps that don’t match any rule and are anonymized by default.

</td></tr><tr><td>

Application

</td><td>

An intuitive name for the application. An application name should only be associated with one category to keep the data clear.

</td></tr><tr><td>

Window name

</td><td>

A name to describe the activity. A value can be used to mask PII. For example, you can use \[\] to mask and replace with the term used in brackets. If this field is empty, the window name from the workstation is used.

</td></tr></tbody>
</table>**Parent Topic:**[Task Mining Reference](../concept/reference-task-mining.md)

