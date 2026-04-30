---
title: Add the Universal Task list category in Service Operations Workspace Core
description: Add the Universal Task list category to the new Service Operations Workspace Core so that agents can access and navigate through various modules directly from the new workspace.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Universal Task, Universal Task, Employee Service Management]
---

# Add the Universal Task list category in Service Operations Workspace Core

Add the Universal Task list category to the new Service Operations Workspace Core so that agents can access and navigate through various modules directly from the new workspace.

## Before you begin

Role required: admin

## About this task

Due to the deprecation of the old service operations workspace, the Universal Task category listing isn’t displayed in the new workspace. To display the relevant modules, you can manually add records to the table sys\_ux\_list\_category.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **UX List Categories** &gt; **Show List**.

    To access the list directly, you can use the navigation search bar and perform a search by using the table name sys\_ux\_list\_category.list.

2.  Insert records in the sys\_ux\_list\_category table by selecting **New**.

3.  On the form, fill in the fields.

    For more information, see [.](https://www.servicenow.com/docs/access?context=ux-list-category-form&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

4.  Select **Submit**.


## Result

The Universal Task list category is added to the Service Operations Workspace Core.

-   **[Add lists under the Universal Task list categories](add-universal-task-lists-under-list-categories.md)**  
Add lists under the newly created Universal Task list category in Service Operations Workspace so that agents can access these modules from the new workspace.

**Parent Topic:**[Using Universal Task](../concept/use-universal-task.md)

