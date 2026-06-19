---
title: Use the GetProcessParameters component
description: Get the values of a process parameter you had set for a bot process in RPA Hub with the GetProcessParameters component in the RPA Desktop Design Studio. The component returns both the individual values of the parameters and all values as an object.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-processprm-getprsprms.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Process Parameters, RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetProcessParameters component

Get the values of a process parameter you had set for a bot process in RPA Hub with the GetProcessParameters component in the RPA Desktop Design Studio. The component returns both the individual values of the parameters and all values as an object.

## Before you begin

Set at least two process parameters as part of a bot process on the RPA Hub. See [Create a process parameter within a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/create-process-parameter-botprocess.md).

Assign the automation to the bot process by using the **Assign bot process** option from the **Design** tab of RPA Desktop Design Studio. You must set the same bot process and robot associated with the process parameter. For more information, see [Assign bot process to an automation project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/assign-bot-process.md).

Role required: none

## About this task

You can configure the properties for the GetProcessParameters component. For more information about these properties, see [Properties of the Process Parameters components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/processprm-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **RPA Hub** &gt; **Process Parameters**.

2.  Drag the GetProcessParameters component to the Design surface.

3.  Click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

4.  Click the add key icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add key icon.\).

5.  Enter the name of one of the process parameters.

    A Data In port is created.

6.  Update the process parameter data type.

7.  Repeat the steps to add more parameters.

8.  Click **OK**.

9.  Connect the data and control ports of the GetProcessParameters component to the corresponding ports of other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data Out \(Parameter\)|Returns the value of an individual process parameter and passes to the next component.|Yes|
    |Data Out \(Object\)|Returns the values of process parameters you had set in the component as an object and passes to the next component.|Yes|
    |Control In|Connect to the Control Out port of one or more components.|Yes|
    |Control Out|Connect to the Control In port of another component or the default end component.|Yes|

10. To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Process Parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/process-parameters.md)

