---
title: Use the CloseMainWindow component
description: Closes any Windows application by providing the Process ID as input.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System process, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the CloseMainWindow component

Closes any Windows application by providing the Process ID as input.

## Before you begin

Role required: none

## About this task

You can configure the properties for the CloseMainWindow component. For more information about these properties, see [Properties of the System Process components](../reference/util-sysprocess-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **System Process**.

2.  Drag the CloseMainWindow component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the CloseMainWindow to the corresponding ports of the other component as described in the following table.

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

The process ID of the application to close. You can pass this value from a previously executed component.

You can get the ProcessId by opening the Task Manager on your Windows machine.

-   **Example:**

ProcessId of Services.exe: 660

</td><td>

Data In

</td><td>

Yes

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


## Example

As part of your automation workflow, after you have opened an app, such as Windows Terminal and ran a command on it, you can close the app window by providing the process ID in the CloseMainWindow component.

Add the Start App component and GetWindowProcessID component before the CloseMainWindow component and connect the ports as shown in the image.

For more information about these components, see [Use the Start App component](use-general-start-app.md) and [Use the GetWindowProcessID component](use-sysprocess-getwindprocessid.md).

![CloseMainWindow component in a simple workflow showing ProcessId as parameter.](../image/closemainwindow-sys-process-rpa.png)

**Parent Topic:**[System process](../concept/system-process-utilities.md)

