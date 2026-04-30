---
title: Replace a tab with a viewport-enabled tab
description: Convert a tab on a page to a viewport-enabled tab. Use viewport-enabled tabs to display third-party custom data, assign audiences, and create variants.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Extend your UI experience with viewport components, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Replace a tab with a viewport-enabled tab

Convert a tab on a page to a viewport-enabled tab. Use viewport-enabled tabs to display third-party custom data, assign audiences, and create variants.

## Before you begin

Role required: admin

## About this task

Replace your tab or tabs with viewport-enabled tabs.

**Note:** Replacing a tab with a viewport-enabled tab is a permanent and one-way process. You lose any existing tab content and must recreate the viewport tab content.

![Replace with viewport tabs confirmation.](../image/viewport-replace-with-tabs-warning.png)

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  Create or open a page with existing tabs, or add a **Tabs** component to your page.

    ![Tabs component.](../image/tabs-component-toolbox.png "Tabs component")

    For more information on how to add a Tabs component to a page, see [Add tabbed content to UI Builder pages](tabs-components.md#).

4.  Select the tabs component that you want to replace with viewport tabs in the content tree.

5.  Select **Replace with viewport tabs** in the configuration panel.

    **Note:** Replacing a tab with a viewport-enabled tab is a permanent and one-way process. You lose any existing tab content and must recreate the viewport tab content.

    ![Replace with viewport tabs option.](../image/viewport-replace-tabs-button.png)

6.  Select **Replace with viewport tabs**.

    ![Replace with viewport tabs confirmation.](../image/viewport-replace-with-tabs-warning.png)

7.  Click **Edit content** to add a viewport-enabled tab.

    ![Arrow pointing to the edit content button in the configure tab.](../image/viewport-replace-tabs-edit-content.png "Edit content")

    For more information on viewport components, see [Add a viewport component to your page](work-with-viewport-components.md).

8.  Select **Save and continue**.

    The sub-page overview page appears.

9.  Select **Create new page.**

10. In the **Name** field, enter a name for your viewport-enabled tab.

11. Keep the default path, or change it to your preference.

12. Select **Continue**.

13. In the **Name** field, enter a name for the page variant or leave it as **Default**.

14. Add one or more audiences for this page.

    If an audience you need is not listed, you can choose the **View all available audiences** to create one.

15. Declare conditions for when to display the page or tab by either using the provided dropdown menus or writing an encoded query string.

    For more information on writing encoded queries, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

16. Select **Open in editor**.

17. Add components to your tab as you would to a page.

18. Add an event handler to any components to make them perform actions, such as loading page content.

    For more information about event handlers, see [Manage actions in UI Builder pages](work-events.md).

19. Select **← Back to \(name of page\)** to return to your original page.

    ![Arrow pointing to Back to Default link in the UI Builder header.](../image/viewport-replace-back-to-default.png)

20. In **Data driven tabs**, select a data source to bind data to your viewport-enabled tab using data resources to dynamically expose your data from tables and records.

    You then bind these data properties to components in your tab. For more information about using data resources, see [Dynamically expose data in UI Builder pages \(advanced feature\)](data-resources.md).

    ![Arrow pointing to the data drive tabs field.](../image/viewport-tabs-data-source.png)

21. Choose where the viewport-enabled tab labels appear on the page and decide whether to hide tab labels so you only see the icons.

    ![Set max width or hide tabs](../image/UIB-tabs-config-span-hide.png)


**Parent Topic:**[Extend your UI experience with viewport components](viewports-overview.md)

