---
title: Use the For Each component
description: Traverse each item in a collection in the order of first to last using the For Each component in the RPA Desktop Design Studio. The collection can be an array, list, or a table.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Loops, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the For Each component

Traverse each item in a collection in the order of first to last using the For Each component in the RPA Desktop Design Studio. The collection can be an array, list, or a table.

## Before you begin

Role required: none

## About this task

You can configure the properties for the For Each component.

|Property|Description|
|--------|-----------|
|Delay After Execution|The number of seconds to pause after running.|
|Delay Before Execution|The number of seconds to pause before running.|
|Delay for each execution \(Seconds\)|Specified delay before an item in the object, array, or a list is executed.|
|Enable Timeout|Option to set a timeout value.|
|Timeout|Number of seconds that the operation ends after if not completed. To apply this value, you must set the **Enable Timeout** property.|

## Procedure

1.  In the Toolbox pane, navigate to **Loops** &gt; **For Each**.

2.  Drag the For Each component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the For Each component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Default value|Mandatory?|
    |---------|---------|---------|---------------------|-------------|----------|
    |Data In|Collection|Object|Takes the collection as an input.|No default value|Yes|
    |Data Out|Current Object|Object|Returns each item from the collection.|Not applicable|Not applicable|

5.  To test the component, under the **DESIGN** tab, click **Run**.


## For Each loop component

Use a For Each loop component to automate user account provisioning. In this scenario, a robot reads an Excel file containing user account requests. Each row in the file includes information such as user name, email, role, and department. The robot processes each request by creating the user account, assigning the appropriate role, and sending a notification to the department manager.

1.  Use the **Data Table** connector to import rows from the Excel file.
2.  Drag a **For Each** component onto the design surface to iterate over the list of request records.
3.  Inside the loop:
    -   Extract fields from the current record.
    -   Navigate to the user management interface and fill in the details.
    -   Submit the form to create the user account.
    -   Send an email notification to the relevant department manager with the account details.

**Parent Topic:**[Loops](../concept/loops.md)

