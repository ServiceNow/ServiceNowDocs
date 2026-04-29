---
title: Configure port properties
description: Configure how data is passed to the input fields of a component or method in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Configure port properties

Configure how data is passed to the input fields of a component or method in RPA Desktop Design Studio.

## Before you begin

Role required: none

## Procedure

1.  On the Design surface, right-click a port or the associated field of a method or component.

2.  Click **Port Properties**.

3.  In the Port Properties dialog box, configure the port properties.

<table id="table_yyj_vqw_qsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Type

</td><td>

Specifies the data type of the input that you are passing to the component or method. This option is enabled when the input field requires that you pass a variable or parameter to the field.

</td></tr><tr><td>

Sensitive Data

</td><td>

Option to hide the data from view on the Design surface.You can also set this option by right-clicking the port and selecting **Mark Data as Sensitive**.![Mark-Data-as-Sensitive-option](../image/mark-data-as-sensitive.png)

</td></tr><tr><td>

Read Data From

</td><td>

The **Read Data From** field appears only for Data In ports, and includes the following options:-   **Connection**: Pass the data from another component.
-   **Static**: An unchanging value that is associated with the component. Use data specified in the Static Value field of this dialog box. When you select this option, the Data in port on the component disappears.

**Note:** This option does not appear in some components and methods.

-   **Variable**: A global or a local variable from where the data must be read. When you select this option, the Data in port on the component disappears and the variable name appears on the port. For more information about variables, see [Create and use a variable in RPA Desktop Design Studio](configure-variables-rpa-studio.md).


</td></tr><tr><td>

Write Data To

</td><td>

The **Write Data To** field appears only for Data Out ports and includes the following options: -   **Connection**: Send data to another component.
-   **Variable**: Use data from a global or a local variable. When you select this option, the variable name appears on the port, and the Data Out port is not present. For more information about variables, see [Create and use a variable in RPA Desktop Design Studio](configure-variables-rpa-studio.md).


</td></tr><tr><td>

Static Value

</td><td>

The value that is attached to the port. This field appears when you select **Static** in the **Read Data From** field.

</td></tr><tr><td>

Mapped Variable

</td><td>

The variable that is mapped to the port. This field appears when you select **Variable** in the **Read Data From** field.

</td></tr></tbody>
</table>
**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

