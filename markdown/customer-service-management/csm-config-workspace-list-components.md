---
title: CRM Workspace list components
description: List pages in CRM Workspace are made up of multiple components that present record data from tables and enable agents to search, sort and filter, and select records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/csm-config-workspace-list-components.html
release: australia
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [List pages, CRM Workspace features, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CRM Workspace list components

List pages in CRM Workspace are made up of multiple components that present record data from tables and enable agents to search, sort and filter, and select records.

A list page is a content page that displays records from a table, such as cases or case tasks. List pages use the following components to help agents navigate lists and search, filter, sort, and group records.

## List menu component

The List menu component displays the available and saved lists for the selected source. This component is used in combination with the Record List component bundle to create a list page.

The List menu component includes the following tabs:

-   **Default lists**: displays the lists that have been configured for the selected source. These lists give agents quick access to relevant records.
-   **My lists**: displays the list created by the agent, which can help streamline repeat workflows. Agents can create their own lists from an existing list or by selecting a new source.

The List menu component is configured by admins in UI Builder. For more information about the component, see [List menu](https://horizon.servicenow.com/workspace/components/now-record-list-menu-connected?release=brazil).

## Record List component bundle

The Record List component bundle includes the following components:

-   Record list header
-   Predicate builder
-   Presentation list
-   Pagination control

For more information about the component bundle, see [Record List](https://horizon.servicenow.com/workspace/components/record-list?release=brazil).

## Record list header component

The Record list header component includes the list title and the available list actions:

-   List title: Displays the name of the list.
-   Record count: Badge that shows the number of items in the list.
-   List subtitle: Displays the elapsed time from the last list refresh.
-   Refresh button: Refreshes the list with the latest data from the source table.
-   Declarative actions: Actions configured for the list such as **New** and **Export**.
-   More actions menu: Additional actions available for the list such as **Copy URL**.
-   Search: Opens the search input modal which agents can use to search the list and clear the search.
-   Filter, Sort by, and Group by: Opens the Predicate builder component, a type of condition builder that agents can use to filter, sort, and group list items.

## Predicate Builder component

The Predicate Builder component enables agents to set conditions from the record list header to filter which records appear in a list. Select **Filter**, **Sort by**, or **Group by** to display the conditions panel:

-   Conditions: select fields and values to filter the list.
-   Sort by: select one or more fields to sort the list and select ascending or descending functions.
-   Group by: select the field to group by.
-   Related list conditions: enables filtering with related lists.

For more information, see [Predicate Builder](https://horizon.servicenow.com/workspace/components/now-predicate-builder?release=brazil).

## Presentation list component

The Presentation list component displays data from the source table in columns and rows. This component also includes:

-   Edit form: Selecting the pencil icon next to a list item opens the record in the Edit form modal.
-   **Select all** and **Select row** check boxes.
-   Column headers: Include drag handles that agents can use to reorder columns; labels that describe the column data; and filter, sort, and group options.
-   Column actions: Provides a menu with additional actions.

## Pagination

The record list bundle uses the pagination control component to navigate pages in the list and set the number of rows per page. Pagination control divides a large set of content into multiple pages. It allows users move to the next or previous page, jump to specific pages across multiple pages.

