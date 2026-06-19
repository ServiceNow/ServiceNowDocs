---
title: Use the DeleteDirectory component
description: Delete a directory by using the DeleteDirectory component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-directory-deletedirectory.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Directory, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the DeleteDirectory component

Delete a directory by using the DeleteDirectory component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the DeleteDirectory component. For more information about these properties, see [Properties of the Directory components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/util-directory-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Directory**.

2.  Drag the DeleteDirectory component to the Design surface.

3.  Connect the data and control ports of the DeleteDirectory component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(directoryPath\)|Takes the path to the directory from a previously executed component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No. Connecting the port is optional.|

4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/directory.md)

