---
title: Create a page in UI Builder
description: Create a page in UI Builder for a portal, workspace, or custom application so that you can build a web experience for your users.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a page in UI Builder

Create a page in UI Builder for a portal, workspace, or custom application so that you can build a web experience for your users.

## Before you begin

Role required: ui\_builder\_admin

## About this task

A page has a collection of components that make up a workspace, portal, or custom application user interface \(UI\).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Select the **Create new page** in the center of the screen.

4.  Select **Create from scratch instead**.

    ![Template selection screen with arrow pointing to Create from scratch instead button.](../image/page-create-blank.png)

    You can also create pages using page templates, see [Create a page from a template](reuse-page-definitions.md) for more information.

    **Note:** As of Xanadu Store Release 1, responsive authoring is available when creating a new UI Builder page from scratch. Responsive authoring is not available for existing pages or pages created with a template, however, these types of pages will continue to use the existing, default reflow model. For more information, see [Responsive authoring](../concept/responsive-authoring.md).

5.  Enter a unique name for the page in the **Name** field.

6.  Specify a path for your page in the **URL Path** field. UI Builder generates a default path based on the name that you provided in the previous step.

    A default path is added based on your page name. You can also create your own path. The path is required and must be unique. The path can include digits \(0-9\), letters \(A-Z, a-z\), and a few special characters \(`"-"`, `"."`, `"_"`, `"~"`\), with the words separated by a forward slash or hyphen. The **URL preview** shows the path of your page.

    **Note:** The application scope defaults to the scope that the user is currently in within the ServiceNow AI Platform®. For more information about the application scope, see [Learn about security and roles](security-roles.md).

7.  Select a URL page type in the **Type** drop-down list.

    URL page types help you categorize and find important pages in the experience view. Select from **None**, **Dashboard**, **Knowledge base**, **List**, and **Record** page types. Pages assigned a type other than **None** are filtered more effectively in the experience view.

    **Note:** A landing page is assigned a **Landing** URL type by default.

8.  Select **Continue**.

9.  Add required parameters to your page URL.

    1.  Click **+ Add**.

    2.  Enter the required parameters for your page.

        A required parameter is a piece of data that your page requires, such as a sys\_id, table, or query. Required parameters are useful for components, because they can bind to the value of the required parameter.

        ![Required parameters in UI Builder.](../image/required-parameter-example.png)

        For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

10. Add optional parameters to the URL of your page.

    1.  Click **+ Add**.

    2.  Enter the optional parameters for your page.

        Unlike required parameters, optional parameters are always name and value pairs that work no matter what order that they are provided in.

        ![Optional parameters in UI Builder.](../image/optional-parameter-example.png)

        For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

11. Select **Looks good**.

12. Enter a name for the page variant.

    The form automatically contains **Default** but you can edit the page variant name.

13. Add one or more audiences for this page.

    If an audience you need is not listed, you can choose the Open audiences in platform link to create one.

14. Declare conditions for when to display the page by either using the provided dropdown menus or writing an encoded query string.

    For more information on writing encoded queries, see Encoded query strings.

15. Select **Continue**.

16. Select the **Build responsive** option \(default\) for greater control of how the page appears at different screen form factors or select **Build without responsive** for automatic adjustment.

    ![Step showing responsive authoring and reflow options when creating a page from scratch.](../image/responsive-author-create-page.png)

    For more information, see [Responsive authoring](../concept/responsive-authoring.md).

17. Select **Create** to create your blank page.

    The page opens in Editor view so you can start adding content such as layouts and components. For more information, see [Customize UI Builder pages using components](../concept/work-components.md).


-   **[Create a page from a template](reuse-page-definitions.md)**  
Use a template to create a page based on a pre-defined page template. A page template can help you create pages faster and keep pages consistent within an experience. Page templates may include components, data resources, and a layout.
-   **[Create a page from a legacy template](legacy-templates.md)**  
Use legacy page templates to reuse a page definition, such as record or list page, for pages in your workspace or portal.

**Parent Topic:**[Manage UI Builder pages and page variants](../concept/work-pages.md)

