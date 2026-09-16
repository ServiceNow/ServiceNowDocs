---
title: Adding a Universal Task list category in SOW core
description: Add the Universal Task list category to the new Service Operations Workspace core so that agents can access and navigate through various modules directly from the new workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/universal-task/add-universal-task-list-categories.html
release: zurich
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Universal Task, Employee Service Management]
---

# Adding a Universal Task list category in SOW core

Add the Universal Task list category to the new Service Operations Workspace core so that agents can access and navigate through various modules directly from the new workspace.

## Before you begin

Role required: admin

## About this task

Due to the deprecation of the old service operations workspace, the Universal Task category listing isn’t displayed in the new workspace. To display the relevant modules, you can manually add records to the table sys\_ux\_list\_category.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **UX List Categories** &gt; **Show List**.

    To access the list directly, you can use the navigation search bar and perform a search by using the table name sys\_ux\_list\_category.list.

2.  Insert records in the sys\_ux\_list\_category table by selecting **New**.

3.  On the form, fill in the fields.

    For more information, see .

4.  Select **Submit**.


## Result

The Universal Task list category is added to the Service Operations Workspace core.

-   **[Add lists under the Universal Task list categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/universal-task/add-universal-task-lists-under-list-categories.md)**  
Add lists under the newly created Universal Task list category in Service Operations Workspace so that agents can access these modules from the new workspace.

**Parent Topic:**[Using Universal Task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/universal-task/use-universal-task.md)

