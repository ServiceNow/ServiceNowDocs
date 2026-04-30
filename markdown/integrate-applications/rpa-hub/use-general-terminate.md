---
title: Use the Terminate component
description: Abort an automation by using the Terminate component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Terminate component

Abort an automation by using the Terminate component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Terminate component. For more information about these properties, see [Properties of the General components](../reference/Properties-general-components.md).

Use the Terminate component in attended automations to complete the automation execution. For more information about the embedded task automation, [Embedded Task Automation in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Terminate**.

2.  Drag the Terminate component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Terminate component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Purpose of connection

</th><th>

Port type

</th><th>

Data type

</th><th>

Mandatory?

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Message

</td><td>

Takes the message when an automation is terminated. This message is also shown in the process job.

</td><td>

Data In

</td><td>

String

</td><td>

No. Connecting the port is optional.

</td><td>

If the Boolean input in the Mark As Error port is True, then you must provide a message.

</td></tr><tr><td>

Mark As Error

</td><td>

Takes the Boolean value that indicates the status of the process job. If True, the state of the process job is Failed. If False, the status of the process job is a success.

</td><td>

Data In

</td><td>

Boolean

</td><td>

No. Connecting the port is optional.

</td><td>

You can view the status of the process job under the **Process Jobs** tab of the respective process in the instance.

</td></tr><tr><td>

Capture Screen

</td><td>

Takes the Boolean value that indicates whether the component captures the screenshot when an automation fails to execute. If True, the screen is captured at that point in time. If False, the screen is not captured.

**Note:** Ensure that the **Track Execution Logs** setting is enabled in your bot process record in RPA Hub. If Flat file is selected as an output type, then the screenshots are not captured.

</td><td>

Data In

</td><td>

Boolean

</td><td>

No. Connecting the port is optional.

</td><td>

To view the screenshot, do the following actions: 1.  On the **Design** tab, click **Attach** **&gt; Remote log**.
2.  Select the required process job and click **Fetch Logs**.
3.  Click **Play log**.

The Execution log window shows the screenshot.

</td></tr></tbody>
</table>5.  To test the component, right-click the component bar and then click **Run From Here**.


## Example

For example, in the automation workflow that requires to read data from an Excel, For Each loop and GetListItem components are used to extract data from the DataTable and display in a message box. If any error occurs while reading the data from the Excel, you can use the Try Catch component to handle the exception and the Terminate component to end the automation. The error message is also shown in process job.

![Terminate component in a simple automation workflow after the Try Catch component. Terminate component displaying Message, Mark As Error, and Capture screen parameters.](../image/general-termininate-comp-rpa.png)

**Parent Topic:**[General](../concept/general-component.md)

