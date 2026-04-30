---
title: Open state management
description: The open state model is a programmatic framework in the Configuration State Model API, which lets you program variations in product options that appear in the product configurator in Sales Customer Relationship Management. The API framework provides certain states and helper API methods for controlling how nodes in the product configurator user interface are displayed.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Setting up the product configurator, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Open state management

The open state model is a programmatic framework in the Configuration State Model API, which lets you program variations in product options that appear in the product configurator in Sales Customer Relationship Management. The API framework provides certain states and helper API methods for controlling how nodes in the product configurator user interface are displayed.

As developers, you can use [extension points for open state management](../task/som-open-state-configuration.md) to set the view-only or editable states on any configurator node, based on events that occur at loading or when product selections change. You can also optionally script information messages along with changing the state of the node. These messages display contextually in the Product Configurator user interface. Various helper API methods are available for reading and setting states on any node, eliminating the need for extensive JSON scripting.

**Note:** Check your entitlements to determine if you have access to these features.

## Use cases for configuration state management

The following table shows different ways that you can control the product options displayed in the product configurator.

|Product configurator use case|Example|
|-----------------------------|-------|
|Hide certain options for a customer|A product attribute selection isn’t displayed for customers in California due to state safety regulations​.|
|Set certain default options for a customer|For upgrades, only the Ultimate plan is displayed for existing customers who have a premium plan.|
|Allow only certain options to be selected based on other attribute options|For certain products such as laptops, display all sizes 13", 15", and 17", but display only 15" and 17" laptops if only the touchscreen feature is required.|
|Allow quantity to be set for products|Some products might have different default quantity values. Allow agents to configure the quantity as long as the value is within the bounds of a minimum quantity and maximum quantity allowed for that product.|
|Allow only certain characteristic selections to be made|Certain product selections require a particular characteristic value to be chosen. For example, upon selection of the Ultimate Internet Plan, the connectivity speed that can be chosen is 5G.|

You can manage the display of options in the product configurator by using the Configuration State Model API Framework.

## Node states

Nodes in the product configurator display product relationship groups, child products, and characteristic options. Nodes can have the following states:

-   **Visible - Yes \(make node visible\) or No \(make node invisible\)**

    Configurations that are visible or not visible to the agent in the product configurator. Options might not be visible if they're incompatible with other selections made by the agent. For example, for a particular car wheel size, incompatible tire options are not visible.

-   **Editable - Yes \(show node and make it selectable\) or No \(show node but make it unselectable\)**

    Configurations that are editable or not editable by the agent in the product configurator. Agents can personalize certain aspects of the product while maintaining constraints that are necessary for the product. For example, for a specific car model, only compatible exterior colors are editable.

-   **Quantity - Visible \(Yes/No\), Editable \(Yes/No\)**

    Configurations that set quantity on a product, enforce rules related to quantity, and show informational and error messages related to quantity at the appropriate node.

-   **Checked - Yes \(show node selections\) or No \(make node selections invisible\)**

    Configurations that show the configuration options for selection based on the context.

-   **Value - Visible \(Yes/No\), Editable \(Yes/No\)**

    Configurations that set a value for a characteristic, enforce rules related to the characteristic, and show informational or error messages related at the appropriate node.


**Note:** Agents can choose to set messages at a node level to provide justification for a state change.

## Events

Manage node states using the Configuration State Model API Framework. Activate these states by using the following two events in the Events Framework of the Configuration State Model:

-   On Load - The state \(visibility, editability\) of each node is initially set to Yes \(true\). The open state is invoked on loading.
-   On Change - This function is called whenever there’s a change in a node's value in the product configurator user interface. However, this state isn’t invoked when quantity changes occur in the product configurator. These states can be set programmatically in one of the following ways: on-load, during selections, or just before the instance is synchronized back to the transaction

## Helper API methods

You can use the following helper API methods to read and set states on any node.

-   **Apply states**

    Set the visible and editable states for product relationship groups, product characteristics, and product characteristic options using Getter and Setter methods to read and change the state of the configuration model.

-   **Getter methods**

    Obtain node paths along with the states on any configuration node:

    -   getAllNodes\(\): Returns JSON with node path \(reference to code\) and its respective relative path with all the states.
    -   getNode\(nodePath\): Returns javascript object of the node for the specified node path if it exists.
    -   getNodeDetails\(nodePath: Return all the states for the specified node path if it exists.
-   **Setter methods**
    -   Set the visible and editable states for product relationship groups, product characteristics, and product characteristic options.
        -   setVisible: True/False at all levels
        -   setVisible\(True/False\)
        -   setEditable: True/False at all levels
        -   setEditable\(True\)
        -   Implementation example:

            ```
            var newHandler = configInstance.getNode(nodePath);
            newHandler.setVisible(true, “This is a sample message for setVisible”);
            newHandler.setEditable(false, “This is a sample message for setEditable”);
            ```

    -   Set the quantity for offers and specifications. The nodePath determines the product, and the value is the quantity to be set.
        -   setQuantity\(value\);
        -   Implementation example:

            ```
            var newHandler = configInstance.getNode\(nodePath\);
            newHandler.setQuantity\(value, “This is a sample message for setQuantity”\);
            ```

    -   Set the configuration options to see what is being selected.
        -   setChecked \(value\); True/False
        -   Implementation example:

            ```
            var nodePath = “QUADPLAYHO1/OPTIONALPRODUCTS/CONNECTEDC2/CONNECTEDC1/VIN”
            var newHandler = configInstance.getNode\(nodePath\);
            var newHandler.setChecked\(true, “This is a sample message for setChecked”\)
            
            ```

    -   Set the value for a characteristic node where the input type is a single line of text.
        -   setValue\( value\);
        -   Implementation example:

            ```
            var nodePath =
            “QUADPLAYHO1/OPTIONALPRODUCTS/CONNECTEDC2/CONNECTEDC1/VIN”
            var newHandler = configInstance.getNode(nodePath);
            newHandler.setValue(“9TKN332”, “This is a sample message for
            setValue”);
            ```

-   **Getter context variable methods**

    Retrieve context variables inside the product configurator user interface.

    -   getHeaderContextVariables\(\): Returns a list of all the header context variables.
    -   getHeaderContextVariableValue\(contextVariable\): Returns a value and the display value of a specific context variable in the header.
    -   getLineContextVariables\(\): Returns a list of all the line context variables.
    -   getLineContextVariableValue\(nodePath, contextVariable\): Returns the value of a specific context variable in the line.

