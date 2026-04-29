---
title: Use connector method
description: Expose and then use the methods within a connector to perform all the actions that the connector can do.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use a connector, Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use connector method

Expose and then use the methods within a connector to perform all the actions that the connector can do.

## Before you begin

You must install the connector plugin. To install, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

To navigate to connectors, open an activity.

Role required: None

## Procedure

1.  In the Toolbox pane, navigate to **Connectors**.

2.  Drag a connector under Global Objects in the Project Explorer pane.

3.  Expose the methods, as given.

    Some connectors expose the methods at the connector level while the others expose the methods at multiple levels. For the latter, you must first configure the connector. To find a connector that needs configuration first, right-click the connector and see if the context-menu displays the **Configure** option.

<table id="choicetable_vy3_55j_tsb"><thead><tr><th align="left" id="d452934e89">

Number of levels

</th><th align="left" id="d452934e92">

Step

</th></tr></thead><tbody><tr><td id="d452934e98">

**Connector**

</td><td>

Double-click the connector.

</td></tr><tr><td id="d452934e107">

**Multiple**

</td><td>

1.  Configure the connector to expose all levels.
2.  Double-click the level.


</td></tr></tbody>
</table>    The methods are exposed under the Object Explorer pane.

4.  Drag the method to the Design surface.

    **Important:** You might come across the following behaviours when you drag and drop an automation component from the Toolbox, Object explorer, Project explorer, and Skills explorer to the Design surface:

    -   If you drag and drop a component to the same component in the Design surface, then the new component replaces the existing component. For example, if you already have the **ActionSet** component on the Design surface and you drag and drop another **ActionSet** component to the existing **ActionSet**, then the new version replaces the existing component.

        All the connections \(control and data connections\), variables, or static data associated to the existing component gets associated to the newly dropped component if the port name and the port data type are the same.

    -   If you drag and drop a new component to a different component or method in the Design surface then the new component replaces the existing component.

        All the connections, variables, or static data associated to the existing component gets associated to the newly dropped component if the port names and the port data types are the same.

    -   If you drag and drop a component between two components that are already connected in the Design surface, then the component is placed between the existing components. You may come across the following behaviours when you drag and drop a component between two components:
        -   If port names and the port data types of the newly dropped component match with the connected components, then the data connections are created.
        -   If the port names are the same and the port data types are different, then the data connections are created only if the port data type is can be converted \(the source port data must be converted to target data type. This is known as typecasting or type conversion. For more information on type casting, see [Java Type Casting](https://www.w3schools.com/java/java_type_casting.asp)\). For example, integer to object but not object to integer.
        -   If the port names are the same and the port data type can be converted, but there is already an existing data connection between the two components, then no new data connection is created.

**Parent Topic:**[Use a connector in RPA Desktop Design Studio](use-connector.md)

