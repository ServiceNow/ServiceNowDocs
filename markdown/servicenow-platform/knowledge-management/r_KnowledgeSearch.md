---
title: Search using Knowledge Management v3
description: Search for knowledge articles from the knowledge homepage using the search bar on the Knowledge Management v3 homepage.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using the homepage of Knowledge Management v3, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Search using Knowledge Management v3

Search for knowledge articles from the knowledge homepage using the search bar on the Knowledge Management v3 homepage.

Search results include only articles and questions you are authorized to read. The search results count do not take into consideration any security rules set for the articles. The number of articles you can access may be lower than the count displayed in the search results page. Documents that are attached to articles are also listed in the search results.

**Note:**

-   To change how the attachments are displayed in the search results, set the **How to display attachments in Knowledge Search Results** **glide.knowman.search.attachment** property. Attachments can be displayed with a text snippet, link only, or not at all.

    **Warning:** Attachments set to display with a text snippet may cause slowness.

-   To use wildcards in your search, navigate to **Contextual Search** &gt; **Search Contexts** &gt; **Knowledge Base Search** and select **Enable wildcard searches**.

Sort knowledge content by relevancy, most recent update, or number of views.

Filter results using the check boxes that appear. Filtering options appear depending on the search text.Knowledge homepage; browsing and searching for articles; viewing articles, providing feedback; posting questions; importing/creating articles

<table id="table_p1c_md5_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Bases

</td><td>

Select a knowledge base to search. You can select only knowledge bases you can access. If you do not select a specific knowledge base, search results include articles and questions from all knowledge bases that you can access. You can also select a knowledge base from the choice list in the search bar.For pinned articles, only those in the selected knowledge base in the corresponding language appear.

</td></tr><tr><td>

Categories

</td><td>

Select one or more knowledge categories. Categories are listed alphabetically.

</td></tr><tr><td>

Authors

</td><td>

Select one or more authors.

</td></tr><tr><td>

Language

</td><td>

The multi-language search feature is available when more than one supported language is enabled.

1.  To enable multi-languages, activate the I18N: Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\) or activate one of the internationalization plugins for the language you require.

**Note:** Activating internationalization plugins for any of the available languages automatically activates the I18N: Knowledge Management Internationalization Plugin v2 plugin.

2.  To display search results in all available languages simultaneously, enable the **glide.knowman.enable\_multi\_language\_search** property.

    1.  Navigate to **Knowledge** &gt; **Administration** &gt; **Properties** &gt; **Knowledge Search Properties** &gt; **Enable multi language search** and select the **Yes** check box.
    2.  Enter `sys_properties.list`in the filter navigator, search for the property to configure, and in the **Value** field, enter `true`.
**Note:** By default, the **glide.knowman.enable\_multi\_language\_search** property is not enabled. Search results are displayed based on the language you select in the language filter on the Search page.


</td></tr></tbody>
</table>**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

**Parent Topic:**[Using the homepage of Knowledge Management v3](../concept/c_KnowledgeHomepage.md)

**Related topics**  


[Knowledge Management properties](r_KnowledgeProperties.md#)

