---
title: UI Builder quick start
description: This quick start guides you through the process of creating your first page in UI Builder. Creating your first page is the first step in understanding how to build user interface pages for your workspace or custom portal experiences.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Exploring UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# UI Builder quick start

This quick start guides you through the process of creating your first page in UI Builder. Creating your first page is the first step in understanding how to build user interface pages for your workspace or custom portal experiences.

## Before you begin

Role required: ui\_builder\_admin

In this UI Builder quick start, you perform the following tasks to build your first page in UI Builder:

-   Start UI Builder.
-   Create a page for your workspace or custom portal experience. For more information about creating pages, see [Create a page in UI Builder](create-page.md).
-   Build your page by adding components. For more information about components, see [Customize UI Builder pages using components](../concept/work-components.md).
-   Save your page.
-   Preview your page to see how it looks in a browser.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

    ![Starting UI Builder.](../image/UIB-start-UIBuilder-video.gif "Start UI Builder")

2.  Select an experience that you want to work in from the UI Builder home page.

    If you don’t see any experiences listed in which to work, contact your administrator to get access to an experience, or create an experience. For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Create a page.

    1.  Select the **+** icon in the **Pages and variants** section.

        ![Create page button on the experience view page.](../image/create-page-icon.png)

    2.  Select **Create a new page**.

        ![Page type selection modal.](../image/page-create-popup.png)

    3.  Select **→ Create from scratch instead**.

        ![Create a blank page by selecting Create from scratch instead.](../image/page-create-blank.png)

        You can also create pages using page templates, see [Create a page from a template](reuse-page-definitions.md) for more information.

    4.  Enter `Start Page` as the unique name for the page in the **Name** field.

    5.  Specify a path for your page in the **URL Path** field. UI Builder generates a default path based on the name that you gave in the last step.

        A default path is added based on your page name. You can also create your own path. The path is required and must be unique. The path can include digits \(0-9\), letters \(A-Z, a-z\), and a few special characters \(`"-"`, `"."`, `"_"`, `"~"`\), with the words separated by a forward slash or hyphen. The **URL preview** shows the path of your page.

        ![Page name and path name fields.](../image/create-page-details.png)

        **Note:** The application scope defaults to the scope that the user is currently in within the ServiceNow AI Platform®. For more information about the application scope, see [Learn about security and roles](security-roles.md).

    6.  Select **Continue**.

    7.  Add parameters to your page URL by selecting **+ Add**.

        For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

    8.  Select **Looks good**.

    9.  Enter `Manager Start Page` as the name for the page variant.

    10. Add one or more audiences for this page.

        If an audience you need isn’t listed, you can choose the **Open audiences in the platform** link to create one.

    11. Add conditions for when to display the page or tab.

    12. Select **Continue**.

    13. On the next screen, select **Build responsive**.

    14. Select **Create** to create your blank page.

    Congratulations! You’ve created your first page! The page is empty of content. You add components to the page to build functionality to it. Components are the building blocks of a page. UI Builder comes with many components ready for you to add to your page. Components can be as simple as a **Heading**, or as complex as a **List**.

4.  Select **Editor** to start adding customizing your page.

    ![Arrow pointing to the page editor link.](../image/select-page-editor.png)

5.  Add a container component to your page.

    A container is what holds your components. Think of a container as an area of the page where you add information, images, or functionality \(your components\). You can have as many containers on a page as you want, with as many containers within containers, with as many components in the containers.

    1.  Select **+ Add content** in the content tree.

        ![Pointer selecting +Add content in the content tree.](../image/qs-add-component.png)

    2.  Select the **Single column** layout in the toolbox.

    3.  Select **Column layout 1** in the content tree to highlight the container.

        ![Arrow pointing to column layout 1 in the content tree.](../image/qs-select-column-1.png)

    4.  Select the component name in the configuration panel.

        ![Column layout label and ID fields.](../image/qs-component-label.png)

    5.  In the **Component label** field, type `Container for heading`.

    6.  In the [Component ID](../concept/ui-builder-glossary.md#) field, type `container_for_heading`.

    7.  Select **Apply**.

        See that the column layout name changes to **Container for heading** in the content tree. The content tree is an important concept. The content tree is an easy way to see the structured layout of your page. The content tree is especially important when you have multiple components on your page. You select the component in your content tree to highlight the component on the page, making it easier to build your page. You can do a text search for a component.

        ![Content tree with customized column layout.](../image/qs-content-tree-custom-label.png)

        For more information on component IDs, see [Component ID](../concept/work-components.md#component_id).

    You’ve successfully added your first column layout to your page.

6.  Add a **Heading** component to your column layout.

    You can add components to the page in different ways. For more information on the ways you can add components to your page, see [Add and configure components](add-components.md#).

    1.  Select **+ Add content** in the content tree below the column layout created in step 5.

        ![Arrow pointing to + Add content within the container for heading.](../image/qs-select-add-component.png)

    2.  Type `heading` into the search and select the **Heading** component.

    3.  Select your new **Heading** component in the content tree to highlight it.

    4.  Select **None** in the configuration panel.

    5.  Select the component name in the configuration panel.

    6.  In the **Component label** field, enter `Custom heading` as the unique label for the heading component.

    7.  In the **Component ID** field, enter `custom_heading` as the unique ID for the heading component.

    8.  Click **Apply**.

        ![Arrow pointing to the custom heading label.](../image/qs-add-header-name-id.png)

7.  Customize the heading component.

    1.  Select the heading component in the content tree.

    2.  Select the **Configure** tab in the configuration panel.

    3.  In the **Label** field, enter the text of your heading, such as `My new heading`.

    4.  The Style changes the size of the heading text.

        For example, if you select **Header-secondary**, the text is smaller. Different headings sizes are useful if you have two headings and want the second heading smaller that the primary heading. For more information on configuring components, see [Configure components in UI Builder](../concept/work-components.md#config_components).

    5.  Leave the **Level** as **1**.

    6.  Select **Save**.

    You’ve added and customized a heading component to your page.

8.  Add a second column layout to your page.

    1.  Similar to before, select **+ Add content** in the content tree.

        ![Arrow pointing to + Add content in the content tree.](../image/qs-select-add-column-2.png)

    2.  Select the **Single column** layout in the toolbox.

    3.  Select **Column layout 1** in the content tree to highlight the container.

        ![Content tree with two column layouts.](../image/qs-content-tree-column-2.png)

    4.  Select the component name in the configuration panel.

    5.  In the **Component label** field, type `Container for content`.

    6.  In the **Component ID** field, type `container_for_content`.

    7.  Select **Apply**.

        ![Column layout label and ID fields.](../image/qs-component-label-2.png)

    8.  Select **Save**.

    You’ve successfully added your second container component to your page.

9.  Add an image component to your page.

    An image is a nice way to add a visual for your page. In this quick start, you add a stock photo that comes with UI Builder. But you can add any image that is available to you.

    1.  Select **+ Add content** in the content tree below the container created in step 8.

    2.  Type `image` into the search and select the **Image** component.

        A default image is loaded in the image component. You can add your own image by adding a URL to the image. You can use images hosted on the internet or images in the ServiceNow AI Platform®. If you use an image hosted on an external site, you must use the `https` protocol for security.

    3.  Select the **Image 1** component in the **Content** tree to highlight the image.

        ![Arrow pointing to Image 1 component in the content tree.](../image/qs-content-tree-image.png)

    4.  Select **None** in the configuration panel.

    5.  Select the component name in the configuration panel.

    6.  In the **Component label** field, type `My image`.

    7.  In the **Component ID** field, type `my_image`.

    8.  Select **Apply**.

        ![Image component label and ID.](../image/qs-image-label.png)

    9.  Select **Save**.

    You added an image component to your page.

    ![UI Builder page showing the image component added to the column layout.](../image/qs-image-component-added.png)

10. Select **Preview** in the UI Builder header to preview your page.

    Congratulations! You completed the UI Builder quick start. Your page generates a preview of how it looks in your Workspace or portal experience.

    ![Preview of the page created in the UI Builder quick start procedure.](../image/qs-page-preview.png)


## Result

1.  Created your first page in UI Builder.
2.  Added your first container component to the page. You changed the label for the container.
3.  Added a **Heading** component as a title to the container. You changed the text of the heading. You also changed the label.
4.  Added a second container component to your page. You changed the label for the container.
5.  Added an **Image** component. You changed the label of the image component.
6.  Saved your new page.
7.  Previewed your page in the browser.

You successfully completed the UI Builder quick start!

**Parent Topic:**[Exploring UI Builder](../concept/create-custom-experience.md)

