---
title: Use the ConsoleLog component
description: Write a message to view the console log of RPA Desktop Design Studio by using the ConsoleLog component.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Debug, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the ConsoleLog component

Write a message to view the console log of RPA Desktop Design Studio by using the ConsoleLog component.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ConsoleLog component. For more information about these properties, see [Properties of the Debug components](../reference/util-debug-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Debug**.

2.  Drag the ConsoleLog component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ConsoleLog component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Description

</th><th>

Data port type

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Message

</td><td>

Provide a message that must to be written to the console log.For example, `started first activity` or `completed the first activity`.

</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


## Result

Open the console log to check the messages.

![Console displaying messages provided in the ConsoleLog component.](../image/console-log-debug-studio.png "Console with provided messages in the ConsoleLog component")

**Parent Topic:**[Debug](../concept/debug-utility.md)

