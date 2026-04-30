---
title: Use the GetTempFileName component
description: Get the names of temporary Windows files by using the GetTempFileName component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the GetTempFileName component

Get the names of temporary Windows files by using the GetTempFileName component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetTempFileName component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the GetTempFileName component to the Design surface.

3.  Connect the data and control ports of the GetTempFileName component to the corresponding ports of the other component as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data Out \(Return\)

</td><td>

Returns the new temporary file name and path on the disk and passes to the next component to be executed.

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
</table>4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[File](../concept/file.md)

