---
title: Use the GetAsTable component
description: Get the content of the clipboard as a data table as part of an automation Workflow by using the GetAsTable component in the RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Clipboard, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetAsTable component

Get the content of the clipboard as a data table as part of an automation Workflow by using the GetAsTable component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetAsTable component. For more information about these properties, see [Properties of the Clipboard components](../reference/util-clipboard-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Clipboard**.

2.  Drag the GetAsTable component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetAsTable component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(ColumnSeperator\)

</td><td>

Passes the column separator for the table columns from the Data Out port of another component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(LineSeperator\)

</td><td>

Passes the data separator for the table columns from the Data Out port of another component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the clipboard content as a data table.

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

Connects to the Control In port of any other component.

</td><td>

No. Connecting the port is optional.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Clipboard](../concept/clipboard.md)

