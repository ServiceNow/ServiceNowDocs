---
title: Use the Format Text component
description: Format the text by using variable placeholders and line and tab variables with the Format Text component in RPA Desktop Design Studio. You can update the text and their positions easily by just updating the variable placeholders and the line and tab variables.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Format Text component

Format the text by using variable placeholders and line and tab variables with the Format Text component in RPA Desktop Design Studio. You can update the text and their positions easily by just updating the variable placeholders and the line and tab variables.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Format Text component. For more information about these properties, see [Properties of the General components](../reference/Properties-general-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Format Text**.

2.  Drag the Format Text component to the Design surface.

3.  To set the text placeholder variable, do the following steps.

    1.  Click the add variable icon \(![Add variable icon.](../image/add-image-icon.png)\).

        A Data In port is added for each variable you add.

    2.  To configure the variable value, see [Configure port properties](configure-input-port-properties.md).

    3.  Repeat the steps to add more variables and values.

4.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

5.  Insert the text in the TEXT FORMAT EDITOR.

6.  Insert the text.

7.  Insert the line separator \\n or tab separator \\t variable at appropriate places within the text.

8.  Insert the text variable placeholders within the text body, wherever appropriate.

    **Tip:** To update the text, update the placeholder value.

9.  Connect the data and control ports of the Format Text component to the corresponding ports of the other component as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Variable\)

</td><td>

Takes the variable value from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out \(Formatted Output\)

</td><td>

Returns the formatted text and passes to the next component.

</td><td>

Yes.To view the output, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Passes the control from the previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Passes the control to the next component.

</td><td>

No. Connecting the port is optional.

</td></tr></tbody>
</table>10. To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[General](../concept/general-component.md)

