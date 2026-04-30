---
title: Override a data port
description: Override a data port of a component in RPA Desktop Design Studio so that you can change the default behavior of the Data In and Data Out ports. By overriding a data port, you can simplify the automation workflow development and testing.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Override a data port

Override a data port of a component in RPA Desktop Design Studio so that you can change the default behavior of the Data In and Data Out ports. By overriding a data port, you can simplify the automation workflow development and testing.

## Before you begin

Configure a component. For more information, see [Use a component in RPA Desktop Design Studio](configure-components.md).

Role required: none

## Procedure

1.  In the RPA Desktop Design Studio, on the Design surface, right-click the Data In or Data Out port of a component that you want to override and select **Port Properties**.

2.  In the PORT PROPERTIES dialog box, edit the details as needed.

<table id="table_v4q_trh_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Port Name

</td><td>

Name of the port.You can't edit this field.

</td></tr><tr><td>

Data Type

</td><td>

Input or output data type of the component:-   **Object**
-   **String**
-   **Integer**
-   **Long**
-   **Boolean**
-   **Float**
-   **Double**
-   **DateTime**
-   **Image**
-   **List**
-   **Table**
-   **Secure String**


</td></tr><tr><td>

Sensitive Data

</td><td>

Option to hide the data from the default view on the Design surface.You can also mark the data as sensitive by doing the following steps:

1.  Right-click the Data In or Data Out Port.
2.  Click **Mark Data as Sensitive**.


</td></tr><tr><td>

Read Data From

</td><td>

Field that appears for the Data In ports only. There are three options:-   **Connection**: Pass the data from another component.
-   **Static**: Define a static value or select a static option that is associated with the component. If you select this option, the Data In port on the component disappears.
-   **Variable**: Map a global or a local variable from where the data must be read. If you select this option, the Data In port on the component disappears and the variable name appears on the port. For more information, see [Create and use a variable in RPA Desktop Design Studio](configure-variables-rpa-studio.md).


</td></tr><tr><td>

Write Data From

</td><td>

Field that appears for Data Out ports only. There are two options:-   **Connection**: Pass the data to another component.
-   **Variable**: Map a global or a local variable from where the data must be written. If you select this option, the Data Out port on the component disappears and the variable name appears on the port. For more information, see [Create and use a variable in RPA Desktop Design Studio](configure-variables-rpa-studio.md).


</td></tr><tr><td>

Static Value

</td><td>

Value of the specific Data port.This field appears when you select **Static** in the **Read Data From** field.

</td></tr></tbody>
</table>3.  Click **OK**.


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

