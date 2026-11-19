---
title: Child Table form
description: The Child Table form enables you to enable AI Search content indexing for a child table that extends an indexed source table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/child-table-form-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-11-04"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Child Table form

The Child Table form enables you to enable AI Search content indexing for a child table that extends an indexed source table.

For details on creating or modifying an indexed source child table, see [Create an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-indexed-source-ais.md).

<table id="table_ly1_wvl_vnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indexed Source

</td><td>

Reference to the indexed source. This field is automatically set.

</td></tr><tr><td>

Table

</td><td>

Label and name for the child table that you want to enable content indexing for. You can only select from tables that extend the indexed source table. As an example, you can add the FAQ \[kb\_template\_faq\] template table as a child table to the Knowledge Table indexed source, since kb\_template\_faq extends the Knowledge \[kb\_knowledge\] table specified in that indexed source.

</td></tr><tr><td>

Active

</td><td>

Option to activate indexing for the child table.

</td></tr><tr><td>

Application

</td><td>

Application scope for the child table indexing configuration. This field is automatically set.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/reference-ais.md)

