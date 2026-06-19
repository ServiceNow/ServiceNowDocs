---
title: Use the SetProperty component
description: Set the properties of an object instance by using the SetProperty component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-utility-reflection-setproperty.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reflection, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the SetProperty component

Set the properties of an object instance by using the SetProperty component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the SetProperty component. For more information about these properties, see [Properties of the Reflection components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/util-reflection-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Reflection**.

2.  Drag the SetProperty component to the Design surface.

3.  On the SetProperty component bar, click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

4.  To add a property, click the add property icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add property icon.\).

5.  In the **Property Name** box, enter the property name.

6.  Update the property data type from the list.

7.  To configure input fields, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

8.  Connect the data and control ports of the SetProperty component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Instance\)|Passes the object from a previously executed component.|No. Connecting the port is optional.|
    |Data Out \(Object\)|Passes the object properties from a previously executed component.|No. Connecting the port is optional.|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|Yes|

9.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Reflection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/reflection-utility.md)

