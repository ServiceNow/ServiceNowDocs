---
title: Configure sort widget instance options
description: Configure widget instance options for the knowledge sort widget on the Knowledge Management Service Portal search results page.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure sort widget instance options

Configure widget instance options for the knowledge sort widget on the Knowledge Management Service Portal search results page.

## Before you begin

Role required: sp\_admin or admin

## About this task

The search results page uses the Knowledge Result Sort widget to provide sort options for the returned list of results. Use the widget instance options to customize the sort options.

## Procedure

1.  Navigate to the Knowledge Management Service Portal search results page.

2.  Control + right-click the sort options at the top of the results list.

3.  Click **Instance Options**.

4.  Configure the desired settings for the sort widget.

<table id="table_y2w_rhj_tz"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Bootstrap color

</td><td>

The color of the search widget.

</td></tr><tr><td>

CSS

</td><td>

Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://www.servicenow.com/docs/access?context=scss-primer&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Hide Relevancy

</td><td>

Removes the relevancy sort option.

</td></tr><tr><td>

Table

</td><td>

The table that contains the fields used to sort the list of knowledge items. The default table is **Knowledge**.

</td></tr><tr><td>

Sort Fields

</td><td>

The fields used for sorting the list of knowledge items.

</td></tr><tr><td>

Sort Field Labels

</td><td>

The labels for the fields that appear in the sort options. The default is **Views:desc,Newest:desc,Alphabetical**. The sort order for the sort field labels is ascending. To use a descending order, denote **:desc**.

</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

