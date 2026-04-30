---
title: Bind data to UI Builder pages using controllers \(advanced feature\)
description: Controllers simplify the linking of data and event logic to enable component presets in UI Builder.Add a data controller to your page to use component presets.Configure a controller to pull data from a table.Delete a controller that you no longer need in UI Builder.The controller public API defines the output data that a controller provides to a preset. This includes the property values and handled events used by a component when a preset is selected. Property and event information is available to view in UI Builder.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Bind data to UI Builder pages using controllers \(advanced feature\)

Controllers simplify the linking of data and event logic to enable component presets in UI Builder.

Controllers enable page builders to easily connect data and scripts to their pages in UI Builder. A controller is a type of data resource that [component presets](ui-builder-glossary.md#) use to bind data to components. Controllers differ from other data resources in that they contain data and event logic that enables presets for components. A controller brings data from the server to a component, and it brings updated data back to the server based on interactions with the component. For more information about component presets, see [Automatically configure components using presets](presets.md#).

Controllers are added by default when you use a UI Builder page template. You can add controllers to UI Builder pages without a controller within the data resources drawer or by selecting a component preset after adding a component to a page. You can view which controllers are configured on your page by opening the data resources drawer.

![List controller added with the List Page Template.](../image/controller-data-shelf-example.png "Controller in the Data resource drawer")

## Types of data controllers in UI Builder

-   **Data controllers**

    Data controllers decide what information should be displayed on UI Builder pages. Data controllers use data resources to sync information in real time and update data/tables when a user inputs information. You can manually add data controllers to a page.

-   **UI controllers**

    UI controllers are added to pages when using UI Builder page templates and cannot be added manually.


## Using controllers with presets in UI Builder

You can add multiple controllers to a UI Builder page, but you can't use the same one twice. If you try to use a component preset that needs a controller, UI Builder prompts you to add it.

Not all components work with controllers, but you can easily see which ones do in the component library. If you have a controller configured on your UI Builder page, you can open the component library to view which components have presets. Components with presets available are highlighted in the component library.

![Highlighted components with preset label.](../image/presets-highlighted-components.png "Components with presets")

**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](data-resources.md)

## Add a controller

Add a data controller to your page to use component presets.

### Before you begin

Role required: admin

### About this task

The record controller is the only controller that you can add to a page in Yokohama.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](work-experiences.md).

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](../task/create-page.md).

4.  Select the **+** icon in the data resource drawer.

5.  Select **Data resource**.

    ![Add a Data resource option.](../image/data-resource-open.png)

6.  Enter `form` in the search field.

7.  Select the controller you would like to add to your page.

8.  Select **Add**.

    ![Select the form controller to add it to the page.](../image/controller-add-button.png)

9.  Fill in the fields to configure the controller.

    ![Controller configuration modal.](../image/controller-apply-button.png)


### Result

The form controller displays in the **Data resources** section.

![Form controller displays in the data resource section.](../image/controller-add-result.png)

## Edit a controller

Configure a controller to pull data from a table.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](work-experiences.md).

3.  Create or open a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](../task/create-page.md).

4.  Select the controller that you want to edit in the **Data and scripts** drawer.

    ![Arrow pointing to the form controller located in the data resources drawer.](../image/controller-add-result.png)

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|Controller is predefined as the type for all controllers.|
    |Table|Add a table that you want the controller to pull data from.|
    |Sys ID|Enter the unique identifier for a record, provide a value, or use -1 to generate a new value.|

6.  Close the edit controller modal.

7.  Select **Save**.


## Delete a controller

Delete a controller that you no longer need in UI Builder.

### Before you begin

Role required: admin

### About this task

Controllers cannot be deleted from pages created with a page template.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](work-experiences.md).

3.  Open the page with the controller you want to delete.

4.  Select the **Menu** icon \(![Menu icon](../image/controller-menu-icon.png)\) next to the controller you want to delete.

    ![Arrow pointing to the data resource menu icon.](../image/controller-open-menu.png)

5.  Select **Delete**.

    ![Arrow pointing to the delete option in the controller menu.](../image/controller-delete-option.png)

    The controller is removed from the local data resource instances.


## View properties and events in the Controller API

The controller public API defines the output data that a controller provides to a preset. This includes the property values and handled events used by a component when a preset is selected. Property and event information is available to view in UI Builder.

The component property values in a preset can be static values or paths to controller output data. You can use the data resource inspector in UI Builder to display the values from the controller data structure used by a preset. To view the payload carried by an event in the preset, you can look in the event handler picker for that event.

### Viewing properties in the Controller API

You can view preset properties in the UIB data inspector. Knowing the available values helps you understand how a component will behave in your design and helps you identify any properties in the preset you might want to override.

This procedure assumes that you have placed a component with a preset on the page and have configured a controller. For instructions, see [Add a controller](controllers.md#).

The configuration tab displays preset property values as a path to the controller output. The base data path is expressed as `@data.<controller_name>`. The remainder of the path is built using the contents of the categories within the controller data hierarchy. You can use this path to view the current values for the record for which the controller has been configured.

![Shows the preset properties expressed as a path to the controller data in the configure panel](../../../build/component-uib-setup/image/controller-api-config-panel.png)

1.  To view the data resources for a component, select the data icon in the lower left sidebar.

    ![Arrow pointing to the data resource icon.](../image/data-shelf-icon.png)

    The three column UIB data inspector appears.

2.  In the first column where the data resources are listed, select the controller whose output you want to view.

    The configuration data for the selected controller appears in the Config tab of the second column. These are the input properties you entered when you configured the controller for the first component with a preset you placed on the page. You can edit these connection values here if you want.

    **Note:** Configuring **-1** for the value in the **Sys ID** field configures the controller for a new record. The controller then generates a full GUID that you can use to store data against the record before it's saved. This allows you to perform actions in a newly created record such as saving attachments.

    ![Shows the user configuration for the Record controller in the data resources panel](../../../build/component-uib-setup/image/controller-api-user-config.png)

3.  Select **top level outputs** in the third column.

    This is the parent level of the controller data hierarchy, indicated with the prefix `@data.`, followed by the controller ID. This combination forms the root path to the data. The data contained in the top level outputs are displayed in the adjacent code field and are available for presets and scripts to use. Other properties at that level are some common properties that apply to all records.

    ![Shows the top level parent category for controller data and how it is used to create the first part of the path to specific data](../../../build/component-uib-setup/image/controller-api-parent-level.png)

    When the preset maps a component property to controller output, the path to the output is shown instead of the value. Paths are denoted as **@data.&lt;controller id&gt;.&lt;path from top level to output property&gt;** and can be used as the values or as part of formula expressions.

    In this example, the mapping in the preset results in a path to `@data.gform.table`.

    ![Shows how the path to a controller output value is derived for a preset property value at the top level](../../../build/component-uib-setup/image/controller-api-top-level-path.png)

4.  To view data below the top level, select the child category indicated by the path in the preset property value.

    The name of the child category appears in the path as `@data.<controller ID>.<category>`. The data from that category is then appended to that path. The root path above the code field indicates the child category being used. In this example, the path to the **View** property in the `form` category is expressed as `@data.gform.form.view`. That preset value displays forms in the **workspace** view.

    ![Shows how the path to the second level of controller data is appended to the base path for the controller in the data inspector](../../../build/component-uib-setup/image/controller-api-second-level-data.png)

    In this example, multiple controller output properties are used in a formula expression to build an object.

    ![Shows how to use multiple controller output properties to build a formula for a property in UI Builder](../../../build/component-uib-setup/image/controller-api-formula-example.png)

5.  To view a scripted property value, select the lock icon next to the property.

    This puts the property into edit mode and opens a modal for editing the script.

    ![Shows the edit scripted property value modal with the mapping to the controller data](../../../build/component-uib-setup/image/controller-api-edit-scripted-value.png)


### Viewing events in the Controller API

You can view handled events mapped to a component by a preset and their payloads in the Events tab in the UI Builder configuration panel. If the data mapping for an event isn't appropriate for your use case, you can add additional data handlers.

**Note:** Data handler mappings provided with the preset are not editable.

1.  Select the Events tab in UI Builder.
2.  To view the mapping for a preset event, select the event tile.

    A modal appears showing the payload properties for the preset event. You can **Disable** the event in this modal.

    ![Selected event showing the modal containing preset values for the event](../../../build/component-uib-setup/image/controller-api-view-preset-event.png)

3.  To add an event handler to the event, select **+ Add event handler** under the event tile.

    ![Shows the control for adding event handlers to a preset event](../../../build/component-uib-setup/image/controller-api-add-event-handler.png)

    A modal appears, showing a list of available, handled events. You can select any action from the list, including an event handler from one of the controllers listed.

4.  Select an event handler from the list and select **Add**.

    The new handler is listed under the event tile.

    ![Shows the event handler that was selected from the list of available handlers added to the event tile](../../../build/component-uib-setup/image/controller-api-new-event-handler.png)


