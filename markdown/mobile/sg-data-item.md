---
title: Data items
description: Data items provide the data presented in a screen.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile app components, Building mobile apps, Mobile Platform]
---

# Data items

Data items provide the data presented in a screen.

Data items are queries on a selected table that bring back data. Screens, which display data from your instance, get their information from data items. For example, if your application contains a list of incidents, the list would use a data item representing records from the incident \[incident\] table.

## Data item types

There are three different types of data items.

-   **Standard data items**

    A standard data item is used to return data from a single table. A standard data item does not include parameters, but can include a filter to return a set of results from the queried table. For example, a standard data item could query all high priority changes from the change request \[change\_request\] table.

    For information on standard data items, see [Configure a standard data item](../task/sg-studio-create-data-item.md).

-   **Parametrized data items**

    A parametrized data item is used to perform a query containing one or more parameters to return data. Parameters are used to pass in variables to your queries. For example, you could use a parameter to include the value of the logged in user so that you can show a list of all incidents assigned to that user.

    For details on parametrized data items, see [Configure a parametrized data item](../task/sg-config-parametrized-data-item.md).

-   **Relationship data items**

    Relationship data items are necessary for embedded lists. Embedded lists are lists that can be embedded within a record screen. Record screens can have one or more embedded segments. An embedded list is a type of segment that can be embedded. When you configure an embedded list, it's important to be familiar with the original record screen table. It's also important to understand the table that contains the records that appear in the embedded list. To create an embedded list, you need a relationship data item. For details about creating a relationship data item, see [Configure a relationship data item for an embedded list](../task/sg-data-item-relationship.md).


## Special use data item configurations

The following data items do not fit into the previous categories, and are used only in the cases detailed in the following sections.

-   **Append encoded query**

    To navigate from a single score analytics preview or from a chart screen header function to a list of records, you need to configure a special data item using an instance relative URL. This is a standard data item that uses a different type of condition. Find more information about how to configure an append encoded query in [Chart screen](chart-screen.md).

-   **Grouped list data item**

    A grouped data item is used exclusively for a grouped list screen. Any data item, standard and relationship, parametrized or not, can be grouped by a field. Find more info about how to configure grouped list data items at [Grouped list screen](grouped-list-screen.md).


