---
title: Use the Start App component
description: Start or launch an application or file by using the START APP component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the Start App component

Start or launch an application or file by using the START APP component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Start App component.

<table id="table_d53_jcp_xtb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delay After Execution

</td><td>

The number of seconds to pause after running.

</td></tr><tr><td>

Delay Before Execution

</td><td>

The number of seconds to pause before running.

</td></tr><tr><td>

Height

</td><td>

Specifies the height of the application window that is launched.

</td></tr><tr><td>

Left

</td><td>

Specifies the location of the application that is launched along the left edge of the screen.

</td></tr><tr><td>

Top

</td><td>

Specifies the location of the application that is launched along the top edge of the screen.

</td></tr><tr><td>

Width

</td><td>

Specifies the width of the application window that is launched.

</td></tr><tr><td>

Enable Timeout

</td><td>

Option to set a timeout value.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds that the operation ends after if not completed. To apply this value, you must set the **Enable Timeout** property.

</td></tr><tr><td>

Max Wait Time in Seconds

</td><td>

Maximum time, in seconds, to wait for the image or application to appear on the screen.The default value is 30 seconds.

</td></tr><tr><td>

Wait For Start

</td><td>

Specifies the wait time \(in seconds\) before the action is executed.

</td></tr><tr><td>

State

</td><td>

Specifies the state in which the Windows based or web-based application is launched. The states are normal, maximized, minimized, hidden, or custom location.

</td></tr></tbody>
</table>## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **START APP**.

2.  Drag the START APP component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Start App component to the corresponding ports of the other component as described in the following table.

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

Data In

</td><td>

File Path

</td><td>

String

</td><td>

Takes the path to the file or the application in the local disk.

</td><td>

No default value

</td><td>

Yes

</td></tr><tr><td>

Data In

</td><td>

Args

</td><td>

String

</td><td>

Takes the arguments for the path.For example, if you provide the local path to the Google Chrome browser, the argument can be https://servicenow.com

</td><td>

No default value

</td><td>

No. Connecting the port is optional.

</td></tr><tr><td>

Data Out

</td><td>

Window Handle

</td><td>

Integer

</td><td>

Returns the window handle of the file or application.

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[General](../concept/general-component.md)

