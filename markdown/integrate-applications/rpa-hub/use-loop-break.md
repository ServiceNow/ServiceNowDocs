---
title: Use the Break component
description: Break a loop at any time with the Break component in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Loops, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Break component

Break a loop at any time with the Break component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Break component.

|Property|Description|
|--------|-----------|
|Delay After Execution|The number of seconds to pause after running.|
|Delay Before Execution|The number of seconds to pause before running.|
|Message|Custom message for the user.|
|Enable Timeout|Option to set a timeout value.|
|Timeout|Number of seconds that the operation ends after if not completed. To apply this value, you must set the **Enable Timeout** property.|

## Procedure

1.  In the Toolbox pane, navigate to **Loops** &gt; **Break**.

2.  Drag the Break component to the Design surface.

3.  Connect the control port of the Break component to the corresponding port of the another component as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Control In|Control In|Not applicable|Takes the input from another component when the defined condition is fulfilled.|Not applicable|Yes|

4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Loops](../concept/loops.md)

