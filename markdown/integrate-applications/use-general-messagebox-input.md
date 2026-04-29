---
title: Use the Input component
description: Set up a user input dialog with by using the Input component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the Input component

Set up a user input dialog with by using the Input component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The input component is used in the Attended Robot automation.

To configure the properties, see [Properties of Confirm components](../reference/Properties-general-components.md#confirm-components).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **MessageBox**.

2.  Drag the Input component to the Design surface.

3.  To provide inputs to the parameters, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Input component to the corresponding ports of the other component as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data in|Message|String|Takes the heading of the user input dialog from another component.|No default value|No|
    |Data out|Return|String|Returns the input entered in the form.|Not applicable|Not applicable|

5.  To test the component, right-click the component bar and click **Run From Here**.


**Parent Topic:**[General](../concept/general-component.md)

