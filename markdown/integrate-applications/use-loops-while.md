---
title: Use the While component
description: Execute a code until a specified condition is true using the While component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Loops, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the While component

Execute a code until a specified condition is true using the While component in RPA Desktop Design Studio.

Watch this video to learn how to use the While component.

How to use the While component 

## Before you begin

Role required: none

## About this task

You can configure the properties for the While component.

|Property|Description|
|--------|-----------|
|Delay After Execution|The number of seconds to pause after running.|
|Delay Before Execution|The number of seconds to pause before running.|
|Delay for each execution \(Seconds\)|Specified delay before each execution of the code while the condition is true.|
|Enable Timeout|Option to set a timeout value.|
|Timeout|Number of seconds that the operation ends after if not completed. To apply this value, you must set the **Enable Timeout** property.|

## Procedure

1.  In the Toolbox pane, navigate to **Loops** &gt; **While**.

2.  Drag the While component to the Design surface.

3.  Double-click the light-yellow colored field \(![Light-yellow-colored-field](../image/expression-field.png)\) under the WHILE component bar.

4.  Enter the condition.

    A Data In port is dynamically added for the parameter that contains the While condition.

5.  Connect the data and control ports of the While component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Purpose of connection

</th><th>

Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

The name of the port is the same as the name of the parameter that defines the condition.

</td><td>

Takes the value of the parameter. The component matches the value with the condition.For example, `i<=10`.

</td><td>

Data In

</td><td>

Object

</td></tr><tr><td>

ControlOut

</td><td>

Use the port at the end of the While Loop to continue to the next action flows.

</td><td>

Control Out

</td><td>

 

</td></tr><tr><td>

LoopPort

</td><td>

Use the port to perform actions inside the While Loop \(such as calculating expressions, logging values, and so on\).

</td><td>

Control Out

</td><td>

 

</td></tr></tbody>
</table>6.  To test the component, under the **DESIGN** tab, click **Run**.


## While component

Drag Variable component before the While component. Add Expression component and MessageBox components after the While component. In the Variable component, enter `1`. In the Expression component, enter `i+1`. Set a Breakpoint at the Expression component. In the While component, enter `i<=10`.

When you run this automation, the value 1 is incremented to 2 and shows in the output, MessageBox, as 2. When you select **Move next** on the Design tab, the value is incremented until 11. Since the condition matches at this point, i&lt;=10, the loop ends and automation is ended.

![While component with Variable, Expression, and MessageBox components showing an automation.](../image/while-loop-example-rpa.png "While component")

**Parent Topic:**[Loops](../concept/loops.md)

