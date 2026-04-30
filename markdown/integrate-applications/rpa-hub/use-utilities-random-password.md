---
title: Use the Password component
description: Generate any random password by using the Password component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Random, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Password component

Generate any random password by using the Password component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can define the complexity of the password based on the following rules:

-   Define the length of the password. 11 is the default length.
-   Number of lowercase characters. The default number is 1.
-   Number of uppercase characters. The default number is 1.
-   Symbols. The default symbols are "~!@\#$%^&amp;\*\(\)\_-+=;?\\/"
-   Number of symbols: The default count is 1.
-   Numbers. The default number is 1.

To configure the properties for the Password component, see [Properties of the Random components](../reference/properties-random-component.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Random**.

2.  Drag the Password component to the Design surface.

3.  To provide the inputs to the fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Password component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data In|Length|Integer|Takes the length of the password.|11|Yes|
    |Data In|Lowercase|Integer|Takes the number of lowercase characters to be included in the password.|1|Yes|
    |Data In|Uppercase|Integer|Takes the number of uppercase characters to be included in the password.|1|Yes|
    |Data In|Symbols|String|Takes the symbols to be included in the password.|~!@\#$%^&amp;\*\(\)\_-+=;?\\/|Yes|
    |Data In|SymbolsCount|Integer|Takes the count of symbols to be included in the password.|1|Yes|
    |Data In|Numbers|Integer|Takes the total count of numbers to be included in the password.|1|Yes|
    |Data Out|Return|String|Returns the random password.|Not applicable|Not applicable|

5.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Random](../concept/random.md)

