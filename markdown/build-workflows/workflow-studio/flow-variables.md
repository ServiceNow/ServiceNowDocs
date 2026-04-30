---
title: Flow variables
description: Similar to Workflow scratchpad variables, create variables that you can use and modify directly in your flow. Access flow variables as data pills directly in the Data panel.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Flow variables

Similar to Workflow scratchpad variables, create variables that you can use and modify directly in your flow. Access flow variables as data pills directly in the Data panel.

Use flow variables to set and retrieve values throughout a flow. Flow variables are similar to subflow inputs and outputs. Both define data available to a flow or subflow. The main difference between them is when they are accessible. Flow variables are accessible throughout a flow. Inputs are only accessible at the start of a subflow, and outputs are only accessible when a subflow completes.

## Creating flow variables

Create variables with the **Flow Variables** option on the More Actions menu. You can create several variables at a time by choosing a name and data type for each one. Flow variables appear as data pills in the Flow Variables section of the Data panel.

## Assigning values to flow variables

Assign values to variables with the Set Flow Variables flow logic. Set Flow Variables has the following inputs:

-   The name of the variable.
-   The data value for the variable.

You can assign values to all of your variables with a single use of Set Flow Variables. Unlike other data pills, the values assigned to flow variables are mutable and can be changed at any time. Using Set Flow Variables overrides the current value of the variable. If no value is assigned to a variable, the default value is **null**.

Flow variable values are set in the order in which they're assigned from top to bottom. If you set the value of the same variable multiple times, the flow only uses the last value set. For example, these three variable definitions result in the variable having the runtime value of `last value set`.

|Order|Variable|Configuration|
|-----|--------|-------------|
|1|variable|first value set|
|2|variable|second value set|
|3|variable|last value set|

Variable values can reference any data pill from earlier in the flow, including other variables. If you set variable values by reference to other data pills, you must maintain the order of the variable assignments. The referenced value must always come before the variable that uses the referenced value. Changing the order may produce null values. For example, these variable definitions only produce the expected runtime values when you maintain the order of the variable definitions.

|Order|Variable|Configuration|Runtime Value|
|-----|--------|-------------|-------------|
|1|variable1|One|One|
|2|variable2|\{variable1\}, Two|One, Two|
|3|variable3|\{variable1\}, \{variable2\}, Three|One, Two, Three|

## Flow execution details

A summary of the Set Flow Variables flow logic appears in the execution details. The details show the name, type, configuration, and runtime values for all the variables set with the action. Execution details also provide information about the variables when they're used in actions or flow logic. In that case, it shows the type, configuration, and runtime values.

## Supported data types

Workflow Studio supports the following data types for flow variables:

-   Date/Time
-   Decimal
-   Floating-point number
-   Integer
-   JSON
-   Reference
-   String
-   True/False

-   **[Create a flow variable](../task/create-flow-variables.md)**  
Create a flow variable to store and retrieve a value throughout a flow.

**Parent Topic:**[Building flows](flows.md)

