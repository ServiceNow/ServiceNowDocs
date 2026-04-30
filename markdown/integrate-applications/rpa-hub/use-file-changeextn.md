---
title: Use the ChangeExtension component
description: Change the extension of a path string by using the ChangeExtension component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the ChangeExtension component

Change the extension of a path string by using the ChangeExtension component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ChangeExtension component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the ChangeExtension component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ChangeExtension component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port Name

</th><th>

Port type

</th><th>

Data Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Path

</td><td>

Data In

</td><td>

String

</td><td>

Takes the path to the file for which the method changes the extension from a previously executed component.

</td></tr><tr><td>

Extension

</td><td>

Data In

</td><td>

String

</td><td>

Takes the new extension \(with or without a leading period\) that the method changes from a previously executed component.Specify null to remove an existing extension from path.

</td></tr><tr><td>

Return

</td><td>

Data Out

</td><td>

String

</td><td>

Returns the changed extension value in string format.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[File](../concept/file.md)

