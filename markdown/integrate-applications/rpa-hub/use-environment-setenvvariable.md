---
title: Use the SetEnvironmentVariable component
description: Create an environment variable as part of an automation Workflow by using the SetEnvironmentVariable component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Environment, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the SetEnvironmentVariable component

Create an environment variable as part of an automation Workflow by using the SetEnvironmentVariable component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the SetEnvironmentVariable component. For more information about these properties, see [Properties of the Environment components](../reference/util-environment-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Environment**.

2.  Drag the SetEnvironmentVariable component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SetEnvironmentVariable component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(variable\)|Takes the environment variable name from a previously executed component.|Yes|
    |Data In \(value\)|Takes the environment variable value from a previously executed component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Environment](../concept/environment-utility.md)

