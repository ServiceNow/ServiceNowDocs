---
title: Use the Try Catch component
description: Catch an error or exception that occurs in a component in an automation.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Try Catch component

Catch an error or exception that occurs in a component in an automation.

## Before you begin

Role required: none

## About this task

To configure the properties for the Try Catch component, see [Properties of the Try Catch component](../reference/Properties-general-components.md#Try-Catch-component).

For details on the issues related to the Try Catch component, see [KB article KB1123551](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123551), [KB article KB1123552](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123552), and [KB article KB1123556](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123556).

You can use multiple instances of the Try Catch component in an automation to handle errors from other components along the same execution path. When the Try Catch component catches an error or exception in a component, the automation after the failed component doesn’t execute. The Try Catch component returns the error message and can optionally execute an alternative flow which is connected to its On Error port. If an activity comprising a Try Catch component calls another activity with no Try Catch component along the same execution path and after its Try Catch component, the Try Catch component can catch errors, if any, in the called activity.

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

When there us no error, passes the control to another component or an Activity.

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

</td></tr></tbody>
</table>4.  To test the component, right-click the component bar and then select **Run From Here**.

    **Note:** The Try Catch component may not work as expected with the Parallel component.


## The TRY CATCH component catches the error from the ReadFromExcel method

The Try Catch component catches the error from the ReadFromExcel method. The On Error port then passes the control to the Show component.

![Try Catch error.](../image/Trycatch_2.PNG)

**Parent Topic:**[General](../concept/general-component.md)

