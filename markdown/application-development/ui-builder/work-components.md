---
title: Customize UI Builder pages using components
description: Learn what a component is in UI Builder. Also, see how components work within UI Builder.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Customize UI Builder pages using components

Learn what a component is in UI Builder. Also, see how components work within UI Builder.

Components are the base elements of your UI Builder page. Components range from core elements like buttons and labels to more complex experience components like lists and forms.

You can add these components to your UI Builder page to build or customize your workspace or portal experience. For example, adding an **Activity stream** component to your page that lets users see their travel request activity.

![Component library showing a list of available components.](../image/components-toolbox-overview.png)

You can add components to your UI Builder page in the following ways.

<table id="addcomponentstable"><thead><tr><th>

Location

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Directly from a page in UI Builder \(option 1\)

</td><td>

Select the add content \(plus\) icon, select the **Components** tab, and then select a component.

 ![Add content icon selected on the stage showing the toolbox window with Components tab selected.](../image/component-add-from-stage.png)

</td></tr><tr><td>

Directly from a page in UI Builder \(option 2\)

</td><td>

On a column layout or component, select the add before \(plus\) or add after \(plus\) icon, and then select a component.

 ![Animation showing how to select the + Add icon on a component and add a component.](../image/component-add-on-stage-plus.png)

</td></tr><tr><td>

From the **Content** tree in UI Builder

</td><td>

In the content tree, select **+ Add content** and then select a component.

 ![Black arrow pointing to + add content option in content tree next to the toolbox window with Components tab selected.](../image/component-add-from-content-tree.png)

</td></tr><tr><td>

From the floating menu above the page in UI Builder

</td><td>

On a column layout or component, select the Menu icon, select **Add before** or **Add after**, and then select a component.

 ![Arrow pointing to the expanded menu on the stage.](../image/component-add-floating.png)

</td></tr></tbody>
</table>## Column layouts in UI Builder

Add column layouts and columns to your UI Builder page first. Then add components to the columns in a column layout to build and customize your page. Think of a column layout as a defined part of the screen where you add components like lists and headings. You can have as many column layouts on a UI Builder page as you want, with as many as six columns in any column layout. Multiple components can be added to a single column. View the structure of your page in the **Content** tree.

![Content tree showing hierarchy of three column layouts with columns containing components including Color picker, Avatar, and Stylized text.](../image/content-tree-layouts.png)

For more information, see [Column layouts](column-layout.md#).

## Configure components in UI Builder

There are three ways to configure a component in the configuration panel.

-   Configure the component properties.
-   Add CSS style overrides.
-   Set up [event handlers](ui-builder-glossary.md#) for the components.

![Configuration panel tabs used to configure, style, and add events to components.](../image/config-panel-tabs.png)

-   **Configure tab**

    Component properties vary based on each component. Component configuration can be simple, as is the case with simple elements like buttons, headings, and labels. Components like lists and forms require significant configuration. For icon and image components, select from a variety of options or use a custom icon or image. You can modify component properties with UI Builder's low-code JSON editor. For more information about configuring components, see [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

    For each property in the component configure tab, you can choose from the following options.

    ![Dynamic data binding and scripting icons are displayed when you hover over a field.](../image/config-panel-hover.png)

    -   Static: Use data from a list, or enter your own data. The data doesn't connect to an external data source.
    -   Dynamic [data binding](ui-builder-glossary.md#): A way to bind a component property to a data resource, page property, or client state.
    -   Script: Enter JavaScript code to populate a property value.
-   **Styles tab**

    You can change the Cascading Style Sheets \(CSS\) styles for individual components. Change color borders, font size, and so on.

-   **Events tab**

    Configure page-level and variant-level [event mappings](ui-builder-glossary.md#). Also add dispatched events and handled events for your variant. The more complex, experience components rely heavily on dynamic data that is provided by a [data resource](ui-builder-glossary.md#). Binding dynamic data to a component is an important feature. You dynamically expose data from tables, records, or other elements on your page. Exposing data enables you to reuse your components. Also, you can point to the configuration fields to see icons data or scripting options for each field.


As you add and configure components on the page, the stage shows your work. If you make changes and the updates do not load on the stage, select the **Open menu** icon and then select **Developer &gt; Reload Stage**. Reloading the stage shows your changes, but does not save them. To save your work, select **Save** at the top right.

![Experience view with Open menu selected showing the Developer and Reload Stage options.](../image/force-stage-reload.png)

## Component Presets in UI Builder

Use [component presets](ui-builder-glossary.md#) to automatically configure components on compatible pages. UI Builder page templates contain controllers that presets use to define component configuration values. For more information, see [Automatically configure components using presets](presets.md#).

![Heading component properties configured by a preset.](../image/preset-list-example.png)

## Component properties sections

Component properties are grouped into sections of similar properties. Open and close sections by selecting the arrows to the right of the property headings. UI Builder admins can select which component configuration properties are displayed or hidden based on UI policies.

![Component property sections expanded to view all available properties.](../image/config-panel-sections.png)

## Component formula editor

Use the UI Builder component formula editor in the configuration panel to bind or modify formulas. You can enter text, data bindings, and/or formulas. Formulas can consist of any combination of the three input types. The component formula editor supports logical, arithmetic, comparison, negation, and functional transform types.

![Component formula editor with an example formula.](../image/component-formula-editor.png)

Each function added to the component formula editor auto-completes. The component formula editor displays a label for each input of the function so you know what parameters each function requires. For more information about the supported functions in the component formula editor, see [Supported functions in the UI Builder component formula editor](../task/add-components.md#).

## Component ID

Use the component ID when you add a script or bind data to the component as a way to reference the component. A component ID is automatically created and is based on the component label when you add a component to a page. You can change the component ID to anything you want, as long as it is unique. Select the name of the component in the configuration panel to see the component ID.

![Component label box where you add or edit a component label that displays in the content tree.](../image/edit-component-label.png)

## Component visibility

Select the eye icon in the configuration panel to set component visibility. Component visibility is based on a property of the component itself, not who is viewing it. You could show or hide a component based on conditions. For example, hiding an image if it has a broken link.

You can set the visibility based on dynamic data binding, or by editing a scripted property value.

Set the **Test value** to test what happens when the visibility is set to true, false, or none.

![Component visibility options in the configuration tab.](../image/component-visibility-options.png)

## Duplicate components

Create an exact copy of a configured component on your UI Builder page except for the name and ID. A duplicated component copies all properties, bindings, and events. For more information, see [Duplicate a component](../task/duplicate-components.md).

![Component menu with arrow pointing to duplicate option.](../image/component-duplicate.png)

-   **[Automatically configure components using presets](presets.md#)**  
Use component presets to automatically configure components on compatible pages.
-   **[Create custom presets for components](../task/preset-builder.md)**  
Create presets to save time and make your component configurations reusable across different experiences.
-   **[Change the default appearance of components](../task/add-styling-to-component.md#)**  
Set the styles for components and wrappers to change the default appearance.
-   **[Enhance accessibility with focus management](../task/focus-management.md)**  
Set focus on specific elements, ensuring users can interact with them effectively using screen readers.
-   **[Duplicate a component](../task/duplicate-components.md)**  
Duplicate a configured component to reuse on a page.
-   **[Dynamically display content with conditional renderers](../task/conditional-renderer.md)**  
Use the conditional renderer component to display content or components based on specified conditions.
-   **[Page collections](page-collections.md)**  
Page Collections are groups of pages that can be used across multiple experiences.
-   **[Change data visualizations in UI Builder](component-hot-swapping.md)**  
Change data visualizations in real time using a drop-down list to preview data in your experience.
-   **[Add tabbed content to UI Builder pages](tabs-components.md#)**  
Use the Tabs component to add tabbed content to pages in UI Builder.
-   **[Add a contextual sidebar](../task/add-contextual-sidebar.md)**  
Add a contextual sidebar to a page with UI Builder to display related content using a vertical tab structure.
-   **[Add forms to UI Builder pages](add-forms-to-ui-builder-pages.md)**  
Use the Form component to add one or more forms to UI Builder pages.
-   **[Create modals in UI Builder](Modals-overview.md)**  
Use modals in UI Builder with components to provide alerts or calls to action for a user. UI Builder comes with modals to save time and effort.
-   **[Extend your UI experience with viewport components](viewports-overview.md)**  
Viewports are specialized components that enable you to extend your experience without needing to own the parent page in UI Builder. You can work with viewports in three ways. You can add a viewport component or a viewport-enabled tab to a page, or add a viewport to the Contextual sidebar component.
-   **[Create popovers in UI Builder](uib-popover.md#)**  
Use popovers on a UI Builder page to overlay contextual information or functionality to help users complete tasks.
-   **[Create modeless dialogs in UI Builder](uib-modeless-dialog.md)**  
Use modeless dialogs on a UI Builder page to add a floating window that enables you to interact with both the window content and the page content below.

**Parent Topic:**[Working in UI Builder](using-ui-builder.md)

