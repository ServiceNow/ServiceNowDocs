---
title: Use the String component
description: Generate a random string by using the String component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-utilities-random-string.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Random, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the String component

Generate a random string by using the String component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the String component. For more information about these properties, see [Properties of the Random components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/properties-random-component.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Random**.

2.  Drag the String component to the Design surface.

3.  Connect the data and control ports of the String component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Size\)|Takes the length of the string from a previously executed component.|Yes|
    |Data Out|Returns the random string and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|Yes|

4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Random](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/random.md)

