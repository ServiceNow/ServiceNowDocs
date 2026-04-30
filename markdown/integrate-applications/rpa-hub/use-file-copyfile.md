---
title: Use the CopyFile component
description: Copy an existing file to a new location by using the CopyFile component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the CopyFile component

Copy an existing file to a new location by using the CopyFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the CopyFile component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the CopyFile component to the Design surface.

3.  To configure the input fields, see by doing the following steps.

    1.  Right-click the field.

    2.  Click **Override**.

    3.  Enter details for the following fields, [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the CopyFile component to the corresponding ports of the other components as described in the following table.

<table id="table_wph_dw1_h2c"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

sourcefilePath

</td><td>

Provide a file path to be copied, along with the file name.For example, `C:\Users\ABC\Desktop\ Folders\Txt Files\Scripts.txt`

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

destFilePath

</td><td>

Provide a destination file path \(along with the file name\), where the file should be copied.For example, `C:\Users\ABC\Desktop\Scripts.txt`

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

overwrite

</td><td>

Provide a True or False value. Set to True to overwrite existing files.

</td><td>

Data In

</td><td>

Boolean

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[File](../concept/file.md)

