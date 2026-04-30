---
title: Contextual search properties
description: Contextual search properties are used to control the fields that you can search from and the number of results displayed per page.
locale: en-US
release: zurich
product: Contextual Search
classification: contextual-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Contextual search, Search administration, Configure core features, Administer]
---

# Contextual search properties

Contextual search properties are used to control the fields that you can search from and the number of results displayed per page.

The contextual search properties are available at **Contextual Search** &gt; **Properties**.

<table id="table_oqg_wbw_wq"><thead><tr><th>

Property label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default value for maximum number of search results returned for table and record producer configurations \[com.snc.contextual\_search.result.default.limit\]

</td><td>

Default value for the maximum number of search results returned when you create a table or record producer configuration. By default, the value is 10.

</td></tr><tr><td>

Number of characters that a configured field needs before triggering a search\[com.snc.contextual\_search.min\_length\]

</td><td>

Number of characters that contextual search requires before triggering a search based on the text entered in the search field. By default, the value is set to 3 characters.This property also applies to the Agent Assist search.

</td></tr><tr><td>

Number of milliseconds that a configured field will wait before triggering a search\[com.snc.contextual\_search.wait\_time\]

</td><td>

Number of milliseconds that contextual search waits before triggering a search based on the text entered in the search field. By default, the value is set to 1,000 milliseconds \(one second\).

</td></tr><tr><td>

Records returned above this threshold will log warnings \[com.snc.contextual\_search.result.threshold\]

</td><td>

Triggers a warning message within the system log whenever more than this number of results are returned in a search. This logging helps if you’re experiencing performance issues because of large searches. By default, the value is set to 10,000 results.

</td></tr><tr><td>

When a Form configuration is created a search field with a name matching this property will be automatically created \[com.snc.contextual\_search.widget.form.default\_field\]

</td><td>

The default field that is used for searching when you create a table configuration. By default, the value is set to short\_description.

</td></tr><tr><td>

Collapse the search results widget when creating a new record in a form \[com.snc.contextual\_search.widget.form.open\_collapsed\_new\_records\]

</td><td>

When the value is set to true and you create a record, the search results widget is collapsed to save space. By default, the value is set to false.

</td></tr><tr><td>

Collapse the search results widget when opening an existing record in a form \[com.snc.contextual\_search.widget.form.open\_collapsed\_existing\_records\]

</td><td>

When the value is set to true and you open an existing record, the search results widget is collapsed to save space. By default, the value is set to true.**Note:** The property applies only to existing records and not to new records.

</td></tr><tr><td>

Auto expand the search results widget when search field updates in a form\[com.snc.contextual\_search.widget.form.expand\_on\_search\_field\_update\]

</td><td>

When the value is set to true and you update the search field in a form, the search results widget automatically expands and runs the search. By default, the value is set to true.

</td></tr><tr><td>

Show meta data on form contextual search results \[com.snc.contextual\_search.widget.form.show\_meta\_data\]

</td><td>

When the value is set to true, each search result includes additional metadata below each result record. By default, the property is set to true. -   For Knowledge articles, you configure the metadata fields to display by modifying Knowledge search properties. As an example, you can display the article's author, article number, and knowledge base name. For details on Knowledge search properties, see [Knowledge Management properties](https://www.servicenow.com/docs/access?context=r_KnowledgeProperties&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   Configure the search result display fields for other resources by editing search result display configurations. For details on search result display configuration settings, see [Edit search resource display field record](../task/edit-addi-resources-field.md).

</td></tr><tr><td>

Always force a relative link in the cxs\_new\_window UI Page\[com.snc.contextual\_search.cxs\_new\_window.force\_relative\_link\]

</td><td>

The property ensures that only relative links open from the contextual search modal window. By default, the property is set to true.When the value is set to true, a link opened from the contextual search modal window is forced to be a relative link.

When the value is set to false, a relative or external link can be opened from the contextual search modal window.

To review this property in the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

**Note:** The contextual search window is displayed in the core UI.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring contextual search](../concept/configuring-contextual-search.md)

