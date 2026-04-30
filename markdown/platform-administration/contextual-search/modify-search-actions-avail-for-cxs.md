---
title: Modify or disable search actions available for contextual search
description: Modify or disable search actions to restrict the actions that a user can perform on a search result.
locale: en-US
release: xanadu
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Modify or disable search actions available for contextual search

Modify or disable search actions to restrict the actions that a user can perform on a search result.

## Before you begin

Role required: admin

## About this task

The Search Action Configurations related list contains all the available Search actions available for the selected Search context. Search actions can be modified and disabled but not deleted.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  Edit a table configuration record.

3.  In the Search Action Configurations related list, view the list of search actions available for the contextual search.

    ![Search actions displayed in the Search Action Configurations related list.](../image/search-actions-1.png)

    To disable a search action, set the value of **Active** to **false**.

    **Note:** You can't disable the **This helped** action.

    The search actions that you can modify are as follows:

    -   **Action label**: Label on the action button on the preview window. For example, **This helped** or **Attached To Incident**.
    -   **Attachment type**: Method to attach a knowledge article with the record. You can embed a link \(recommended\) to the article or embed a copy of the article.
    -   **Show on new record**: Enables the **Attach** button to appear when you are creating a record. Prior to the London release, the user had to fill out and save the form, then re-expand the related search results to access the **Attach** button.

        **Note:** This option only applies to tables with the Platform UI type. It defaults to **false** to provide a consistent user experience between Platform and Workspace tables.

    ![Search actions highlighted in the search result preview window.](../image/search-actions-2.png)


**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

