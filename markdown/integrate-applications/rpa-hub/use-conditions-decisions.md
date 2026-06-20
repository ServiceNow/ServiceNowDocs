---
title: Use the Decision component
description: Automate the decision-making process by using the Decision component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-conditions-decisions.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Conditions, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Decision component

Automate the decision-making process by using the Decision component in RPA Desktop Design Studio.

Watch this video to learn how to use the Decision component.

How to use the Decision component 

## Before you begin

Role required: none

## About this task

You can specify a conditional expression in the component. If the expression contains any parameters, they appear as input ports. If the expression is correct based on the inputs provided, then the True Output Port takes control. Else, the False Output port takes control and executes the automation.

For defining conditions, the Decision component provides many functions, operators, and expressions. For more information, see [Functions, data types, and operators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/conditions-decision-func-opr.md).

To configure the properties for the Decision component, see [Properties of the Conditions components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/conditions-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **Conditions** &gt; **Decision**.

2.  Drag the Decision component to the Design surface.

3.  Double-click the field under the DECISION component bar.\[Omitted image "decision-enable-field.png"\] Alt text: Enable the Decision component field.

4.  Enter the condition in the field, such as a=5 where "a" is the parameter.

    A Data In port is dynamically created.

5.  To enter a value in the Data In field, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-input-port-properties.md).

6.  Connect the data and control ports of the Decision component to the corresponding ports of the other components.

    |Port type|Port name|Data type|Purpose of connection|Default Value|
    |---------|---------|---------|---------------------|-------------|
    |Data In|The name is the same as the name of the parameter. For example, in the condition a=5, "a" will be the port name.|Object|Takes the input or data for the parameters that are created in the condition.|None|

7.  To test the component, right-click the component bar and then click **Run From Here**.


## Accept an input and match with a condition

In the DECISION component, a conditional expression "i=10" is set. Since "i" is the parameter, an input port is dynamically created in the component. The Variable \([Create and use a variable in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-variables-rpa-studio.md)\) component provides the input "5" to the Decision component which is False. Hence, the False Output port takes control and the Show \([Use the Show component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-general-messagebox-show.md)\) component shows the message "False." \[Omitted image "Decision.PNG"\] Alt text: Use of the Decision component

**Parent Topic:**[Conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/conditions-components.md)

