---
title: Use the IsRunningFromStudio component
description: Determine whether a project is run by studio as part of an automation Workflow using the IsRunningFromStudio component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Debug, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the IsRunningFromStudio component

Determine whether a project is run by studio as part of an automation Workflow using the IsRunningFromStudio component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the IsRunningFromStudio component. For more information about these properties, see [Properties of the Debug components](../reference/util-debug-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Debug**.

2.  Drag the IsRunningFromStudio component to the Design surface.

3.  Connect the data and control ports of the IsRunningFromStudio component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data Out

</td><td>

Returns **True** if a project is being run from the RPA Desktop Design Studio. Otherwise, it returns **False**.

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


**Parent Topic:**[Debug](../concept/debug-utility.md)

