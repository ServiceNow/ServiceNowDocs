---
title: Edit a page
description: Edit a page to change the page name, path, and parameters.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Edit a page

Edit a page to change the page name, path, and parameters.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Edit page settings to change the name, path, and type of your page. This is useful if you decide this information should be changed after you create the page. If your page is in a different application scope, you can choose to edit it in the original scope.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open the experience with the page that you want to edit.

3.  Next to the page that you want to edit, select the More actions icon ![](../../task-table/image/MoreActionsIcon.png) then **View settings**.

    ![View settings selected within the More actions menu.](../image/edit-page-settings-link.png)

4.  In the page settings window you can change the name, path, type, and parameters of your page.

    ![Page settings screen with page parameters help text highlighted.](../image/edit-page-settings.png)

5.  Add required parameters to your page URL.

    1.  Click **+ Add**.

    2.  Enter the required parameters for your page.

        A required parameter is a piece of data that your page requires, such as a sys\_id, table, or query. Required parameters are useful for components, because they can bind to the value of the required parameter.

        ![Required parameters in page settings.](../image/required-parameter-settings.png)

        For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

6.  Add optional pieces of data that you want to add to the URL of your page.

    1.  Click **+ Add**.

    2.  Enter the optional parameters for your page.

        Unlike required parameters, optional parameters are always name and value pairs that work no matter what order that they are provided in.

        ![Optional parameters in page settings.](../image/optional-parameter-settings.png)

        For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

7.  Click **Save**.


**Parent Topic:**[Manage UI Builder pages and page variants](../concept/work-pages.md)

