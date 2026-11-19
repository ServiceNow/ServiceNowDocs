---
title: Edit a page
description: Edit a page to change the page name, path, and parameters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/edit-page.html
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

3.  Next to the page that you want to edit, select the More actions icon \[Omitted image "MoreActionsIcon.png"\] Alt text: then **View settings**.

    \[Omitted image "edit-page-settings-link.png"\] Alt text: View settings selected within the More actions menu.

4.  In the page settings window you can change the name, path, type, and parameters of your page.

    \[Omitted image "edit-page-settings.png"\] Alt text: Page settings screen with page parameters help text highlighted.

5.  Add required parameters to your page URL.

    1.  Click **+ Add**.

    2.  Enter the required parameters for your page.

        A required parameter is a piece of data that your page requires, such as a sys\_id, table, or query. Required parameters are useful for components, because they can bind to the value of the required parameter.

        \[Omitted image "required-parameter-settings.png"\] Alt text: Required parameters in page settings.

        For more information, see [Manage UI Builder pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-pages.md).

6.  Add optional pieces of data that you want to add to the URL of your page.

    1.  Click **+ Add**.

    2.  Enter the optional parameters for your page.

        Unlike required parameters, optional parameters are always name and value pairs that work no matter what order that they are provided in.

        \[Omitted image "optional-parameter-settings.png"\] Alt text: Optional parameters in page settings.

        For more information, see [Manage UI Builder pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-pages.md).

7.  Click **Save**.


**Parent Topic:**[Manage UI Builder pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-pages.md)

