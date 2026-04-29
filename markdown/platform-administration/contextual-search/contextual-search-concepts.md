---
title: Contextual search concepts
description: Contextual search concepts help you to understand different contextual search components that are used in the documentation, configuration, and user interface. Understanding of the concepts makes it easier for you to comprehend the interconnection between the components.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Contextual search concepts

Contextual search concepts help you to understand different contextual search components that are used in the documentation, configuration, and user interface. Understanding of the concepts makes it easier for you to comprehend the interconnection between the components.

Contextual search uses terms and concepts that can differ from industry norms due to the unique nature of the ServiceNow platform. Contextual search includes the following concepts and components:

-   **[Search resource](../task/t_ApplyConfigurationToSearch.md)**

    Resource that can be searched such as Catalog or Knowledge Articles. As the resources are scripted and contain JavaScript, they can combine results from more than one table.

    **Note:**

    -   ServiceNow provides pre-defined scripted search resources. You can't create, update, or delete search resources.
    -   A search resource uses the [Zing search engine](../../search-administration/reference/features-search-administration.md) to search a table.
-   **[Searcher](../task/t_ViewASearcher.md)**

    A single search resource or a group of search resources that can be searched. For example, the Knowledge and catalog searcher contains Knowledge Articles, Questions and Catalog Items as its search resources.

    **Note:** ServiceNow provides pre-defined searchers. You can't create, update, or delete searchers.

-   **[Additional resources](../task/add-addi-resource-to-source-list.md)**

    An additional resource is a single table source with query conditions that you can search. Additional resources aren't scripted as you search from a single table. For example, Resolved Incidents \(within the last six months\).

    **Note:**

    -   ServiceNow provides pre-defined additional resources. You can't create or delete additional resources, but can update additional resources to better match your organization requirements. For example, you can update the condition and description for Resolved Incidents \(Last 6 months\) to change it to Resolved Incidents \(Last 3 months\).
    -   An additional resource performs the search based on the type of the source:
        -   Table: The [Zing search engine](../../search-administration/reference/features-search-administration.md) to used to search a table.
        -   [Predictive Intelligence similarity](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US): Search is based on similarity and not on the Zing search engine.
-   **[Search result display fields](../task/edit-addi-resources-field.md)**

    Defines the fields whose values are displayed with the search result of an additional resource. The fields can include **Assigned to**, **Opened by**, and **State**. The search result display fields appear at the bottom of a search result record.

    **Note:** ServiceNow provides pre-defined search result display fields. You can't create or delete additional resources, but you can update search result display fields to better match your organization requirements. For example, change which field to use as a title or the description or which fields to show at the bottom of a search result record.

-   **[Search context](../task/t_DefineSearchContext.md)**

    Brings together a searcher and additional resources \(if any\) that can be searched.

    **Note:** ServiceNow provides pre-defined search contexts. You can also create search contexts.

-   **[Searcher text](../task/t_DefineSearchContext.md)**

    Defined in a search context, a searcher text specifies a user-friendly group name for the searcher. When a searcher contains more than one search resource, a group name is used to represent that group of search resources. For example, the Incident Deflection search context uses a searcher that searches Knowledge Articles, Questions and Catalog Items. The user-friendly searcher group name that represents all of them is Knowledge &amp; Catalog.

-   **[Search on tab](../task/t_DefineSearchContext.md)**

    Defined in the search context, **Search on tab** specifies when a contextual search should start the search. The different scenarios when search is performed are:

    -   If you select the **Search on tab** check box, the search only runs when you update and leave the search field \(recommended\).
    -   If you clear the **Search on tab** check box, the search runs when you pause typing.
-   **[Search actions](../task/modify-search-actions-avail-for-cxs.md)**

    Specifies the actions for each such results. For example, for catalog items, the search action is **Order** and for knowledge articles it's **Attach**. All sources have the **This helped** action.


**Parent Topic:**[Contextual search](c_ContextualSearch.md)

