---
title: Use the GetRandomFileName component
description: Get randomly generated file names and their extensions by using the GetRandomFileName component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the GetRandomFileName component

Get randomly generated file names and their extensions by using the GetRandomFileName component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetRandomFileName component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the GetRandomFileName component to the Design surface.

3.  Connect the data and control ports of the GetRandomFileName component to the corresponding ports of the other component as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data Out \(Return\)

</td><td>

Returns the random file name and extension and passes to the next component

</td><td>

Yes.To preview the data, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Passes the file names from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Connects to the Control In port of another component or the default end component.

</td><td>

No. Connecting the port is optional.

</td></tr></tbody>
</table>4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[File](../concept/file.md)

