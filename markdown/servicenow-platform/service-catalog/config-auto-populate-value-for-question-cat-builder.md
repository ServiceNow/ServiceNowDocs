---
title: Configure an auto-populate value for a question in Catalog Builder
description: Configure the value of a question to populate automatically whenever the value of another question of the reference type changes.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a question for a catalog item in Catalog Builder, Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure an auto-populate value for a question in Catalog Builder

Configure the value of a question to populate automatically whenever the value of another question of the reference type changes.

## Before you begin

Role required: catalog\_builder\_editor, catalog\_admin, or admin

## About this task

In a catalog item, for example, you can set up the value of the “Name of the manager” question to auto-populate whenever the value of the “Select the requester” question changes.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  Select the **Catalog items** tab.

3.  Select a catalog item and navigate to the **Questions** tab.

4.  Select **Insert new question**.

5.  On the **Questions** tab, do the following:

    1.  In the **Question type** field, select **Choice**.

    2.  In the **Question subtype** field, select **Record reference**.

    3.  In the **Question label** field, enter `Name of the manager`.

    4.  Select the **Read-only** option.

6.  On the **Additional details** tab, in the Source table field, search for and select `User` \(`sys_user`\).

7.  On the **Auto-populate** tab, do the following:

    1.  In the **Select the question this depends on** field, select the reference question that this question depends on.

        For example, select **Select the requester**.

        The list displays all the Reference and Requested For question types that belong to the current catalog item and the associated single-row variable sets.

    2.  To select the field that contains the value that you want to set, select the Select the lookup field icon \(![Select the lookup field icon.](../image/magic-wand-icon.png)\).

        The list shows all the values in the sys\_user table.

    3.  From the list, select **Manager**.

        **Note:** To search any value, enter what you're looking for, for example, `manager` or dot-walk to get the required value.

        For more information about dot-walking, see [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

8.  Select **Insert question**.


**Parent Topic:**[Create a question for a catalog item in Catalog Builder](create-question-cat-builder.md)

