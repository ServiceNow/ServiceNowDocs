---
title: Set a filter to follow another filter in a many-to-many relationship
description: In some cases, values on a pair of filters can refer to multiple values on each other. For one such filter to follow another, it must go through a connecting table.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Select or cascading filters, Filters, Platform Analytics experience, Platform Analytics]
---

# Set a filter to follow another filter in a many-to-many relationship

In some cases, values on a pair of filters can refer to multiple values on each other. For one such filter to follow another, it must go through a connecting table.

## Before you begin

Role required: admin

## About this task

In most cases, a filter follows another filter either in a one-to-one relationship or in a one-to-many relationship. In the latter case, the filter source is a reference field. Anyone who can edit a dashboard can set up one such filter to follow another on that dashboard, in a direct connection. Users with the analytics\_filter\_admin role can also create such filters in the filter library. For more information, see the example in [Configure a Single/Multiple select or cascading filter](create-select-filter-workspace.md).

If the values on each filter can refer to multiple values on the other filter \(a many-to-many relationship\), you have to select a connecting table. This connecting table has a unique record for every possible reference between the two filters. The connecting tables between two tables are defined in the Collection \[sys\_collection\] and Many to Many Definition \[sys\_m2m\] tables. Only administrators can access these tables.

Connection tables come predefined for any relevant tables included in the base system or in Platform Analytics Solutions. However, if you want to use a custom table in a many-to-many relationship, you must define that relationship in the Many to Many Definition table. For more information, see [Create a many-to-many table relationship](https://www.servicenow.com/docs/access?context=t_CreateAManyToManyRelationship&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Add at least two single or multiple select filters to the relevant dashboard.

    For more information about adding filters to a dashboard, see [Create or add a filter on an inline dashboard](select-workspace-filter-type.md).

2.  Put the dashboard in Edit mode.

3.  Open the configuration menu for the filter that you want to follow the other filter.

    If the filter can follow any other filters on the dashboard in a many-to-many relationship, these filters are listed under **Filters with table connection** in the **Other filters to follow** section.

    ![Toggles for two filters under Filters with table connection.](../image/m2m-filter-toggles.png)

4.  Turn following on for the filters that you want this filter to follow.

5.  If no connecting table has been selected for that filter, a dialog opens to select the connecting table.

    The Table icon by the toggle is grayed out when no connecting table has been selected yet.

    ![Table symbol showing that the connecting table has not been selected yet.](../image/m2m-filter-conn-table-not-selected.png)

    After you set the connecting table, you can select the table icon to change it.

    If you have the choice between more than one connecting table, the names of the connecting tables should suggest which one to select. For example, Excluded Users \[sys\_user\_license\_exclude\] filters on users who don’t have a subscription whereas User Subscription \[sys\_user\_has\_license\] filters on users who do.

    ![Selection of two possible connecting tables.](../image/m2m-filter-select-connecting-table.png)

6.  Save the dashboard and exit editing mode.


