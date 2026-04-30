---
title: Use the Try Catch component
description: Catch an error or exception that occurs in a component in an automation and transfer control to the other components within the automation.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Try Catch component

Catch an error or exception that occurs in a component in an automationand transfer control to the other components within the automation.

## Before you begin

Role required: none

## About this task

To configure the properties for the Try Catch component, see [Properties of the Try Catch component](../reference/Properties-general-components.md#Try-Catch-component).

For details on the issues related to the Try Catch component, see [KB article KB1123551](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123551), [KB article KB1123552](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123552), and [KB article KB1123556](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123556).

The Try Catch component enables you to define which components run within the exception-handling scope and which run outside it. When an error occurs in a component within the Try scope, the component captures the exception and stops execution of the remaining components in that path. You can connect an alternative flow to the On Error port to handle the exception. Components that must run outside the exception-handling scope can be connected to the Finally port.

You can use multiple instances of the Try Catch component in an automation to handle errors from other components along the same execution path. If an activity that contains a Try Catch component calls another activity that doesn’t include the Try Catch component, the Try Catch component in the calling activity can still catch errors from the called activity.

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Try Catch**.

2.  Drag the Try Catch component to the Design surface.

3.  Connect the ports of the Try Catch component to the corresponding ports of the other components or activities as described in the following table.

<table id="table_gtq_gq1_ntb"><thead><tr><th>

Port type

</th><th>

Port name

</th><th>

Data type

</th><th>

Purpose of connection

</th><th>

Default value

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Control Out

</td><td>

Control-Out

</td><td>

Not applicable

</td><td>

When there is no error, passes the control to another component or an activity.

</td><td>

Not applicable

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

On Error

</td><td>

Not applicable

</td><td>

Passes the control to another component or activity after the Try Catch component catches an error.Use this port after the Try Catch component catches an error or exception and you want to execute another component in the current or another activity.

</td><td>

Not applicable

</td><td>

No. Connecting the port is optional.

</td></tr><tr><td>

Data Out

</td><td>

Error Message

</td><td>

String

</td><td>

Returns the error message.

</td><td>

Not applicable

</td><td>

No. Connecting the port is optional.

</td></tr><tr><td>

Data Out

</td><td>

Finally

</td><td>

Not applicable

</td><td>

Enables you to execute component or activity after Try and Catch, regardless of whether an exception occurs or not.

</td><td>

Not applicable

</td><td>

No. Connecting the port is optional.

</td></tr></tbody>
</table>4.  To test the component, right-click the component bar and then select **Run From Here**.

    **Note:** The Try Catch component may not work as expected with the Parallel component.


## Handling errors while processing an Excel file

An automation uses a **Try Catch** component when reading data from Excel. If the ReadFromExcel component fails because the file path is empty, the **Try Catch** component captures the error and displays the error message using a MessageBox. The **Finally** path then runs and displays the current date and time before the automation ends.

![Example of exception handling in the Try Catch block.](../image/Trycatch_2.PNG)

**Parent Topic:**[General](../concept/general-component.md)

