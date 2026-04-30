---
title: Use the ReadFromXPS component
description: Read the data from an XPS file by using the ReadFromXPS component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Reader, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the ReadFromXPS component

Read the data from an XPS file by using the ReadFromXPS component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ReadFromXPS component. For more information about these properties, see [Properties of the Data Reader components](../reference/util-datareader-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Data Reader**.

2.  Drag the ReadFromXPS component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ReadFromXPS component to the corresponding ports of the other components as described in the following table.

    |Parameter|Description|Data Port type|Data type|
    |---------|-----------|--------------|---------|
    |Filepath|The file path of the XPS file.|Data In|String|
    |PageNumber|The page number from the XPS file to read the data from.|Data In|Integer|
    |Data|Returns the extracted data from the XPS file.|Data Out|String|

5.  To preview the data, right-click the **Return** field and click **Preview Data**.

6.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Data Reader](../concept/datareader-utility.md)

