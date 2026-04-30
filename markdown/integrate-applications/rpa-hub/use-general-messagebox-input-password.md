---
title: Use the Input Password component
description: Set up a password input form by using the Input Password component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Input Password component

Set up a password input form by using the Input Password component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The Input Password component is used in Attended Robot automations.

To configure the properties for the Input Password component, see [Properties of Confirm components](../reference/Properties-general-components.md#confirm-components).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **MessageBox**.

2.  Drag the Input Password component to the Design surface.

3.  To provide inputs to the parameters, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Input Password component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data in|Message|String|Takes the heading of the password from a previously executed component.|No default value|No|
    |Data out|Return|Secured String|Returns the password entered in the form as a secured string.|Not applicable|Not applicable|

5.  To test the component, right-click the component bar and click **Run From Here**.


**Parent Topic:**[General](../concept/general-component.md)

