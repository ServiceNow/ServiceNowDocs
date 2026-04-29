---
title: Use the CreateFile component
description: Zip an existing folder or create a zip file by using the CreateFile component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zip, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the CreateFile component

Zip an existing folder or create a zip file by using the CreateFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the CreateFile component. For more information about these properties, see [Properties of the Zip components](../reference/util-zip-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Zip**.

2.  Drag the CreateFile component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the CreateFile component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(zipFilePath\)

</td><td>

Location of the zip file along with the zip file name that needs to be created.For example, `C:\Users\abel.tutor\Downloads\test.zip`

</td><td>

Yes

</td></tr><tr><td>

Data In \(Path\)

</td><td>

Location of the source file or folder.For example, for file- `C:\Users\abel.tutor\Downloads\test.txt`

For example, for folder- `C:\Users\abel.tutor\Downloads`

</td><td>

Yes

</td></tr><tr><td>

Type

</td><td>

Open port properties and then select either **File** or **Folder** from the **Static Value** field.

</td><td>

Yes

</td></tr><tr><td>

Data Out \(Boolean\)

</td><td>

Returns **True** if the file is successfully created to the specified location. Otherwise, returns **False**.

</td><td>

Yes

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

Yes

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Zip](../concept/zip-utilities.md)

