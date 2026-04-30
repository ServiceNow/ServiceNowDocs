---
title: Use the Expression component
description: Perform mathematical and logical operations with various operands and operators using the Expression component in RPA Desktop Design Studio. The Expression component supports multiple operators and functions for you to use.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Expression component

Perform mathematical and logical operations with various operands and operators using the Expression component in RPA Desktop Design Studio. The Expression component supports multiple operators and functions for you to use.

## Before you begin

Role required: none

## About this task

You can combine Expressions with operators with each operator having a priority. The priorities of the operators are given.

1.  Primary
2.  Unary
3.  Power
4.  Multiplicative
5.  Additive
6.  Relational
7.  Logical

The Expression component supports multiple functions. See [Supported functions for the Expression components](../reference/supported-expression-functions.md).

You can configure the properties for the Expression component.

|Property|Description|
|--------|-----------|
|Delay After Execution|The number of seconds to pause after running.|
|Delay Before Execution|The number of seconds to pause before running.|
|Enable Timeout|Option to set a timeout value.|
|Timeout|Number of seconds that the operation ends after if not completed. To apply this value, you must set the **Enable Timeout** property.|

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Expression**.

2.  Drag the Expression component to the Design surface.

3.  Double-click the light-yellow colored field and enter the expression.![Edit-Expression-field.](../image/expression-field-edit.png)

    A Data In port is dynamically added for each operand. For example, if you enter the expression X+Y, then two Data In ports are added for "X" and "Y". The Data In ports accept values for the operands.

4.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

5.  Connect the data and control ports of the Expression component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data in|The name of the port is the same as the name of the operand. For example, if X is the operand, then the port name is "X".|String|Takes the value of the operand.|No default value.|Yes|
    |Data out|Result|Object|Returns the result of the expression.|Not applicable|Not applicable|

6.  To test the component, right-click the component bar and then click **Run From Here**.


## Expression component performs a mathematical operation between two operands

![Mathematical operation between two operands.](../image/Expression_False.PNG)

In the example, the Variable component passes the integer values for the two operands "i" and "j" set in the Expression component. The Expression component takes the values and finds whether the value of i&gt;=j. The result is passed to the Decision component. The Decision component passes the result to the Show component. In the example, since the value of "i" is lesser than "j", the Show component shows "False" in a message box.

**Parent Topic:**[General](../concept/general-component.md)

