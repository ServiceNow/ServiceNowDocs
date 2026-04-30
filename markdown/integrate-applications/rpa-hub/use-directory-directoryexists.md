---
title: Use the DirectoryExists component
description: Find out if a directory exists by using the DirectoryExists component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Directory, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the DirectoryExists component

Find out if a directory exists by using the DirectoryExists component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the DirectoryExists component. For more information about these properties, see [Properties of the Directory components](../reference/util-directory-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Directory**.

2.  Drag the DirectoryExists component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the DirectoryExists component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(directoryPath\)

</td><td>

Takes the path to the directory and its name from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns **True** if the specified directory exists. Otherwise, it returns **False** and passes to the next component.

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


**Parent Topic:**[Directory](../concept/directory.md)

