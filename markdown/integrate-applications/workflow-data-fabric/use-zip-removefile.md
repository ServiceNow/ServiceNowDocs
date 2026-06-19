---
title: Use the RemoveFile component
description: Delete a specified file in a zip archive by using the RemoveFile component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-zip-removefile.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zip, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the RemoveFile component

Delete a specified file in a zip archive by using the RemoveFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the RemoveFile component. For more information about these properties, see [Properties of the Zip components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/util-zip-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Zip**.

2.  Drag the RemoveFile component to the Design surface.

3.  To configure the input fields, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

4.  Connect the data and control ports of the RemoveFile component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(zipFilePath\)|Provides the zipFilePath and PathtoExtract Data In ports to extract files to a location.|Yes|
    |Data In \(file\)|Takes the file name from a previously executed component.|Yes|
    |Data Out|Returns **True** if the files are successfully removed. Otherwise, returns **False**.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Zip](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/zip-utilities.md)

