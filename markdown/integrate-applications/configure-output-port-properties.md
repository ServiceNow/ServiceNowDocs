---
title: Configure output port properties
description: Configure the ways the output ports or fields of components or methods return output in the RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Configure output port properties

Configure the ways the output ports or fields of components or methods return output in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## Procedure

1.  Right-click the output field or Data out port of the component or method.

2.  Click **Override**.

3.  Configure how the method or component processes the output as given in the table.

<table id="table_r4z_hxd_rsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sensitive Data

</td><td>

Option to hide the data from the default view on the Design surface.

</td></tr><tr><td>

Write Data To

</td><td>

Field that appears for Data Out ports only. There are two options:-   **Connection**: Pass the data to another component.
-   **Variable**: Map a global or a local variable from where the data must be written. If you select this option, the Data Out port on the component disappears and the variable name appears on the port. For more information, see [Create and use a variable in RPA Desktop Design Studio](configure-variables-rpa-studio.md).


</td></tr></tbody>
</table>
**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

