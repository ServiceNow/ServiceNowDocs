---
title: Create a page collection across multiple UI pages
description: Create a page collection to accommodate tabbed content that can be used across experiences.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Page collections, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a page collection across multiple UI pages

Create a page collection to accommodate tabbed content that can be used across experiences.

## Before you begin

Role required: admin

## About this task

Use page collections to create tabbed content in your experiences with the Tabs component in UI Builder.

Pages within a page collection don’t have access to the parent page's URL parameters or data resources. You can set conditions for pages in a page collection to define which page to display to certain audiences. Page templates are not supported inside a page collection.

## Procedure

1.  Click **Create** &gt; **Page collection**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to track your page collection internally.|
    |Controller|Controller that defines the data for the page collection.|
    |App shell UI|Type of app shell UI that you want to use with the page collection. The app shell is the wrapper of the page contents, which is similar to the functionality of a web page. The app shell can show things like the logo of your company, user preferences, and the search icon. For more information, see [Define UI experiences using app shells](../concept/app-shells-uibuilder.md).|
    |Description|Short description to help find your page collection. Write a description that helps page builders understand what content is included in the page collection.|
    |Application scope|Application scope defines which application that the page collection is part of. To create a page collection in a different application scope, change the application scope in the platform and then create a page collection in UI Builder.|

3.  Click **Create**.

4.  Click **Edit page collection**.

    A new tab opens to the page collection editing screen.

5.  Click **Start editing**.

6.  Click **Create a page**

7.  Enter a unique name for the page in the **Name** field.

8.  Specify a path for your page in the **Path** field. UI Builder generates a default path based on the name that you provided in the previous step.

    **Note:** The application scope defaults to the scope that the user is in. For more information about the application scope, see [Learn about security and roles](security-roles.md).

9.  Click **Create**.

10. Set advanced settings such as required and optional parameters, as well as variant settings.

    1.  Select **Add required parameters** to add any required parameters to your page URL.

        A required parameter is a piece of data that your page requires, such as a sys\_id, table, or query. Required parameters are useful for components, because they can bind to the value of the required parameter.

        ![Required parameters screen in UI Builder.](../image/required-parameter-example.png)

        For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

    2.  Select **Add optional parameters** to add any optional pieces of data that you want to add to the URL of your page.

        Unlike required parameters, optional parameters are always name and value pairs that work regardless of the order they’re provided in.

        ![Optional parameters screen in UI Builder.](../image/optional-parameter-example.png)

        For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

    3.  Click the required or optional parameter in the URL, and in the **Test values** field type a value, such as `incident`.

        You add a test value to your page to populate data into the page as a way to test it. For example, if you add a table as a required parameter, you could add a test value of incident to bring in test data on the incident for that table.

        ![Test value form for UI Builder pages.](../image/test-values.png)

        For more information on test values, see [Test values in a page](../concept/test-value.md).

    4.  Select the **Variant** tab to set the audience and conditions settings for your page.

        When you create a page, UI Builder also creates a variant of the page for you by default. A page variant is a variation of your page at the same path that lets you target experiences for different audiences using user criteria. For example, a page for managers, and a variant of that page for the manager's direct reports. For more information about creating a variant, see [Create a page variant](create-variant.md).

        ![Default variant settings page in UI Builder.](../image/create-page-variant-default.png)

        For more information about audiences, see [Learn about audiences](../concept/add-audiences.md).

    5.  Click **Done**.

11. Click **Done**.

12. [Add and configure components](add-components.md#) on your page.

13. Click **Save**.

14. Add more pages to your page collection.

    1.  Click **Menu**.

    2.  Select **Create page**.

    3.  Repeat steps 6 through 13.

15. Close the page collection window.


**Parent Topic:**[Page collections](../concept/page-collections.md)

