---
title: Use the Decision component
description: Automate the decision-making process by using the Decision component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Conditions, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Decision component

Automate the decision-making process by using the Decision component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can specify a conditional expression in the component. If the expression contains any parameters, they appear as input ports. If the expression is correct based on the inputs provided, then the True Output Port takes control. Else, the False Output port takes control and executes the automation.

For defining conditions, the Decision component provides many functions, operators, and expressions. For more information, see [Functions, data types, and operators](../reference/conditions-decision-func-opr.md).

To configure the properties for the Decision component, see [Properties of the Conditions components](../reference/conditions-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **Conditions** &gt; **Decision**.

2.  Drag the Decision component to the Design surface.

3.  Double-click the field under the DECISION component bar.![Enable the Decision component field.](../image/decision-enable-field.png)

4.  Enter the condition in the field, such as a=5 where "a" is the parameter.

    A Data In port is dynamically created.

5.  To enter a value in the Data In field, see [Configure port properties](configure-input-port-properties.md).

6.  Connect the data and control ports of the Decision component to the corresponding ports of the other components.

    |Port type|Port name|Data type|Purpose of connection|Default Value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data In|The name is the same as the name of the parameter. For example, in the condition a=5, "a" will be the port name.|Object|Takes the input or data for the parameters that are created in the condition.|None|It's mandatory when you define parameters. Else, it's optional.|

7.  To test the component, right-click the component bar and then click **Run From Here**.


## Accept an input and match with a condition

In the DECISION component, a conditional expression "i=10" is set. Since "i" is the parameter, an input port is dynamically created in the component. The Variable \([Create and use a variable in RPA Desktop Design Studio](configure-variables-rpa-studio.md)\) component provides the input "5" to the Decision component which is False. Hence, the False Output port takes control and the Show \([Use the Show component](use-general-messagebox-show.md)\) component shows the message "False." ![Use of the Decision component](../image/Decision.PNG)

**Parent Topic:**[Conditions](../concept/conditions-components.md)

