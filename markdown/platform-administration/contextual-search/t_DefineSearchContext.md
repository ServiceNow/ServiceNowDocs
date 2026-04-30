---
title: Define a search context
description: Define where agents can search for a particular resource. You can specify that the search resources are predefined or additional resources outside the system.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a search context

Define where agents can search for a particular resource. You can specify that the search resources are predefined or additional resources outside the system.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Search Contexts**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_gh2_gtj_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the search context.

</td></tr><tr><td>

Short description

</td><td>

Brief summary of the context.

</td></tr><tr><td>

Searcher

</td><td>

Lookup icon \(![Lookup icon to select a searcher.](../image/look-up-icon.png)\) to select a searcher for this context. The searcher determines the information source to search.-   Catalog only: Provides search results from service catalog items.
-   Knowledge and catalog: Provides search results from knowledge articles and service catalog items.
-   Knowledge only: Provides search results from knowledge articles.
-   Knowledge, Discussions and pinned: Provides search results from knowledge articles, pinned knowledge articles, and ServiceNow Community.
-   Knowledge, pinned knowledge and catalog: Provides search results from knowledge articles, pinned knowledge articles, and service catalog items.
-   Knowledge and pinned knowledge: Searches knowledge articles and pinned knowledge articles.
-   Knowledge, Pinned, Catalog: Provides search results from Knowledge, Pinned Knowledge, and Catalog Items.
-   Knowledge and pinned: Provides search results from knowledge articles and pinned knowledge articles.
-   Pinned Knowledge only: Provides search results from pinned knowledge articles.
 **Note:** The **Searcher** field is optional. You can decide whether to show or hide sources from an agent.

</td></tr><tr><td>

Searcher default search

</td><td>

List used to select a specific resource from the **Searcher** field to search as default.

</td></tr><tr><td>

Searcher text

</td><td>

Unique label for the searcher group that is used when there is more than one resource in the searcher.

</td></tr><tr><td>

Active

</td><td>

Option to activate the search context form.

</td></tr><tr><td>

Enable wildcard searches

</td><td>

Option to enable wildcard characters, such as \* and %, for searches.

</td></tr><tr><td>

Search on tab

</td><td>

Option to determine when to perform the search. If you select this option, the search runs only when you enter text in a field and then leave the field. If you clear the check box, the search runs after you stop typing even though the cursor is still in the same field.**Note:**

To display the search context in the Source selector on Platform, you must select this option. Search contexts with this option deselected don't appear in the Source selector on Platform.

</td></tr></tbody>
</table>    The **Searcher default search** list is available if the **Searcher** is the default search. If an additional resource is the default search, you see the **Set Searcher as the Default Search** related link. For information on how to set the default source for search context, see [Set the default source for search context](set-source-search-context.md).

4.  Select and hold \(or right-click\) the form header and select **Save**.


**Parent Topic:**[Configuring contextual search](../concept/configuring-contextual-search.md)

