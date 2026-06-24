---
title: Lists in the classic environment
description: A list displays a set of records from a table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/c\_UseLists.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Lists in the classic environment

A list displays a set of records from a table.

**Note:** This content pertains to the Classic Environment, which refers to working in lists of records and on record forms directly, not in the [Configurable Workspace interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/workspace-landing-page.md). You can work in the Classic Environment with Next Experience active, or with it inactive, which is referred to as Core UI, \(formerly known as UI16\).

Users can search, sort, filter, and edit data in lists. Lists may be embedded in forms and may be hierarchical \(have sublists\).

The list interface consists of a title bar, filters and breadcrumbs, columns of data, and a footer. Each column in a list corresponds to a field on the table.

A [Response time indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/c_ResponseTimeIndicator.md) \(\[Omitted image "Response\_time\_indicator\_UI15.png"\] Alt text: Response time indicator\) may appear at the bottom right of some lists to indicate the processing time required to display the list.

\[Omitted image "800px-UI16\_list\_view.png"\] Alt text: Record list

## List features and actions

The list interface consists of a title bar, filters and breadcrumbs, and columns of data. Each of these components provides features and lets you act on the list and the displayed records.

\[Omitted image "list-features-UI16.png"\] Alt text: Features, menus, and actions.

## Hierarchical lists

Hierarchical lists allow users to view records from related lists directly without navigating to a form.

Lists can have sublists in a hierarchy that can also be accessed in list view. To expand or collapse the related lists on a record in a hierarchical list, click the arrow \(\[Omitted image "Arrow.png"\] Alt text: Arrow\) beside the reference icon.

\[Omitted image "HierarchicalList.png"\] Alt text: Hierarchical list

Administrators can enable hierarchical lists for a table. For more information, see [Enable a hierarchical list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/list-administration/t_EnableAHierarchicalList.md) .

## Detail rows

Detail rows, when enabled, appear below the field row for each record and display the value of a specified field. For example, the detail row might display the short description for each incident in a list. Detail rows support the same functionality as fields, including links, editing capabilities, and access to the context menu.

**Note:** When a field is designated as the source for the list detail rows, the system hides the list column for that field.

\[Omitted image "400px-Detail\_rows.png"\] Alt text: Detail rows

Administrators can enable detail rows and add them to lists. For more information, see [Administer detail rows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/list-administration/t_EnableDetailRows.md).

-   **[List fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/r_Fields.md)**  
Fields display data and provide certain functions.
-   **[Configure and use list functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-use-list-functions.md)**  
All users can interact with lists for the tables their role permits them to access. Some list and column header menu options are controlled by permissions grated to the user role.
-   **[Activity streams in list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/c_DisplayActivityStreams.md)**  
Stream live activity information for all records on the current list.
-   **[Search a list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/t_SearchAList.md)**  
You can search a list to find information quickly. The list title bar includes options for searching the list. Administrators can enable text searches for any list.
-   **[Grouped lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/c_GroupedLists.md)**  
Grouping aggregates a list by a field and displays the record count per group. Grouping can help you find data quickly by organizing and providing a summary of search or filter results.
-   **[Filters and breadcrumbs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/c_UsingFiltersAndBreadcrumbs.md)**  
A filter is a set of conditions applied to a table to help you find and work with a subset of the data in that table.
-   **[Methods for list edits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/r_MethodsForListEdits.md)**  
Users can edit data in lists using various methods.
-   **[Personal lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/c_PersonalLists.md)**  
You can create personal lists to customize which columns appear and the order in which they appear. Personal lists modify a specific list view according to your individual preferences.

**Parent Topic:**[Working in the classic environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/working-in-classic-lists-and-forms.md)

