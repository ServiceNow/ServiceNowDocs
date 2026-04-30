---
title: Lists in the classic environment
description: A list displays a set of records from a table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Lists in the classic environment

A list displays a set of records from a table.

**Note:** This content pertains to the Classic Environment, which refers to working in lists of records and on record forms directly, not in the [Configurable Workspace interface](../../../administer/configurable-workspace/concept/workspace-landing-page.md). You can work in the Classic Environment with Next Experience active, or with it inactive, which is referred to as Core UI, \(formerly known as UI16\).

Users can search, sort, filter, and edit data in lists. Lists may be embedded in forms and may be hierarchical \(have sublists\).

The list interface consists of a title bar, filters and breadcrumbs, columns of data, and a footer. Each column in a list corresponds to a field on the table.

A [Response time indicator](../../common-ui-elements/concept/c_ResponseTimeIndicator.md) \(![Response time indicator](../image/Response_time_indicator_UI15.png)\) may appear at the bottom right of some lists to indicate the processing time required to display the list.

![Record list](../image/800px-UI16_list_view.png "Record list")

## List features and actions

The list interface consists of a title bar, filters and breadcrumbs, and columns of data. Each of these components provides features and lets you act on the list and the displayed records.

![Features, menus, and actions.](../image/list-features-UI16.png "Features, menus, and actions")

## Hierarchical lists

Hierarchical lists allow users to view records from related lists directly without navigating to a form.

Lists can have sublists in a hierarchy that can also be accessed in list view. To expand or collapse the related lists on a record in a hierarchical list, click the arrow \(![Arrow](../image/Arrow.png)\) beside the reference icon.

![Hierarchical list](../image/HierarchicalList.png "Hierarchical list")

Administrators can enable hierarchical lists for a table. For more information, see [Enable a hierarchical list](https://www.servicenow.com/docs/access?context=t_EnableAHierarchicalList&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) .

## Detail rows

Detail rows, when enabled, appear below the field row for each record and display the value of a specified field. For example, the detail row might display the short description for each incident in a list. Detail rows support the same functionality as fields, including links, editing capabilities, and access to the context menu.

**Note:** When a field is designated as the source for the list detail rows, the system hides the list column for that field.

![Detail rows](../image/400px-Detail_rows.png "Detail rows")

Administrators can enable detail rows and add them to lists. For more information, see [Administer detail rows](https://www.servicenow.com/docs/access?context=t_EnableDetailRows&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   **[List fields](../reference/r_Fields.md)**  
Fields display data and provide certain functions.
-   **[Configure and use list functions](../task/configure-use-list-functions.md#)**  
All users can interact with lists for the tables their role permits them to access. Some list and column header menu options are controlled by permissions grated to the user role.
-   **[Activity streams in list view](c_DisplayActivityStreams.md)**  
Stream live activity information for all records on the current list.
-   **[Search a list](../task/t_SearchAList.md#)**  
You can search a list to find information quickly. The list title bar includes options for searching the list. Administrators can enable text searches for any list.
-   **[Grouped lists](c_GroupedLists.md#)**  
Grouping aggregates a list by a field and displays the record count per group. Grouping can help you find data quickly by organizing and providing a summary of search or filter results.
-   **[Filters and breadcrumbs](c_UsingFiltersAndBreadcrumbs.md)**  
A filter is a set of conditions applied to a table to help you find and work with a subset of the data in that table.
-   **[Methods for list edits](../reference/r_MethodsForListEdits.md)**  
Users can edit data in lists using various methods.
-   **[Personal lists](c_PersonalLists.md#)**  
You can create personal lists to customize which columns appear and the order in which they appear. Personal lists modify a specific list view according to your individual preferences.

**Parent Topic:**[Working in the classic environment](../../../get-started/servicenow-overview/concept/working-in-classic-lists-and-forms.md)

