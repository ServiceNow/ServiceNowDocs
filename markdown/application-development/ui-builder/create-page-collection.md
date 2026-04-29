---
title: Create a page collection across multiple UI pages
description: Create a page collection to accommodate tabbed content that can be used across experiences.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Page collections, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a page collection across multiple UI pages

Create a page collection to accommodate tabbed content that can be used across experiences.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Use page collections to create tabbed content in your experiences with the Tabs component in UI Builder.

Pages within a page collection don’t have access to the parent page's URL parameters or data resources. You can set conditions for pages in a page collection to define which page to display to certain audiences. Page templates are not supported inside a page collection.

## Procedure

1.  Click **Create** &gt; **Page collection**.

2.  On the form, fill in the fields.

<table id="table_s4y_ryn_15b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to track your page collection internally.

</td></tr><tr><td>

App shell UI

</td><td>

Type of app shell UI that you want to use with the page collection. The app shell is the wrapper of the page contents, which is similar to the functionality of a web page. The app shell can show things like the logo of your company, user preferences, and the search icon. For more information, see [Define UI experiences using app shells](../concept/app-shells-uibuilder.md).

</td></tr><tr><td>

Component

</td><td>

Select the component that will use the page collection. Page collections can be used with the following components:-   Viewports
-   Viewport Modals
-   Tabs


</td></tr><tr><td>

Description

</td><td>

Short description to help find your page collection. Write a description that helps page builders understand what content is included in the page collection.

</td></tr></tbody>
</table>3.  Click **Next**.

4.  Select a controller to connect data to your page collection.

    If the controller you selected depends on another controller, you will need to add both.

5.  Enter a label in the **Label** field.

6.  Enter a unique Id in the **Id** field.

7.  Click **Create**.

8.  Click **Create new page**

9.  Enter a unique name for the page in the **Name** field.

10. Specify a path for your page in the **Path** field. UI Builder generates a default path based on the name that you provided in the previous step.

    **Note:** The application scope defaults to the scope that the user is in. For more information about the application scope, see [Learn about security and roles](security-roles.md).

11. Click **Continue**.

12. Add one or more audiences for this page.

    If an audience you need is not listed, you can choose the Open audiences in platform link to create one.

13. Add one or more conditions for this page.

14. Select the **Build responsive** option \(default\) for greater control of how the page appears at different screen form factors or select **Build without responsive** for automatic adjustment.

    ![Step showing responsive authoring and reflow options when creating a page from scratch.](../image/responsive-author-create-page.png)

    For more information, see [Responsive authoring](../concept/responsive-authoring.md).

15. Add more pages to your page collection.


**Parent Topic:**[Page collections](../concept/page-collections.md)

