---
title: Use the UtcNow component
description: Get the current date and time of the system in the Coordinated Universal Time \(UTC\) format by using the UtcNow component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DateTime, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the UtcNow component

Get the current date and time of the system in the Coordinated Universal Time \(UTC\) format by using the UtcNow component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the UtcNow component. For more information about these properties, see [Properties of the DateTime components](../reference/util-datetime-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **DateTime**.

2.  Drag the UtcNow component to the Design surface.

3.  Connect the data and control ports of the UtcNow component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data Out

</td><td>

Passes the current date in the UTC format.

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
</table>4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[DateTime](../concept/datetime-utility.md)

