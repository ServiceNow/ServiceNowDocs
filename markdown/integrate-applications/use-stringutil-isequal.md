---
title: Use the IsEqual component
description: Check whether two string objects have the same value by using the IsEqual component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the IsEqual component

Check whether two string objects have the same value by using the IsEqual component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the IsEqual component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the IsEqual component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

    **Note:** The component considers the case of the string values as it performs a case-sensitive comparison.

4.  Connect the data and control ports of the IsEqual component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Text1\)|Takes the first of the two strings that the component compares from a previously executed component.|Yes|
    |Data In \(Text2\)|Takes the last of the two strings that the component compares from a previously executed component.|yes|
    |Data Out \(Boolean\)|Returns the Boolean value indicating whether the strings matched and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

