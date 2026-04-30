---
title: Semantic Index Field form
description: The Semantic Index Field form contains information about a field from an AI Search indexed source that you want to index for semantic vector search. Use this form when defining or modifying semantic index fields in a semantic index configuration.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-02-04"
reading_time_minutes: 2
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Semantic Index Field form

The Semantic Index Field form contains information about a field from an AI Search indexed source that you want to index for semantic vector search. Use this form when defining or modifying semantic index fields in a semantic index configuration.

To learn about defining and modifying semantic indexing settings for an indexed source, see [Configure semantic indexing settings for an indexed source](../task/configure-semantic-indexing-ais.md). For details on semantic index configuration fields, see [Semantic Index Configuration form](semantic-index-configuration-form.md).

**Note:** This form is only available when the AI Search Semantic Controller plugin \(com.glide.ais.semantic\_search\) is active on your instance. To activate this plugin, your instance must have at least one [Now Assist application](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) installed.

<table id="table_t1b_wjh_xcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Semantic Index Name

</td><td>

The name of the semantic index defined in the semantic index field's parent semantic index configuration. This field is automatically set.

</td></tr><tr><td>

Source

</td><td>

ServiceNow AI Platform® source table whose value you want to include in the semantic index.

</td></tr><tr><td>

Type

</td><td>

Type of object to index for semantic vector search.-   Default value: **Field**
-   Supported values:
    -   **Field**: Field from the ServiceNow AI Platform source table specified by your **Source** selection.
    -   **Attachment**: Attachments from the ServiceNow AI Platform source table specified by your **Source** selection.
-   Type: choice list

</td></tr><tr><td>

Application

</td><td>

Application scope for the semantic index field record. This field is automatically set.

</td></tr><tr><td>

Order

</td><td>

Order of concatenation for this field's value relative to the values of other semantic index fields defined in the same semantic index configuration. Fields with lower values appear first in the concatenation.

 This field's value is only meaningful when **Truncate** or **Full Text** is selected from **Chunking Strategy** for the semantic index field's parent semantic index configuration.

-   Supported values: Any positive integer
-   Type: integer

</td></tr><tr><td>

Field

</td><td>

Name of the source table field to include in the semantic index. This field's value will be handled according to the parent semantic index configuration's specified **Chunking configuration for embedding** settings.

 This field is automatically set to **attachment\_body** when **Attachment** is selected from **Type**.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

