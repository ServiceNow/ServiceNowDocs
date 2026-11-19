---
title: Custom Matcher form
description: The Custom Matcher form enables you to create a global search custom matcher.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/custom-matcher-form-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Custom Matcher form

The Custom Matcher form enables you to create a global search custom matcher.

For details on creating a global search custom matcher, see [Create a custom search matcher for global search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-search-matcher-ais.md).

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
</table>**Parent Topic:**[AI Search reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/reference-ais.md)

