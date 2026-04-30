---
title: Use the Terminate component
description: End the specified Windows system process by using the Terminate component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System process, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Terminate component

End the specified Windows system process by using the Terminate component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Terminate component. For more information about these properties, see [Properties of the System Process components](../reference/util-sysprocess-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **System Process**.

2.  Drag the Terminate component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Terminate component to the corresponding ports of the other component as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Port type

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

ProcessId

</td><td>

The process ID of the process to terminate. You can pass this value from a previously executed component. You can get the processId by opening the Task Manager on your Windows machine.-   **Example:**

ProcessId of Services.exe: 660

</td><td>

Data In

</td><td>

Yes

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


## Example

As part of your automation workflow, after you have opened an app, such as Windows Terminal and ran a command on it, you can terminate the app by providing the process ID in the Terminate component.![Terminate component in a simple workflow showing ProcessId as parameter.](../image/terminate-system-process-rpa.png)

**Parent Topic:**[System process](../concept/system-process-utilities.md)

