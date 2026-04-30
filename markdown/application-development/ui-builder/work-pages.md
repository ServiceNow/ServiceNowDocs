---
title: Manage UI Builder pages and page variants
description: Learn what a page is in UI Builder. Understand the building blocks of a UI Builder page, such as column layouts and components.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 14
breadcrumb: [Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Manage UI Builder pages and page variants

Learn what a page is in UI Builder. Understand the building blocks of a UI Builder page, such as column layouts and components.

## UI Builder quick start

Create pages in UI Builder as part of a workspace or custom portal experience. UI Builder pages consist of layouts and [components](ui-builder-glossary.md#). You build a page using column layouts and components to guide a user through an experience. For example, you could build a page to manage travel requests for your employees. The page could have column layouts with components that contain lists of all travel requests submitted and approved. You can add buttons that let users add and submit travel requests. The way you build your page is limitless.

**Note:** One developer should work on any one [variant](ui-builder-glossary.md#) at a time.

## Column layouts and components in UI Builder

Column layouts and components are the building blocks of your UI Builder page. Add column layouts and components to your page to build or customize your workspace or portal experience. For example, add a column layout and within a column place a button component that lets users submit requests.

You can add column layouts, columns, and components, as well as navigate between them, from the stage or the Content tree.

A column layout can contain one or more columns. Columns can contain components. Change the visual styling of column layouts, columns, and components to make it your own experience.

|Type|Description|
|----|-----------|
|Column layout|A flexible container with one to six columns. Add column layouts to provide structure and a framework for a page.|
|Column|Fill columns with components.|
|Component|Base elements of a page, such as buttons, lists, and forms.|
|[Modal](ui-builder-glossary.md#)|Use a modal to create a page type in UI Builder that renders on top of the page and requires action.|
|[Popover](ui-builder-glossary.md#)|A popover is a type of container that appears above a UI Builder page when triggered by an event. Use the popover component to display additional information or actions related to the page.|

See [Customize UI Builder pages using components](work-components.md) for more information.

## Create a UI Builder page

Create a UI Builder page to build a page experience from scratch or use a page template. Build a page one component at a time. If you use one of the pre-defined page templates, you start from a base structure and can customize it to meet your needs.

Name your UI Builder page. Set the path \(or keep the default path that is automatically added based on your page name\). A default path is added based on your page name. You can also create your own path, but the path must be unique. The **URL preview** shows the path of your page.

The application scope protects applications by identifying and restricting access to application files and data. The application scope defaults to the scope that the user is currently in within the ServiceNow AI Platform®. For more information about application scope, see [Learn about security and roles](../task/security-roles.md).

Use a UI Builder page template to create a page based on a pre-defined page template, and then customize the page to your needs. You can reference or copy a page template. For more information, see [Create a page from a template](../task/reuse-page-definitions.md).

![Create page screen where you enter a page name and path. It also shows application scope setting.](../image/create-page-details.png)

## Create a UI Builder page: Advanced settings

Add required parameters to your UI Builder page. A required parameter is a piece of data that your page requires, such as a sys\_id, table, or query. Required parameters are useful for components as they can bind to the value of the required parameter. For example, you can add a table parameter to the URL field and then bind data to that table. When the table is referenced, it exposes the table data to any components on the page. Required parameters are visible in the URL when you add them to your page. In the following example, a required parameter called table was added. Notice it was appended to the URL.

![Parameter called table added to the page. The URL is appended with table.](../image/required-parameter-example.png)

Add optional parameters to your UI Builder page. Optional parameters are optional pieces of data that you can add to the URL of your page. Unlike required parameters, optional parameters are always name and value pairs that work no matter what order they’re provided.

![Edit optional parameters option.](../image/optional-parameter-example.png)

Set the audience and conditions settings for UI Builder page variants. When you create a page, UI Builder also creates a variant of the page for you by default. A page variant is a variation of your page at the same path that lets you target experiences for different audiences using user criteria. For example, a page for managers, and a variant of that page for the manager's direct reports. For more information about creating a variant, see [Create a page variant](../task/create-variant.md).

![Default variant settings page in UI Builder.](../image/create-page-variant-default.png)

For more information about audiences, see [Learn about audiences](add-audiences.md).

## Test values in UI Builder

Add a test value to your UI Builder page as a way to bring test data into the page for testing purposes. For example, if you add a table as a required parameter, you could add a test value of incident and bind a data resource to it to bring in test data on the incident for that table.

![Test value form for UI Builder pages.](../image/test-values.png)

To get test values to show data, add a data resource, then configure the data resource to bind a record to the test value in the URL. For example, you could add `incident` as a test value. Then add a data resource named **Look up a single record**. In the **Table field**, dynamically bind the incident test value to a `context.props.table` table, as shown in the following image.

![Bind incident to table.](../image/test-value-bind-data.png)

## View an existing UI Builder page

You can work in any UI Builder page in your experience based on your role settings. Click on the name of the page you want to work in while in the experience view of your experience.

![Experience view for the Admin Center experience.](../image/experience-view-admin-center.png)

While in the page editor, open a different page variant by selecting the drop-down in the header.

![Drop down option next to Page where you can open another page.](../image/page-drop-down.png)

## Create a UI Builder page variant

A variant lets you target different audiences with different content, using user criteria. For example, you can create a homepage for agents, and a variant of the page for managers that exists at the same URL path.

You set the audience for each UI Builder page variant. The audience determines who uses the page variant. For example, if you create a travel request page, create a variant of that page for managers to manage the employee travel requests. You set the audience for the manager page for anyone in the manager role. Employees cannot view that variant. For more information about audiences, see [Learn about audiences](add-audiences.md).

See [Create a page variant](../task/create-variant.md) for more information.

## Edit UI Builder page settings

Change the settings of your UI Builder page at any time by selecting **Settings** in the UI Builder experience view. You can change the name, path, and parameters of your page after you create a page.

![Arrow pointing to settings link to edit page settings.](../image/edit-page-settings-link.png)

See [Edit a page](../task/edit-page.md) for more information.

## UI Builder Content tree

The content tree in the page management panel is important. It not only shows every column layout, column, and component on your UI Builder page, it lets you easily find your components and work with them. The content tree is especially important when you have multiple components on your page. You select the component in your content tree to highlight the component on the page, making it easier to build your page.

![Content tree with components.](../image/content-tree-sidebar.png "Content tree with components")

When you click a component in the content tree, it highlights the component on your stage so you can configure, add styling, events, data, and so on. You can drag items in the content tree to reorganize your page.

It’s important to add a component label when you add a component to your page. The component label is used in the content tree to apply labels IDs to each component in the content tree. You can identify the components much easier in the content tree when they're labeled appropriately.

![Component label box where you add or edit a component label that shows in the content tree.](../image/edit-component-label.png)

## UI Builder Toolbox

Use the UI Builder toolbox to add layouts and components to your page. Access the UI Builder toolbox by selecting **+ Add content** or the **+** icon in the stage.

![UI Builder toolbox showing basic and advanced layout options.](../image/toolbox-layouts.png)

Search the toolbox to find layouts and components that you want to add to a UI Builder page.

View a brief description of a layout or component by selecting the information icon ![Information icon.](../image/uib-info-icon.png) to view the tooltip. The components tab displays different colors if a component can use a preset or is bundled with multiple components.

![Action bar tool tip explaining what the component is made up of.](../image/toolbox-tool-tip.png)

## UI Builder Stage

The stage is the largest area in the UI Builder editor and is used for building pages. Add your column layouts and components here by either selecting a + button, or dragging from the Component pane to the page.

![The stage of UI Builder where you build your pages.](../image/stage-ui-builder.png)

On the stage, the body, column layouts, and columns are outlined in magenta. Components are outlined in blue.

![Animation showing column layouts and columns displayed on the stage with a magenta outline and components outlined in blue.](../image/stage-colors-video.gif)

Use the Tree item icon to navigate to a different layer of content. For example, if a column is selected, easily navigate to the parent column layout or a component within the column.

![Tree button selected showing hierarchy of column layout, column, and component.](../image/stage-tree-icon-navigate.png)

Select the Menu icon on a column layout or component for options such as duplicate and delete.

![Menu button selected showing additional options.](../image/stage-menu-icon.png)

Changes made on the stage are reflected in the Styles panel at right. Changes made in the Styles panel immediately update the elements on the stage.

## Scale the size of the stage in UI Builder

Adjust the size of the stage in the UI Builder editor by selecting the Width drop-down.

![Width drop-down to resize the page builder window to a specific number of pixels.](../image/stage-resize.png)

## Undo and Redo in UI Builder

Undo and redo changes you've made to your UI Builder page. Reverse any action you make to a page layout, component, style or layout.

The undo and redo function can be found in the header toolbar. You can select the undo \(![Undo button.](../image/undo-button.png)\) or redo \(![Redo button.](../image/redo-button.png)\) button to reverse an action. You can also click the undo drop down to go back multiple steps. You cannot undo and redo changes made in the data shelf.

You can undo the previous 20 actions by selecting the undo drop-down.

![List of changes that can be reversed using the undo drop-down.](../image/undo-drop-down.png)

## UI Builder Configuration panel

Use the configuration panel to work with components, including arranging, styling, and setting up event handlers.

-   Select the **Config** tab to configure components. Each component has different configuration options that let you control the necessary parts of the component. For example, a button component is simple, and you can only configure its appearance, label, and a few properties. A list component is more complicated, and contains dozens of editable list parameters.

    ![Configuration options for a button component, including style, label, disabling text wrap, and hiding the bottom margin.](../image/nav-page-config-panel.png)

-   Select the **Styles** tab in the configuration panel to add styling to a component. You can use standards-based Cascading Style Sheets \(CSS\) to change the visual style of a component. For example, add or change a background color, a border, or any other CSS style.

    ![Styles tab with options such as alignment, sizing, spacing, background, and border.](../image/nav-style-tab.png)

    See [Change the default appearance of components](../task/add-styling-to-component.md#) for more information.

-   Select the **Events** tab to configure events that add actions to your components, pages, data resources, and declarative actions. When you add components to your UI Builder page, they are not configured to perform any action. For example, a button component is static and does not do anything until you bind an event action to it, such as deleting a record.

    ![Events tab in the configuration panel.](../image/nav-events-tab.png)

    See [Manage actions in UI Builder pages](work-events.md) for more information.

-   Column layouts govern how components are arranged on a page. When you add a column layout to a UI Builder page, you can configure how you want the layout designed. After you add a component to a column in the layout, you can configure the elements in more advanced ways. For example, you can justify the content, align items, and set the height, width, margins, background, borders, and padding of your column layout, columns, and components. CSS grid is the most powerful layout system. CSS Grid is built on top of a two-dimensional grid that gives you power over how you create your pages.

    ![Layout options such as alignment, direction, and sizing.](../image/nav-style-tab-container.png)

    See [Organize components in UI Builder pages](work-layouts.md) for more information.


## Open a UI Builder page to preview it

Preview a UI Builder page to see what the page looks like as a web page.

Select the ![Preview this variant.](../image/preview-button.png) button to test the variant that you're currently working on, including modals, viewports, components, data resources, and dynamic data. Previewing a page variant is useful for seeing how it looks and functions while building an experience.

Another method of previewing a page is to request the URL path from the server. Use this method to test if a user sees the variant when they open the page. Select the drop-down arrow next to **Preview** and select **Open URL path** ![Open the URL path for the page.](../image/open-url-path-drop.png) or select **Preview** **&gt; Open URL path** ![Open the URL path for the page.](../image/open-url-path-button.png).

See [Learn how to view and test your UI Builder experience](preview-page-ui-builder.md) for more information.

## Developer editing in UI Builder

From the Menu, edit the UI Builder page as a developer on the platform. This option lets you change the platform-level details of your page and takes you out of UI Builder. You must have the proper role as a developer.

![Menu showing Developer edit options such as open variant collection, open page definition, and open variant record.](../image/nav-developer-menu.png)

-   **[Create a page in UI Builder](../task/create-page.md)**  
Create a page in UI Builder for a portal, workspace, or custom application so that you can build a web experience for your users.
-   **[Edit a page](../task/edit-page.md)**  
Edit a page to change the page name, path, and parameters.
-   **[Add an audience to your UI Builder page](../task/configure-audiences.md)**  
Add one or more audiences to your page or page variant.
-   **[Test values in a page](test-value.md)**  
Add test values to your URL as a way to bring test data into a page.
-   **[Create a page variant](../task/create-variant.md)**  
A page variant in UI Builder is a variation of a page that exists at the same path that targets different audiences using user criteria.
-   **[Responsive authoring](responsive-authoring.md)**  
Use responsive authoring to create UI Builder pages that adjust smoothly to different form factors \(sizes\), such as desktop, tablet, and mobile.
-   **[Learn how to view and test your UI Builder experience](preview-page-ui-builder.md)**  
Preview your experience in UI Builder to see how it looks and functions while building an experience. Previewing helps ensure that your experience works as expected, that the data resources are available, and that the layouts are set up correctly.

**Parent Topic:**[Working in UI Builder](using-ui-builder.md)

