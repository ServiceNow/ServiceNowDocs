---
title: Use the For Loop component
description: Execute a code recurrently to perform tasks of repetitive nature with the For Loop component in the RPA Desktop Design Studio. The For Loop is a control flow component for specifying iterations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Loops, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the For Loop component

Execute a code recurrently to perform tasks of repetitive nature with the For Loop component in the RPA Desktop Design Studio. The For Loop is a control flow component for specifying iterations.

## Before you begin

Role required: none

## About this task

You can configure the properties for the For Loop component.

|Property|Description|
|--------|-----------|
|Delay After Execution|The number of seconds to pause after running.|
|Delay Before Execution|The number of seconds to pause before running.|
|Delay for each execution \(Seconds\)|Specified delay before each execution.|
|Increment By|Specified number by which the component increments the values. For example, if the number is 2 and the loop is from 1 through 10, then the numbers are 1, 3, 5, and so on.|
|Enable Timeout|Option to set a timeout value.|
|Timeout|Number of seconds that the operation ends after if not completed. To apply this value, you must set the **Enable Timeout** property.|

## Procedure

1.  In the Toolbox pane, navigate to **Loops** &gt; **For Loop**.

2.  Drag the For Loop component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the For Loop component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data In|From|Integer|Takes the starting value of the For Loop counter.|Not applicable|Yes|
    |Data In|To|Integer|Takes the end value of the For Loop counter.|Not applicable|Yes|
    |Data Out|Index|Integer|Passes the current value of the For Loop counter to the next component.|Not applicable|Yes|
    |Control Out|Loop|Not applicable|Passes the iteration to the next component.|Not applicable|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Loops](../concept/loops.md)

