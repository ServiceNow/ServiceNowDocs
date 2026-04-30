---
title: Lists
description: Learn about the components in UI Builder that enable admins to create and customize lists and list pages for a Configurable Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Lists

Learn about the components in UI Builder that enable admins to create and customize lists and list pages for a Configurable Workspace.

## Lists overview

A [list](../configurable-workspace-glossary.md#) is a content page that displays zero or more records from a database table. The list has rows and columns. Each row is a record, and each column is a field from the record.

Lists display multiple records in a Configurable Workspace, such as cases, task, or incidents, so that agents can find and work on records quickly.

## List pages in Configurable Workspace

A list page is a workspace page designed to help agents navigate, filter, and manage records. List pages for Configurable Workspace are created with the List page template in UI Builder. The List page template includes the Record List component bundle and List menu component.

![](../image/configurable-workspace-list-page.png)

## Record List component bundle

The Record List component bundle includes the following components.

-   **Record List Header**

    The Record List Header shows contextual information about the list.

-   **Presentational List**

    The Presentational List displays the actual list of records from any data source in a tabular format.


The Record List component bundle is configured by admins in UI Builder.

## List menu component

The List menu component displays all available and saved lists for the selected source. It's not included in the Record List component bundle itself but exists within a list page.

The List menu component includes the following tabs.

-   **Default lists**

    The Default lists tab displays all available lists based on the selected source. These lists gives agents quick access to relevant records.

-   **My lists**

    The My lists tab enables agents to access their saved lists that help streamline repeat workflows and create their own lists from an existing list or by selecting a new source.


The List menu component is configured by admins in UI Builder. For information on List menu component configurations, see [List menu UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-record-list-menu-connected/uib-setup).

## Predicate Builder

The Predicate Builder component enables agents to set conditions from the list header to filter which records appear in a list.

![Predicate Builder for a Configurable Workspace](../image/configurable-workspace-predicate-builder.png)

The Predicate Builder is configured by admins in UI Builder.

