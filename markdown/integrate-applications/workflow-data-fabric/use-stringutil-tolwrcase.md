---
title: Use the ToLowerCase component
description: Convert an uppercase text to lowercase letters by using the ToLowerCase component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-stringutil-tolwrcase.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the ToLowerCase component

Convert an uppercase text to lowercase letters by using the ToLowerCase component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ToLowerCase component. For more information about these properties, see [Properties of the String Utilities components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the ToLowerCase component to the Design surface.

3.  To configure the input fields, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

4.  Connect the data and control ports of the ToLowerCase component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Text\)|Takes the text that the component converts to lowercase from a previously executed component.|Yes|
    |Data Out \(String\)|Returns the lowercase text and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|In|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/string-utilities.md)

