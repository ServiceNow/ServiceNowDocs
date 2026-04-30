---
title: Use the Combine component
description: Combine two paths to create a single path with the Combine component in RPA Desktop Design Studio. For example, C:\\Users could be the first path and \\Data\\TestFolder could be the second path and both could be combined to create the path C:\\Users\\Data\\TestFolder.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Combine component

Combine two paths to create a single path with the Combine component in RPA Desktop Design Studio. For example, C:\\Users could be the first path and \\Data\\TestFolder could be the second path and both could be combined to create the path C:\\Users\\Data\\TestFolder.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Combine component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the Combine component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Combine component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Path 1\)

</td><td>

Takes the first part of the combined path from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Path 2\)

</td><td>

Takes the last part of the combined path from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out \(String\)

</td><td>

Returns the combined path and passes to the next component.

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

