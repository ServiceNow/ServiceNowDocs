---
title: Custom Matcher form
description: The Custom Matcher form includes information about global search custom matchers defined for AI Search. Use this form when creating a custom matcher to return exact-match results from a specific table and column for search terms matching a regular expression.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-06-25"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Custom Matcher form

The Custom Matcher form includes information about global search custom matchers defined for AI Search. Use this form when creating a custom matcher to return exact-match results from a specific table and column for search terms matching a regular expression.

For details on creating a global search custom matcher, see [Create a custom search matcher for global search](../task/create-search-matcher-ais.md).

<table id="table_lxb_c1j_kvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the custom matcher.

</td></tr><tr><td>

Regex

</td><td>

Java regular expression pattern that AI Search compares search queries to. When a search query matches this regular expression pattern, the custom matcher triggers and the search only returns results from the specified **Table** and **Column**. This field is automatically set when you select **Generate Regex**.**Note:** For details on Java regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/regex/Pattern.html).

</td></tr><tr><td>

Table name

</td><td>

Table that you want to restrict search matches to when a user search satisfies the custom matcher's **Regex** regular expression pattern.

</td></tr><tr><td>

Application

</td><td>

Application scope for the custom matcher. This field is automatically set.

</td></tr><tr><td>

Column

</td><td>

Field from the specified **Table** that you want to restrict search matches to when a user search satisfies the custom matcher's **Regex** regular expression pattern.

</td></tr><tr><td>

Active

</td><td>

Option to activate the custom matcher. To deactivate the matcher, clear the **Active** option.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

