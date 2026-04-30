---
title: Use the GetLastModifiedFile component
description: Get the name and path to the last modified file in a directory by using the GetLastModifiedFile component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the GetLastModifiedFile component

Get the name and path to the last modified file in a directory by using the GetLastModifiedFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetLastModifiedFile component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the GetLastModifiedFile component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetLastModifiedFile component to the corresponding ports of the other component as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Folderpath\)

</td><td>

Takes the path to the directory from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(searchSubDirectories\)

</td><td>

Takes the Boolean response to indicate whether the method searches subdirectories inside the target directory from a previously executed component.

</td><td>

No. Connecting the port is optional.

</td></tr><tr><td>

Data In \(fileExtension\)

</td><td>

If you want to find files by their extensions, then use this option. Takes the extension of a file type from a previously executed component.

</td><td>

No. Connecting the port is optional.

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns the path to the file and its name that were modified last.

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


**Parent Topic:**[File](../concept/file.md)

