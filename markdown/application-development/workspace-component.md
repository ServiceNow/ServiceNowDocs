---
title: Add a component to Agent Workspace
description: Use custom components to create a custom Workspace interface to fulfill the specific need of your company's agents.Set properties in a configuration file to add your component to the UI Builder in your instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Add a component to Agent Workspace

Use custom components to create a custom Workspace interface to fulfill the specific need of your company's agents.

Communicating with customers through multiple channels can be time consuming. To be efficient in these omni-channel interactions, your agents need a single view of customer information to reduce context switching between multiple tools. By developing custom components for Workspace, your team can bring communications from multiple channels into one interface.

## Adding components to a Workspace

Once deployed to your instance, you can add components to Workspace in these ways.

-   **Add a component to a Workspace modal**

    Use a UI action to launch a custom component in a modal so an agent doesn't have to navigate to a different screen to accomplish a task. For more information, see [Render a component in a modal](https://www.servicenow.com/docs/access?context=declarative-actions-landing&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

-   **Add a component to a Workspace landing page using UI Builder**

    Use the UI Builder to create custom landing pages for your agents. UI Builder is a drag-and-drop tool that lets you visually arrange workspace components. For more information, see [Configuring Configurable Workspace](https://www.servicenow.com/docs/access?context=c_set-up-configurable-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    Configure properties in the `now-ui.json` file to use deployed components in the UI Builder. For instructions, see the [ServiceNow Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/ui-builder).

-   **Add a component to a Workspace record view**

    You can add custom or standard components to the component area in the Workspace record view. For more information, see [Forms](https://www.servicenow.com/docs/access?context=form-configurable-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


**Parent Topic:**[Create custom components using ServiceNow CLI](custom-components.md)

## Add a component to UI Builder

Set properties in a configuration file to add your component to the UI Builder in your instance.

### Before you begin

-   [Set up your environment](../task/set-up-environment.md)
-   [Set up your project](../task/setup-component-project.md)
-   [Develop a component](../task/develop-component.md)

### Procedure

1.  In your project directory, open `now-ui.json`.

2.  Add the `components.[component-name].uiBuilder` object to the file.

    This object adds the component to the UI Builder.

    This object includes these key-value pairs:

    |Key|Data type|Description|
    |---|---------|-----------|
    |components.\[component-name\].uiBuilder|Object|Object that adds the component to UI Builder.|
    |components.\[component-name\].uiBuilder.label|String|Required. The display name of the component in UI Builder.|
    |components.\[component-name\].uiBuilder.icon|String|Required. The name of the icon that appears in UI Builder.|
    |components.\[component-name\].uiBuilder.description|String|Required. A short description of the functionality of the component.|

    ```
    {
      "components": {
        "card": {
          "uiBuilder": {
            "label" : "Card",
            "icon" : "chat-fill", 
            "description" : "A visual card format for a record.",
            "associatedTypes": ["global.core"]
          },
    ```

3.  If your component includes properties, add the `components.[component-name].properties` array to the file.

    This adds the properties as configuration options for the component in UI Builder.

    This object includes these key-value pairs:

<table id="table_vdz_qzb_5kb"><thead><tr><th>

Key

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

components.\[component-name\].properties

</td><td>

Array &lt;Object&gt;

</td><td>

An array of objects that includes all the properties of the component and all relevant information about those properties.

</td></tr><tr><td>

components.\[component-name\].properties\[\].name

</td><td>

String

</td><td>

Name of the property in your component's code.

</td></tr><tr><td>

components.\[component-name\].properties\[\].label

</td><td>

String

</td><td>

Display name of the property to display in UI Builder, if applicable.

</td></tr><tr><td>

components.\[component-name\].properties\[\].description

</td><td>

String

</td><td>

A short description of what the property does or how to use it.

</td></tr><tr><td>

components.\[component-name\].properties\[\].readOnly

</td><td>

Boolean

</td><td>

When true, prevents a user from configuring the property in UI Builder. Default: false.

</td></tr><tr><td>

components.\[component-name\].properties\[\].required

</td><td>

Boolean

</td><td>

When true, the user must configure the property. Default: false.

</td></tr><tr><td>

components.\[component-name\].properties\[\].defaultValue

</td><td>

String

</td><td>

The default value when the user does not provide one.

</td></tr><tr><td>

components.\[component-name\].properties\[\].associatedTypes

</td><td>

Array

</td><td>

Describes where in the UI Builder toolbox the component appears. Value must be `"global.core"`.

</td></tr><tr><td>

components.\[component-name\].properties\[\].typeMetadata

</td><td>

Object

</td><td>

Extra configuration data that some data types require, such as reference properties and choice lists.

</td></tr></tbody>
</table>    ```
    {
      "components": {
        "properties": [
    		    {
    			"name": "backgroundColor",
    			"label": "Background Color",
    			"description": "Background Color",
    			"readOnly": false,
    			"required": false,
    			"defaultValue": "lightgray"
    		    },
    		    {
    		       "name": "cardType",
    			"label": "Type of card",
    			"description": "Type of card",
    			"readOnly": false,
    			"required": false,
    			"defaultValue": ""
    		    }
    			]
    ```

4.  Save the file.


### What to do next

[Deploy a component to an instance](../task/deploy-to-instance.md).

**Related topics**  


[Create custom components using ServiceNow CLI](custom-components.md)

