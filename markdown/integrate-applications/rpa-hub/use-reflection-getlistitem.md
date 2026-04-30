---
title: Use the GetListItem component
description: Return items from a list by using the GetListItem component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reflection, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetListItem component

Return items from a list by using the GetListItem component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetListItem component. For more information about these properties, see [Properties of the Reflection components](../reference/util-reflection-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Reflection**.

2.  Drag the GetListItem component to the Design surface.

3.  To set the field that accepts an item from the list, do the following steps.

    1.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

    2.  Click the add index icon \(![Add index icon.](../image/add-image-icon.png)\).

    3.  Update the data type of the index value.

        A Data out port is dynamically created with each index that you add.

    4.  Repeat the steps to add more indexes.

    5.  Click **OK**.

4.  To configure the input field, [Configure port properties](configure-input-port-properties.md).

5.  Connect the data and control ports of the GetListItem component to the corresponding ports of the other components.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data In|Instance|Object|Takes a list item.|No default value|Yes|
    |Data Out|Name of the port is the same as the name of the index value that is created.|Object|Returns the list item.|Not applicable|Not applicable|

6.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Reflection](../concept/reflection-utility.md)

