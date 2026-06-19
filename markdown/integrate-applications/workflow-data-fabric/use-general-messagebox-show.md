---
title: Use the Show component
description: Display custom messages as part of a Attended Robot automation by using the Show component in the RPA Desktop Design Studio
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-general-messagebox-show.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Show component

Display custom messages as part of a Attended Robot automation by using the Show component in the RPA Desktop Design Studio

## Before you begin

Role required: none

## About this task

For example, in an assisted automation, a component could evaluate a user input and show a message `Incorrect Date of Birth` through the Show component.

You can configure the properties for the Show component. For more information about these properties, see [Properties of the General components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/Properties-general-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **MessageBox**.

2.  Drag the Show component to the Design surface.

3.  To configure the input field, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

4.  Connect the data and control ports of the Show component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data in|Message|String|Takes the custom message that the component shows.|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[General](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/general-component.md)

