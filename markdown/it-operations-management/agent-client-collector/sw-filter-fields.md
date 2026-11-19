---
title: Software filter fields
description: The following table lists the software filter fields from which you can create a filter.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/sw-filter-fields.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-08-23"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector for Visibility Content reference, Agent Client Collector, IT Operations Management]
---

# Software filter fields

The following table lists the software filter fields from which you can create a filter.

<table id="table_dnc_5zm_3kc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive label for the rule. For example, **Exclude company name shortcut**.

</td></tr><tr><td>

Software name

</td><td>

\(Optional\) Enter the display name of the software. In the **Condition** dropdown, select the matching type: -   Starts with
-   Ends with
-   Contains
-   Exact match
-   Regex

</td></tr><tr><td>

Publisher

</td><td>

\(Optional\) Enter the software vendor or publisher name. In the **Condition** dropdown, select the matching type: -   Starts with
-   Ends with
-   Contains
-   Exact match
-   Regex

</td></tr><tr><td>

Version

</td><td>

\(Optional\) Enter the version string. In the **Condition** dropdown, select the matching type:-   Starts with
-   Ends with
-   Contains
-   Exact match
-   Regex

**Note:** Although this field and the **Software name** and **Publisher** fields are optional, at least one of them must have a value.

</td></tr><tr><td>

OS filter

</td><td>

Select the operating system the rule applies to: -   All
-   Windows
-   Linux
-   macOS

</td></tr><tr><td>

Discovery source

</td><td>

\(Optional\) Enter the Discovery source to restrict the rule to installations reported by a specific source. Leave blank to apply the rule to installations from any source.

</td></tr><tr><td>

Active

</td><td>

Toggle to **Active** to enable the rule.

</td></tr></tbody>
</table>