---
title: Define an AI Search Results Action
description: Configure which portal page opens when a result is selected from the list of search results.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [AI Search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Define an AI Search Results Action

Configure which portal page opens when a result is selected from the list of search results.

## Before you begin

Role required: sp\_admin or admin

## About this task

This configuration is required for UXF Client Action buttons in genius results or search results cards.

**Note:** If the action is being implemented as a server script, the script is executed by the search widget. Notification messages defined in the server script are displayed.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **AI Search** &gt; **Search Results Action** and select **New**.

2.  On the form, fill in the fields.

<table id="table_mfl_y4s_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

A unique description of the search results action.

</td></tr><tr><td>

Service Portal\(s\)

</td><td>

Portals in which the search results action appears. If left blank, the search results action appears in all active portals.

</td></tr><tr><td>

AI Search Source

</td><td>

Content that portal users can search on, including tables in your instance or external data sources. For more information, see [Defining search sources](https://www.servicenow.com/docs/access?context=search-sources-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Action name

</td><td>

Name of the action assignment. Only navigation actions are supported for selecting a search result in portals.

</td></tr><tr><td>

Application

</td><td>

Application scope of the search results action.

</td></tr><tr><td>

Active

</td><td>

Option to activate the search results action.

</td></tr><tr><td>

Order

</td><td>

Priority that the search results action takes over other actions with the same configuration. To give higher priority to an action, enter a lower number.

 If two actions have the same order, then the oldest action takes priority.

</td></tr><tr><td>

Portal page

</td><td>

Page on that opens when a result from the search source is selected from the list of search results.

</td></tr><tr><td>

Payload query parameters

</td><td>

Query parameters to apply to the URL.

-   In the first drop-down, select the payload fields that correspond to the selected **Action name**.

**Note:** You can find the payload fields by opening the record referenced in the **Action name** field. Then, in the Action Assignment record, open the record referenced in the **Specify client action** field. The **Payload** field in the Action Payload Definition record specifies the fields used.

-   In the next field, enter the query parameter to use in the URL.


</td></tr><tr><td>

Additional query parameters

</td><td>

Custom query parameters to use in addition to the payload query parameters. For example, to add `view=sp` as a query parameter, you would enter `view` and `sp` in the **Name** and **Value** fields, respectively.

</td></tr></tbody>
</table>3.  Select **Submit**.


**Parent Topic:**[AI Search in Service Portal](../concept/ai-search.md)

