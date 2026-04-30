---
title: Use the ChangeExtension component
description: Change the extension of a file by using the ChangeExtension component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the ChangeExtension component

Change the extension of a file by using the ChangeExtension component in RPA Desktop Design Studio.

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

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Path\)

</td><td>

Takes the path to the file for which the method changes the extension from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Extension\)

</td><td>

Takes the new extension that the method changes from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the path with the changed extension and passes to the next component.

</td><td>

Yes.To preview the data, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Connects to the Control Out port of one or more components.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Connects to the Control In port of another component or the default end component.

</td><td>

No. Connecting the port is optional.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


## ChangeExtension component

Your RPA robot processes a batch of report files downloaded with `.txt` extension. To ensure consistency and compatibility with downstream systems, you need to rename these files to the `.doc` extension, after processing.

1.  Enter a variable component on the design canvas that stores the file path with extension.
2.  Add the ChangeExtension action after the variable component.
3.  Set the target extension to `.pdf`.

![changeExtension component with .docx extension.](../image/change-extension-rpa.png)

**Parent Topic:**[File](../concept/file.md)

