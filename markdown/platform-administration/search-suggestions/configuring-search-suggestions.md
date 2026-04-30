---
title: Configuring Search Suggestions
description: You can configure Search Suggestions settings to control the creation of auto-complete suggestions and search suggestions on your instance.
locale: en-US
release: xanadu
product: Search Suggestions
classification: search-suggestions
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Search Suggestions, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring Search Suggestions

You can configure Search Suggestions settings to control the creation of auto-complete suggestions and search suggestions on your instance.

## Configuration overview

<table id="table_bc2_nh2_dzb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Schedule the Build Search Suggestions script](../task/schedule-search-suggestion-builds.md)

</td><td>

Specify how often and at what time the system generates auto-complete suggestions and search suggestions from stored search strings. By default, this task runs daily.

</td></tr><tr><td>

[Schedule suggestion pruning](../task/limit-number-of-suggestions.md)

</td><td>

Specify how often and at what time the system prunes the lowest-rated suggestions to limit the Search Suggestion \[sys\_search\_suggestion\] table to 500,000 suggestions. By default, this task runs weekly.

</td></tr><tr><td>

[Set maximum age for searches used in suggestion generation](../task/set-maximum-number-of-search-strings.md)

</td><td>

Specify the maximum age of search strings the system considers when creating auto-complete suggestions and search suggestions. By default, the system only generates suggestions using search strings from the last 180 days.

</td></tr><tr><td>

[Prevent the creation of suggestions in special cases](../task/preventing-suggestions.md)

</td><td>

Disable generation of suggestions from specific search strings to keep unhelpful terms from appearing in suggestions or to prevent disclosure of personal or secure information. As part of this task, you may want to [test regular expression patterns](../task/test-regular-expressions.md) in your Search Suggestion Exclusion List Rule entries.

</td></tr></tbody>
</table>